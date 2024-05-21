<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Permintaan Maaf</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f8ff;
            margin: 0;
        }
        #container {
            background-color: #ffffff;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        h1 {
            color: #333333;
            margin-bottom: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 25px;
            transition: background-color 0.3s, transform 0.3s;
        }
        #yesBtn {
            background-color: #28a745;
            color: #ffffff;
        }
        #yesBtn:hover {
            background-color: #218838;
            transform: scale(1.1);
        }
        #noBtn {
            background-color: #dc3545;
            color: #ffffff;
            position: absolute;
        }
        #noBtn:hover {
            background-color: #c82333;
            transform: scale(1.1);
        }
    </style>
</head>
<body>

<div id="container">
    <h1>Tolong maafkan saya Mba Diana</h1>
    <button id="yesBtn">Iya</button>
    <button id="noBtn">Tidak</button>
</div>

<script>
    const noBtn = document.getElementById('noBtn');
    const container = document.getElementById('container');

    noBtn.addEventListener('mouseover', function() {
        const containerRect = container.getBoundingClientRect();
        const newX = Math.random() * (window.innerWidth - containerRect.width);
        const newY = Math.random() * (window.innerHeight - containerRect.height);
        
        noBtn.style.left = newX + 'px';
        noBtn.style.top = newY + 'px';
    });

    document.getElementById('yesBtn').addEventListener('click', function() {
        alert('Terima kasih telah memaafkan saya diana');
    });
</script>

</body>
</html>
