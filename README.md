<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LETS DO IT</title>
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
            text-decoration: none; /* Remove underline from links */
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
    
    <h1>Download Multiple PDFs from GitHub</h1>
    <div id="buttons-container">
        <!-- Buttons and images will be generated here -->
    </div>

    <script>
        const pdfFiles = [
            { name: 'Drawing 5 Drawing v3', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Drawing%205%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193539.png' },
            { name: 'Plummer block', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Plummer%20Block%20Drawing%20v7.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193553.png' },
            { name: 'Socket and spigot cotter', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Socket%20and%20spigot%20cotter%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193602.png' },
            { name: 'Ramsbottom safety valve', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Ramsbottom%20Safety%20valve%20Drawing%20v2.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193611.png' },
            { name: 'ISO tread form', url: 'https://raw.githubusercontent.com/googlefind/hi/main/ISO%20Thread%20Form%20Drawing%20v1.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193618.png' },
            { name: 'Drawing 1', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Drawing%20Drawing%201.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193625.png' },
            { name: 'Drawing 0', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Drawing%200.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193633.png' },
            { name: 'Machine vice drawing v5', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Machine%20Vice%20Drawing%20v5.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193641.png' },
            { name: 'Drawing 2 Drawing', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Drawing%202%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193649.png { name: 'Connecting Rod drawing', url: 'https://raw.githubusercontent.com/googlefind/hi/main/knuckle%20joint%202%20Drawing%20v2.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193857.png' },
            { name: 'New File 1', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Protected%20Flanged%20Coupling%202%20Drawing%20v2.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193710.png' },
            { name: 'New File 2', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Thread%20Form%204%20Drawing%20v1.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193720.png' },
            { name: 'New File 3', url: 'https://raw.githubusercontent.com/googlefind/hi/main/4%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193727.png' },
            { name: 'New File 4', url: 'https://raw.githubusercontent.com/googlefind/hi/main/universal%20coupling%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193734.png' },
            { name: 'New File 5', url: 'https://raw.githubusercontent.com/googlefind/hi/main/SCREW%20JACK%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193741.png' },
            { name: 'New File 6', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Squre%20Headed%20Boul%20Drawing%20v6.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193754.png' },
            { name: 'New File 7', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Thread%20Form%203%20Drawing%20v2.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193801.png' },
            { name: 'New File 8', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Coil%20Form%201%20Drawing%20v1.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193808.png' },
            { name: 'New File 9', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Coil%20Form%202%20Drawing%20v1.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193819.png' },
            { name: 'New File 10', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Drawing%203%20Drawing%20v5.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193835.png' },
            { name: 'New File 11', url: 'https://raw.githubusercontent.com/googlefind/hi/main/hexagonal%20headed%20bolt%20Drawing%20v3.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193842.png' },
            { name: 'New File 12', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Connecting%20Rod%20Drawing%20v4.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-01%20193848.png' },
            { name: 'model Tail Stock', url: 'https://raw.githubusercontent.com/googlefind/hi/main/Model%20Tail%20Stock.pdf', imgUrl: 'https://raw.githubusercontent.com/googlefind/hi/main/Screenshot%202025-01-04%20081045.png' },
        ];

        const buttonsContainer = document.getElementById('buttons-container');

        pdfFiles.forEach(file => {
            const container = document.createElement('div');
            container.className ```html
            = 'image-container';

            const img = document.createElement('img');
            img.src = file.imgUrl;
            img.alt = file.name;

            const button = document.createElement('a');
            button.href = file.url;
            button.className = 'download-button';
            button.innerText = `Download ${file.name}`;
            button.download = ''; // This attribute allows direct download

            container.appendChild(img);
            container.appendChild(button);
            buttonsContainer.appendChild(container);
        });
    </script>
    <p>MR_VD</p>
</body>
</html>
