<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Document</title>
<style>
    body {
        position: relative;
        width: 563px;
        height: 860px;
        margin: 0 auto;
    }
    
    .background {
        position: absolute;
        width: 100%;
        height: 100%;
        background-image: url('background poem img.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        display: none; /* Hide the background initially */
    }
    
    .poem-text {
        display: none; /* Hide the poem initially */
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        max-width: 80%;
        padding: 40px;
        font-size: 14px; /* Adjust the font size as needed */
        text-align: center;
        font-family: 'Poiret One', sans-serif; /* Change font family */
        font-weight: bold; /* Make the text bold */
    }

    .envelope-img {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        max-width: 80%;
        background-color: white; /* Plain white background */
    }

    /* Hide the background image only for the envelope */
    .envelope-img::before {
        content: "";
        position: absolute;
        width: 100%;
        height: 100%;
        background-image: none; /* Hide the background image */
    }

    .for-you-text {
        position: absolute;
        top: calc(50% - 220px); /* Adjust the position */
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
        font-size: 24px;
        font-weight: bold;
    }

    .next-button {
        position: absolute;
        top: calc(50% + 120px); /* Adjust the position */
        left: 50%;
        transform: translateX(-50%);
        font-size: 16px;
        background-color: purple; /* Change the button color to purple */
        color: white;
        border: none;
        border-radius: 5px;
        padding: 10px 20px;
        cursor: pointer;
    }
</style>
<link href="https://fonts.googleapis.com/css2?family=Poiret+One&display=swap" rel="stylesheet">
</head>
<body>
    <div class="background"></div>
    <div class="for-you-text">For You</div>
    <img class="envelope-img" src="envelope.gif" alt="Envelope GIF">
    <button class="next-button" onclick="showPoem()">Open</button>
    <div class="poem-text">
        <p>Hints, dance in the moon's soft glow.</p>
        <p>Amidst whispers of wishes, we'll sow.</p>
        <p>Painting dreams with stars in the night sky.</p>
        <p>Playing melodies as time rushes by.</p>
        <p>Yearning for laughter, let's seize the day.</p>
        <p>Boundless joy in each moment we sway.</p>
        <p>In the embrace of dawn's golden hue.</p>
        <p>Radiant smiles, our friendship anew.</p>
        <p>Tender memories, like petals in the wind.</p>
        <p>Hearts intertwined, in harmony we've pinned.</p>
        <p>Daybreak whispers secrets of the divine.</p>
        <p>A symphony of love in every line.</p>
        <p>You, the essence of grace and light.</p>
        <p>Cherished friend, in the darkest night.</p>
        <p>Here's to endless adventures, bold and true.</p>
        <p>In every step, I'll be there for you.</p>
        <p>Now, as another year begins to shine.</p>
        <p>Eternal wishes, dear Chine, are thine.</p>
    </div>

    <script>
        function showPoem() {
            var background = document.querySelector(".background");
            var poemText = document.querySelector(".poem-text");
            var envelopeImg = document.querySelector(".envelope-img");
            var forYouText = document.querySelector(".for-you-text");
            var nextButton = document.querySelector(".next-button");
            
            background.style.display = "block"; // Show the background
            poemText.style.display = "block"; // Show the poem
            envelopeImg.style.display = "none"; // Hide the envelope GIF
            forYouText.style.display = "none"; // Hide the "For You" text
            nextButton.style.display = "none"; // Hide the "Next" button
        }
    </script>
</body>
</html>
