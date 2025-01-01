
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download Multiple PDFs from GitHub</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }

        .download-button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            margin: 5px;
        }

        .download-button:hover {
            background-color: #45a049;
        }

        .image-container {
            margin-bottom: 20px;
        }

        .image-container img {
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <h1>Download PDFs</h1>
    <p>Click the buttons below to download the PDF files.</p>
    
    <div id="buttons-container">
        <!-- Buttons and images will be generated here -->
    </div>

    <script>
        const pdfFiles = [
            { name: 'Drawing 5 Drawing v3', url: 'https://raw.githubusercontent.com/googlefind/hi/a3cc15f25d35bbd0c0ea3204d958b0c3d5454b4b/Drawing%205%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/addb682a1e3af49bee42a6ebba24cc5527a6d877/Screenshot%202025-01-01%20193539.png' },
            { name: 'File 2', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file2.pdf', imgUrl: 'https://example.com/image2.jpg' },
            { name: 'File 3', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file3.pdf', imgUrl: 'https://example.com/image3.jpg' },
            { name: 'File 4', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file4.pdf', imgUrl: 'https://example.com/image4.jpg' },
            { name: 'File 5', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file5.pdf', imgUrl: 'https://example.com/image5.jpg' },
            { name: 'File 6', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file6.pdf', imgUrl: 'https://example.com/image6.jpg' },
            { name: 'File 7', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file7.pdf', imgUrl: 'https://example.com/image7.jpg' },
            { name: 'File 8', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file8.pdf', imgUrl: 'https://example.com/image8.jpg' },
            { name: 'File 9', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file9.pdf', imgUrl: 'https://example.com/image9.jpg' },
            { name: 'File 10', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file10.pdf', imgUrl: 'https://example.com/image10.jpg' },
            { name: 'File 11', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file11.pdf', imgUrl: 'https://example.com/image11.jpg' },
            { name: 'File 12', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file12.pdf', imgUrl: 'https://example.com/image12.jpg' },
            { name: 'File 13', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file13.pdf', imgUrl: 'https://example.com/image13.jpg' },
            { name: 'File 14', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file14.pdf', imgUrl: 'https://example.com/image14.jpg' },
            { name: 'File 15', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file15.pdf', imgUrl: 'https://example.com/image15.jpg' },
            { name: 'File 16', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file16.pdf', imgUrl: 'https://example.com/image16.jpg' },
            { name: 'File 17', url: 'https://raw.githubusercontent.com/yourusername/yourrepository/main/file17.pdf', imgUrl: 'https://example.com/image17.jpg' },
        ];

        const buttonsContainer = document.getElementById('buttons-container');

        pdfFiles.forEach(file => {
            const container = document.createElement('div');
            container.className = 'image-container';

            const img = document.createElement('img');
            img.src = file.imgUrl;
            img.alt = file.name;

            const button = document.createElement('a');
            button.href = file.url;
            button.className = 'download-button';
            button.innerText = `Download ${file.name}`;
            button.target = '_blank';

            container.appendChild(img);
            container.appendChild(button);
            buttonsContainer.appendChild(container);
        });
    </script>
</body>
</html>
