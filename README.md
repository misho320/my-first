# my-first
<!DOCTYPE html>
<html lang="ka">
<head>
    <meta charset="UTF-8">
    <title>SocMediaManagerMisho</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f0f0f0; text-align: center; padding: 50px; }
        h1 { color: #333; }
        p { color: #555; font-size: 18px; }
        .button { padding: 10px 20px; font-size: 16px; cursor: pointer; background-color: #4CAF50; color: white; border: none; border-radius: 5px; margin: 5px; }
        .button:hover { background-color: #45a049; }
        .social-buttons a { text-decoration: none; margin: 0 10px; font-size: 20px; }
        .slider { max-width: 600px; margin: 20px auto; position: relative; }
        .slides img { width: 100%; display: none; border-radius: 10px; }
        .slides img.active { display: block; }
    </style>
</head>
<body>

    <h1>გამარჯობა! მე მიშო ვარ - თქვენი Social Media Manager</h1>
    <p>ეს ჩემი უფასო საიტია, პირდაპირ ბრაუზერში!</p>

    <button class="button" onclick="alert('მოგესალმებით SocMediaManagerMisho.ge-ზე!')">დაწკაპე აქ</button>

    <!-- სოციალური მედია ღილაკები -->
    <div class="social-buttons">
        <a href="https://www.facebook.com/" target="_blank">Facebook</a>
        <a href="https://www.instagram.com/" target="_blank">Instagram</a>
        <a href="https://www.twitter.com/" target="_blank">Twitter</a>
    </div>

    <!-- სლაიდერი -->
    <div class="slider">
        <div class="slides">
            <img src="https://via.placeholder.com/600x300?text=Slide+1" class="active">
            <img src="https://via.placeholder.com/600x300?text=Slide+2">
            <img src="https://via.placeholder.com/600x300?text=Slide+3">
        </div>
    </div>

    <script>
        // სლაიდერის ფუნქცია
        let current = 0;
        const slides = document.querySelectorAll('.slides img');

        function showSlide(index){
            slides.forEach((slide, i) => {
                slide.classList.toggle('active', i === index);
            });
        }

        setInterval(() => {
            current = (current + 1) % slides.length;
            showSlide(current);
        }, 3000);
    </script>

</body>
</html>
