# day1
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For You</title>

    <style>

        body{
            margin:0;
            height:100vh;
            display:flex;
            justify-content:center;
            align-items:center;
            background:linear-gradient(120deg,#1f1c2c,#928dab);
            font-family:"Segoe UI",sans-serif;
        }

        .card{
            width:90%;
            max-width:600px;
            background:rgba(255,255,255,0.08);
            backdrop-filter:blur(12px);
            border-radius:20px;
            padding:50px 40px;
            color:white;
            box-shadow:0 25px 40px rgba(0,0,0,0.4);
        }

        h1{
            font-weight:500;
            letter-spacing:1px;
            margin-bottom:25px;
        }

        p{
            font-size:18px;
            line-height:1.8;
            opacity:0.9;
        }

        .line{
            width:60px;
            height:3px;
            background:#ff8fa3;
            margin:25px 0;
            border-radius:5px;
        }

        button{
            margin-top:40px;
            background:none;
            border:1px solid rgba(255,255,255,0.4);
            color:white;
            padding:12px 30px;
            border-radius:25px;
            font-size:15px;
            cursor:pointer;
            transition:0.3s;
        }

        button:hover{
            background:rgba(255,255,255,0.15);
        }

        .page{
            display:none;
        }

        .active{
            display:block;
        }

        footer{
            margin-top:30px;
            font-size:13px;
            opacity:0.6;
        }

    </style>
</head>

<body>

<div class="card">

    <!-- PAGE 1 -->
    <div class="page active">
        <h1>Hi,</h1>
        <div class="line"></div>
        <p>
            Ini bukan website besar.<br>
            Bukan juga sesuatu yang berlebihan.<br><br>
            Cuma cara sederhana untuk bilang:<br>
            Aku menghargai kehadiranmu.
        </p>
    </div>

    <!-- PAGE 2 -->
    <div class="page">
        <h1>Tentang Kamu</h1>
        <div class="line"></div>
        <p>
            Kamu punya cara sendiri<br>
            untuk membuat suasana terasa lebih tenang.<br><br>
            Tanpa banyak usaha.<br>
            Tanpa banyak kata.
        </p>
    </div>

    <!-- PAGE 3 -->
    <div class="page">
        <h1>Sejujurnya</h1>
        <div class="line"></div>
        <p>
            Aku menikmati setiap percakapan kecil kita.<br>
            Hal-hal sederhana.<br>
            Hal-hal biasa.<br><br>
            Tapi entah kenapa selalu terasa berarti.
        </p>
    </div>

    <!-- PAGE 4 -->
    <div class="page">
        <h1>Tidak Terburu-buru</h1>
        <div class="line"></div>
        <p>
            Aku tidak ingin memaksa apapun.<br>
            Tidak ingin mendahului waktu.<br><br>
            Kalau suatu hari<br>
            kita berjalan lebih dekat,<br>
            semoga itu karena rasa yang sama.
        </p>
    </div>

    <!-- PAGE 5 -->
    <div class="page">
        <h1>Hari Ini</h1>
        <div class="line"></div>
        <p>
            Di hari Valentine ini,<br>
            aku cuma ingin kamu tahu:<br><br>
            Kamu seseorang yang istimewa<br>
            dalam caraku sendiri.
        </p>
    </div>

    <!-- PAGE 6 -->
    <div class="page">
        <h1>Terima Kasih</h1>
        <div class="line"></div>
        <p>
            Terima kasih sudah hadir.<br>
            Terima kasih sudah menjadi dirimu sendiri.<br><br>
            Semoga kita selalu baik.<br>
            Apapun bentuk ceritanya nanti.
        </p>
    </div>

    <button onclick="next()">Next</button>

    <footer>
        Written sincerely
    </footer>

</div>


<script>

    let page = 0;
    const pages = document.querySelectorAll(".page");

    function next(){

        pages[page].classList.remove("active");
        page++;

        if(page >= pages.length){
            page = 0;
        }

        pages[page].classList.add("active");
    }

</script>

</body>
</html>
