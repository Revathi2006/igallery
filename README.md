# Ex.05 Design of Interactive Image Gallery
## Date:7.05.2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Image Gallery</title>
  <style>
    body {
      margin: 0;
      padding: 30px;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, pink, orange);
      text-align: center;
    }

    h1 {
      color: #143D60;
      margin-bottom: 20px;
      font-size: 2.5rem;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      max-width: 1200px;
      margin: auto;
    }

    .gallery img {
      width: 100%;
      height: 220px;
      object-fit: cover;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }

    .gallery img:hover {
      transform: scale(1.05);
      box-shadow: 0 12px 25px rgba(0, 0, 0, 0.3);
    }

    .lightbox {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.85);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    .lightbox img {
      max-width: 90%;
      max-height: 80%;
      border-radius: 10px;
      box-shadow: 0 0 30px #000;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .footer {
      margin-top: 40px;
      color: #27667B;
      font-weight: bold;
      font-size: 1.1rem;
    }
  </style>
</head>
<body>

  <h1>Interactive Image Gallery </h1>
  <br>
  <br>

  <div class="gallery">
    <img src="download.jpg" alt="Image 1">
    
    <img src="cat 2.jpg" alt="Image 2">
    <img src="cat 3.jpg" alt="Image 3">
    
    <img src="dog 1.jpg" alt="Image 4">
    <img src="dog 2.webp" alt="Image 5">
    <img src="dog 3.webp" alt="Image 6">
    <img src="bird1.jpg" alt="Image 7">
    <img src="bird 2.jpg" alt="Image 8">

  </div>

  <div class="lightbox" id="lightbox">
    <img id="lightbox-img" src="" alt="Full View">
  </div>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
  <hr>
  <div class="footer">
    Name: Revathi.S <br>
    <br>
    Register No: 212224230228
  </div>

  <script>
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    const galleryImgs = document.querySelectorAll('.gallery img');

    galleryImgs.forEach(img => {
      img.addEventListener('click', () => {
        lightboxImg.src = img.src;
        lightbox.style.display = 'flex';
      });
    });

    lightbox.addEventListener('click', () => {
      lightbox.style.display = 'none';
    });
  </script>

</body>
</html>
```

## OUTPUT:


![alt text](<revathi/galleryapp/static/Screenshot (71).png>)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
