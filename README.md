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
            max-width: 300px; 
            width: 100%;     
            height: auto;    
            border: 2px solid #4CAF50;
        }
    </style>
</head>
<body>
    
    <div id="buttons-container">
        <!-- Buttons and images will be generated here -->
    </div>

    <script>
        const pdfFiles = [
            { name: 'Drawing 5 Drawing v3', url: 'https://raw.githubusercontent.com/googlefind/hi/a3cc15f25d35bbd0c0ea3204d958b0c3d5454b4b/Drawing%205%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/addb682a1e3af49bee42a6ebba24cc5527a6d877/Screenshot%202025-01-01%20193539.png' },
            { name: 'Plummer block', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file2.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image2.png' },
            { name: 'Socket and spigot cotter', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file3.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image3.png' },
            { name: 'Ramsbottom safety valve', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file4.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image4.png' },
            { name: 'ISO tread form', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file5.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image5.png' },
            { name: 'Drawing 1', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file6.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image6.png' },
            { name: 'Drawing 0', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file7.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image7.png' },
            { name: 'Machine vice drawing v5', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file8.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image8.png' },
            { name: 'Drawing 2 Drawing', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file9.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image9.png' },
            { name: 'Knuckle joint 2', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file10.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image10.png' },
            { name: 'Protected flanged coupling', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file11.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image11.png' },
            { name: 'Thread form 4', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file12.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image12.png' },
            { name: '4 Drawing', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file13.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image13.png' },
            { name: 'Universal coupling', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file14.pdf', imgUrl: 'https ://raw.githubusercontent.com/johnDoe/myRepo/main/image14.png' },
            { name: 'Screw jack drawing', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file15.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image15.png' },
            { name: 'Square Headed bolt Drawing', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file16.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image16.png' },
            { name: 'Thread form 3', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file17.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image17.png' },
            { name: 'Coil form 1', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file18.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image18.png' },
            { name: 'Coil form 2', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file19.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image19.png' },
            { name: 'Drawing 3 Drawing', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file20.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image20.png' },
            { name: 'File hexagonal headed bolt', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file21.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image21.png' },
            { name: 'Connecting Rod drawing', url: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/file22.pdf', imgUrl: 'https://raw.githubusercontent.com/johnDoe/myRepo/main/image22.png' },
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
            button.innerText = `_ ${file.name}`;
            button.target = '_blank';

            container.appendChild(img);
            container.appendChild(button);
            buttonsContainer.appendChild(container);
        });
    </script>
    <p>MR_VD</p>
</body>
</html>
