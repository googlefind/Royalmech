<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Search</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f5f5f5;
        }

        .logo {
            margin-bottom: 20px;
        }

        input[type="text"] {
            padding: 10px;
            width: 50%;
            max-width: 400px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 20px;
            margin-bottom: 20px;
        }

        input[type="submit"] {
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            background-color: #4285F4;
            color: white;
            border-radius: 20px;
            cursor: pointer;
        }

        input[type="submit"]:hover {
            background-color: #357AE8;
        }
    </style>
</head>
<body>

    <!-- Google Logo -->
    <div class="logo">
        <img src="https://www.google.com/images/branding/googlelogo/2x/google-logo-light_color_92x30dp.png" alt="Google Logo">
    </div>

    <!-- Search Box -->
    <form action="https://www.google.com/search" method="get">
        <input type="text" name="q" placeholder="Search Google or type a URL" required>
        <br>
        <input type="submit" value="Google Search">
    </form>

</body>
</html>
