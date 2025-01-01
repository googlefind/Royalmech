<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download PDF from GitHub</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }

        #download-button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
        }

        #download-button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <h1>Download PDF</h1>
    <p>Click the button below to download the PDF file.</p>
    
    <button id="download-button">Download PDF</button>

    <script>
        document.getElementById('download-button').addEventListener('click', function() {
            const pdfUrl = 'https://github.com/yourusername/yourrepository/raw/main/yourfile.pdf'; // Replace with your PDF file URL
            const link = document.createElement('a');
            link.href = pdfUrl;
            link.download = 'yourfile.pdf'; // Specify the name for the downloaded file
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        });
    </script>
</body>
</html>
