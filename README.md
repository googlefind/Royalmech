<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Copy Image from GitHub</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }

        #github-image {
            max-width: 100%;
            height: auto;
            margin-bottom: 20px;
        }

        #copy-button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Copy Image from GitHub</h1>
    <img id="github-image" src="https://raw.githubusercontent.com/user/repo/main/Screenshot%202025-01-01%20193539.png" alt="GitHub Image" />
    <button id="copy-button">Copy Image</button>

    <canvas id="canvas" style="display: none;"></canvas>

    <script>
        document.getElementById('copy-button').addEventListener('click', function() {
            const img = document.getElementById('github-image');
            const canvas = document.getElementById('canvas');
            const ctx = canvas.getContext('2d');

            // Set canvas dimensions to match the image
            canvas.width = img.naturalWidth; // Use naturalWidth for the original size
            canvas.height = img.naturalHeight; // Use naturalHeight for the original size

            // Draw the image onto the canvas
            ctx.drawImage(img, 0, 0);

            // Convert the canvas to a Blob and copy to clipboard
            canvas.toBlob(function(blob) {
                const item = new ClipboardItem({ 'image/png': blob });
                navigator.clipboard.write([item]).then(() => {
                    alert('Image copied to clipboard!');
                }).catch(err => {
                    console.error('Failed to copy: ', err);
                });
            }, 'image/png');
        });
    </script>
</body>
</html>
