# Denemetrayicisi
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Basit Tarayıcı</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
        input {
            padding: 10px;
            width: 80%;
            margin-bottom: 10px;
        }
        button {
            padding: 10px 20px;
        }
    </style>
</head>
<body>
    <h1>Basit Tarayıcı</h1>
    <input type="text" id="urlInput" placeholder="Bir URL girin..." />
    <button onclick="goToSite()">Git</button>
    <iframe id="siteFrame" style="width: 100%; height: 80%; border: none;"></iframe>

    <script>
        function goToSite() {
            var url = document.getElementById('urlInput').value;
            if (!url.startsWith('http://') && !url.startsWith('https://')) {
                url = 'http://' + url;
            }
            document.getElementById('siteFrame').src = url;
        }
    </script>
</body>
</html>
