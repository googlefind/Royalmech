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
    <img id="github-image" src="Screenshot 2025-01-01 193539.png" alt="GitHub Image" />
    <button id="copy-button">Copy Image Link</button>

    <script>
        document.getElementById('copy-button').addEventListener('click', function() {
            const imageUrl = document.getElementById('github-image').src;
            navigator.clipboard.writeText(imageUrl).then(() => {
                alert('Image link copied to clipboard!');
            }).catch(err => {
                console.error('Failed to copy: ', err);
            });
        });
    </script>
</body>
</html>
