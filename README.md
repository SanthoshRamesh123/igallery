# Ex.08 Design of Interactive Image Gallery
## Date:27/05/2025

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
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="gallery.css">
</head>
<body>
    <div class="gallery-container">
        <div class="gallery-item">
            <img src="image 1.avif" alt="Image 1">
        </div>
        <div class="gallery-item">
            <img src="image 2.jpg" alt="Image 2">
        </div>
        <div class="gallery-item">
            <img src="image 3.jpg" alt="Image 3">
        </div>
        <div class="gallery-item">
            <img src="" alt="Image 4">
        </div>
        <div class="gallery-item">
            <img src="image 4.jpg" alt="Image 4">
        </div>
    </div>

    <div class="modal" id="modal">
        <span class="close" id="close">&times;</span>
        <img class="modal-content" id="modal-img">
    </div>

    <script src="gallery.js"></script>
</body>
</html>
 
 gallery.css
 style.css

body {
    background-color: gray;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #e3e0e0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
}

.gallery-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 10px;
    padding: 20px;
    max-width: 1200px;
    width: 100%;
}

.gallery-item img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(255, 255, 255, 0.1);
    transition: transform 0.3s ease;
}

.gallery-item img:hover {
    transform: scale(1.30);
    cursor: pointer;
}

.modal {
    display: none;
    position: fixed;
    z-index: 1;
    padding-top: 100px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.7);
}

.modal-content {
    margin: auto;
    display: block;
    width: 80%;
    max-width: 700px;
    border-radius: 10px;
}

.close {
    position: absolute;
    top: 10px;
    right: 25px;
    color: #ffffff;
    font-size: 36px;
    font-weight: bold;
    cursor: pointer;
}

.close:hover,
.close:focus {
    color: #ffffff;
    text-decoration: none;
    cursor: pointer;
}
gallery.js
const images = document.querySelectorAll('.gallery-item img');
const modal = document.getElementById('modal');
const modalImg = document.getElementById('modal-img');
const closeBtn = document.getElementById('close');

images.forEach((image) => {
    image.addEventListener('click', () => {
        modal.style.display = 'block';
        modalImg.src = image.src; 
    });
});

closeBtn.addEventListener('click', () => {
    modal.style.display = 'none';
});
```
## OUTPUT:
![alt text](<Screenshot 2025-05-27 095740-1.png>)
![alt text](<Screenshot 2025-05-27 095753.png>)
![alt text](<Screenshot 2025-05-27 095803.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
