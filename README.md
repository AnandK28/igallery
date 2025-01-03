# Ex.08 Design of Interactive Image Gallery
## Date:
19/12/2024

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
  <title>My Image Gallery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f3f3f3;
      margin: 0;
      padding: 20px;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
    }

    .gallery-item {
      width: 150px;
      cursor: pointer;
      border: 1px solid #ccc;
      margin: 5px;
    }

    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
    }

    .modal-content {
      max-width: 90%;
      max-height: 90%;
    }

    .close {
      position: absolute;
      top: 10px;
      right: 20px;
      color: white;
      font-size: 24px;
    }
  </style>
  <script>
    function openModal(image) {
      var modal = document.getElementById('imageModal');
      var modalImg = document.getElementById('modalImage');
      
      modal.style.display = "flex";
      modalImg.src = image.src;
    }

    function closeModal() {
      var modal = document.getElementById('imageModal');
      modal.style.display = "none";
    }
  </script>
</head>
<body>
  <h1>My Image Gallery</h1>
  <div class="gallery">
    <img src="1.jpg" alt="Image 1" class="gallery-item" onclick="openModal(this)">
    <img src="2.jpg" alt="Image 2" class="gallery-item" onclick="openModal(this)">
    <img src="3.jpg" alt="Image 3" class="gallery-item" onclick="openModal(this)">
    <img src="4.jpg" alt="Image 4" class="gallery-item" onclick="openModal(this)">
    <img src="5.jpg" alt="Image 5" class="gallery-item" onclick="openModal(this)">
  </div>

  <!-- Modal -->
  <div id="imageModal" class="modal" onclick="closeModal()">
    <span class="close">&times;</span>
    <img class="modal-content" id="modalImage">
  </div>
</body>
</html>
```

## OUTPUT:
![alt text](<Screenshot 2024-12-19 084739.png>)
![alt text](<Screenshot 2024-12-19 084748.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
