<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background-image: url('anhnen3.png');
      background-size: contain;
      background-repeat: no-repeat;
      background-position: top center;
      background-color: black;
      min-height: 100vh;
      display: flex;
      justify-content: flex-end;
      align-items: center;
    }

   .menu-vertical {
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin-right: 400px;
  margin-top: 300px; /* Thêm dòng này */
  background-color: transparent;
  padding: 20px;
  border-radius: 10px;
}


    .menu-vertical button {
      padding: 10px 20px;
      font-size: 1rem;
      background-color: #FFD700;
      color: black;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: transform 0.2s;
    }

    .menu-vertical button:hover {
      transform: scale(1.05);
      background-color: #ffe45e;
    }

    .content {
      display: none;
      background: rgba(0, 0, 0, 0.6);
      padding: 20px;
      border-radius: 10px;
      max-width: 90%;
      margin: 10px auto;
      color: white;
    }

    @media (max-width: 768px) {
      body {
        flex-direction: column;
        justify-content: flex-start;
        background-size: cover;
      }

      .menu-vertical {
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        margin: 20px 0;
      }

      .menu-vertical button {
        width: 45%;
        margin: 5px;
      }
    }
  </style>
</head>
<body>
  <div class="menu-vertical">
    <button onclick="moQuyen1()"> Quyển 1</button>
    <button onclick="showContent('gioithieu2')"> Quyển 2</button>
    <button onclick="showContent('gioithieu3')"> Quyển 3</button>
    <button onclick="showContent('gioithieu4')"> Quyển 4</button>
    <button onclick="showContent('gioithieu5')"> Quyển 5</button>
  </div>

  <div id="gioithieu2" class="content">Nội dung Quyển 2...</div>
  <div id="gioithieu3" class="content">Nội dung Quyển 3...</div>
  <div id="gioithieu4" class="content">Nội dung Quyển 4...</div>
  <div id="gioithieu5" class="content">Nội dung Quyển 5...</div>

  <script>
    function moQuyen1() {
      window.open('https://drive.google.com/file/d/1Xxh3G-BFcPzr-l15TbTPEsN8R4y0GxcC/view?usp=drive_link', '_blank');
    }

    function showContent(id) {
      const contents = document.querySelectorAll('.content');
      contents.forEach(c => c.style.display = 'none');
      document.getElementById(id).style.display = 'block';
    }
  </script>
</body>
</html>
