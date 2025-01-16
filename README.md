<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titik Kumpul Wong Mumet Karo Wong Ruwet</title>
    <style>
        body {
            font-family: 'Times New Roman', Times, serif, sans-serif;
            margin: 0;
            padding: 0;
        }

        nav {
            background-color: #6e0202;
            color: white(255, 255, 253);
            padding: 1rem;
            display: flex;
            justify-content: space-around;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 1.2rem;
        }

        nav a:hover {
            text-decoration: underline;
        }

        .content {
            display: none;
            padding: 2rem;
            text-align: center;
        }

        .content.active {
            display: block;
        }

        .home-content {
            background-color: white;
        }

        .about-content {
            background-color: white;
        }

        .contact-content {
            background-color: white;
        }
    </style>
</head>
<body>
    <nav>
        <a href="#" id="home-link">Motto</a>
        <a href="#" id="about-link">Bidang</a>
        <a href="#" id="contact-link">Keluhanmu</a>
    </nav>

    <div id="home-content" class="content home-content">
        <h1>Selamat datang di ruang konsultasi wong ruwet</h1>
        <p>Kami melayani keluh kesah wong mumet bagaimanapun bentuknya. Meskipun itu adalah ruwet yang di luar nurul sekalipun.</p>
    </div>

    <div id="about-content" class="content about-content">
        <h1>Melayani dengan Setulus Hati</h1>
        <p> 1. Wong Pedhot
            2. Wong bar Rungkad
            3. Lose Streak ML
            4. Virus wibu
            5. Virus Plastik
            6. Fans Emyu
        </p>
    </div>

    <div id="contact-content" class="content contact-content active">
        <h1>Contact Us</h1>
        <p>Get in touch with us via this page. Fill out the form below to reach out:</p>
        <form>
            <label for="Nama">Nama:</label><br>
            <input type="Nama" id="Nama" name="Nama" placeholder="Namalu nyett" required><br><br>

            <label for="Nomor">Nomor:</label><br>
            <input type="Nomor" id="Nomor" name="Nomor" placeholder="Nomor Nyetttt" required><br><br>

            <label for="Keluhanmu">Keluhanmu:</label><br>
            <textarea id="Keluhanmu" name="Keluhanmu" placeholder="Your Message" rows="5" required></textarea><br><br>

            <button type="Tombol Kirim">Kirim</button>
        </form>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            const links = document.querySelectorAll('nav a');
            const contents = document.querySelectorAll('.content');

            links.forEach(link => {
                link.addEventListener('click', function (e) {
                    e.preventDefault();

                    // Remove active class from all contents
                    contents.forEach(content => content.classList.remove('active'));

                    // Add active class to the corresponding content
                    const id = link.id.split('-')[0] + '-content';
                    document.getElementById(id).classList.add('active');
                });
            });
        });
    </script>
</body>
</html>
