<!DOCTYPE html>
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
    </style>
</head>
<body>
    <h1>Download PDFs</h1>
    <p>Click the buttons below to download the PDF files.</p>
    
    <div id="buttons-container">
        <!-- Buttons will be generated here -->
    </div>

    <script>
        const pdfFiles = [
            { name:'File1',url:'https://github.com/googlefind/hi/blob/ee4e424ba466242d3399ef68ba132804c40b0065/Drawing%205%20Drawing%20v3.pdf' },
            { name: 'File 2', url: 'https://github.com/yourusername/yourrepository/raw/main/file2.pdf' },
            { name: 'File 3', url: 'https://github.com/yourusername/yourrepository/raw/main/file3.pdf' },
            { name: 'File 4', url: 'https://github.com/yourusername/yourrepository/raw/main/file4.pdf' },
            { name: 'File 5', url: 'https://github.com/yourusername/yourrepository/raw/main/file5.pdf' },
            { name: 'File 6', url: 'https://github.com/yourusername/yourrepository/raw/main/file6.pdf' },
            { name: 'File 7', url: 'https://github.com/yourusername/yourrepository/raw/main/file7.pdf' },
            { name: 'File 8', url: 'https://github.com/yourusername/yourrepository/raw/main/file8.pdf' },
            { name: 'File 9', url: 'https://github.com/yourusername/yourrepository/raw/main/file9.pdf' },
            { name: 'File 10', url: 'https://github.com/yourusername/yourrepository/raw/main/file10.pdf' },
            { name: 'File 11', url: 'https://github.com/yourusername/yourrepository/raw/main/file11.pdf' },
            { name: 'File 12', url: 'https://github.com/yourusername/yourrepository/raw/main/file12.pdf' },
            { name: 'File 13', url: 'https://github.com/yourusername/yourrepository/raw/main/file13.pdf' },
            { name: 'File 14', url: 'https://github.com/yourusername/yourrepository/raw/main/file14.pdf' },
            { name: 'File 15', url: 'https://github.com/yourusername/yourrepository/raw/main/file15.pdf' },
            { name: 'File 16', url: 'https://github.com/yourusername/yourrepository/raw/main/file16.pdf' },
            { name: 'File 17', url: 'https://github.com/yourusername/yourrepository/raw/main/file17.pdf' },
            { name: 'File 18', url: 'https://github.com/yourusername/yourrepository/raw/main/file18.pdf' },
            { name: 'File 19', url: 'https://github.com/yourusername/yourrepository/raw/main/file19.pdf' },
            { name: 'File 20', url: 'https://github.com/yourusername/yourrepository/raw/main/file20.pdf' },
            { name: 'File 21', url: 'https://github.com/yourusername/yourrepository/raw/main/file21.pdf' },
            { name: 'File 22', url: 'https://github.com/yourusername/yourrepository/raw/main/file22.pdf' },
            { name: 'File 23', url: 'https://github.com/yourusername/yourrepository/raw/main/file23.pdf' }
        ];

        const buttonsContainer = document.getElementById('buttons-container');

        pdfFiles.forEach(file => {
            const button = document.createElement('button');
            button.className = 'download-button';
            button.innerText = `Download ${file.name}`;
            button.addEventListener('click', function() {
                const link = document.createElement('a');
                link.href = file.url;
                link.download = `${file.name}.pdf`;
                document.body.appendChild(link);
                link.click();
                document.body.removeChild(link);
            });
            buttonsContainer.appendChild(button);
        });
   
