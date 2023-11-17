<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phòng chứa bệnh nhân</title>
    <link rel="shortcut icon" href="https://github.com/hafong26/gallery/blob/main/images/avt-zalo-512x512.png?raw=true"
        type="image/x-icon">
    <link rel="stylesheet" href='https://unpkg.com/boxicons@2.0.9/css/boxicons.min.css'>
    <link href="https://fonts.googleapis.com/css2?family=Bungee+Inline&display=swap" rel="stylesheet">
    <style>
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
            font-family: 'Bungee Inline';
        }

        body {
            position: relative;
            overflow: hidden;
            user-select: none;
        }

        body.dark {
            filter: invert(100%)
        }

        .container {
            background-color: #fff;
            color: #000;
            height: 100vh;

        }

        .eye {
            position: absolute;
            bottom: 1em;
            right: 1em;
            border-radius: 50%;
            padding: .5em;
            font-size: 30px;
            background: #000;
            color: #fff;
            border: medium solid #fff;
        }

        .eye:active {
            cursor: pointer;
        }
    </style>
</head>

<body class="dark">
    <div class="container"></div>
    <div class="eye" onclick="document.body.classList.toggle('dark')">
        <i class='bx bxs-show'></i>
    </div>
    <script>
        const text = [
            'Nhấp vào biểu tượng "con mắt" để bật Dark Mode',
            'Tải lại trang để thay đổi tốc độ chạy của chữ'
        ]
        const loadMatrix = (n) => {
            for (i = 0; i < n; i++) {
                let el = document.createElement('marquee')
                el.textContent = text[i % text.length]
                let random = Math.floor(Math.random() * 100 + 1)
                el.setAttribute('scrollamount', random)
                document.querySelector('.container').append(el)
            }
        }
        loadMatrix(30)
    </script>


</body>

</html>
