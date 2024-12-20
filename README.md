# Ex.08 Design of Interactive Image Gallery
# Date:28-10-2024
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GALLERY</title>
    <style>
        body {
            background-color: khaki;
            font-family: 'Open Sans', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }

        .header {
            text-align: center;
            color: palevioletred;
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
            font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        }

        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            padding: 20px;
            max-width: 1200px;
            width: 100%;
            animation: fadeIn 1s ease-in-out;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 8px 16px rgba(red, green, blue, alpha);
        }

        .gallery-item img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            transition: transform 0.3s ease, filter 0.3s ease;
        }

        .gallery-item img:hover {
            transform: scale(1.1);
            filter: brightness(0.8);
            cursor: pointer;
        }

        .caption {
            position: absolute;
            bottom: 8px;
            left: 8px;
            background-color: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 12px;
            text-align: center;
            width: calc(100% - 16px);
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 600px;
            border-radius: 10px;
        }

        .close {
            position: absolute;
            top: 10px;
            right: 20px;
            color: white;
            font-size: 30px;
            cursor: pointer;
        }

        .modal-description {
            color: white;
            text-align: center;
            padding: 10px;
            font-size: 16px;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .footer{
            font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
            color: black;
            align-items: end;
            font-size:large;

        }

    </style>
</head>
<body>
    

    <div class="header">INTERACTIVE IMAGE GALLERY</div>
    <h3 style="color: salmon; font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;">YUVASHREE R(24900809)</h3>
    <div class="gallery-container">
        <div class="gallery-item">
            <img src="gall1.jpg">
            <div class="caption">BEAUTY</div>
        </div>
        <div class="gallery-item">
            <img src="gal2.webp">
            <div class="caption">NATURE</div>
        </div>
        <div class="gallery-item">
            <img src="gal3.jpg">
            <div class="caption">LISTENING</div>
        </div>
        <div class="gallery-item">
            <img src="gal1.jpg">
            <div class="caption">SAVE TREES</div>
        </div>
        <div class="gallery-item">
            <img src="gal4.avif" >
            <div class="caption">SUNSET</div>
        </div>
    </div>

    <div class="modal" id="modal">
        <span class="close" id="close">&times;</span>
        <img class="modal-content" id="modal-img">
        <div class="modal-description" id="modal-description"></div>
    </div>

    <script>
        const images = document.querySelectorAll('.gallery-item img');
        const modal = document.getElementById('modal');
        const modalImg = document.getElementById('modal-img');
        const modalDescription = document.getElementById('modal-description');
        const closeBtn = document.getElementById('close');

        images.forEach((image) => {
            image.addEventListener('click', () => {
                modal.style.display = 'flex';
                modalImg.src = image.src;
                modalDescription.textContent = image.getAttribute('data-description');
            });
        });

        closeBtn.addEventListener('click', () => {
            modal.style.display = 'none';
        });
    </script>
    <footer>
        <div class="footer">
        <p>Designed and developed by YUVASHREE R</p>
    </div>
    </footer>

</body>
</html>

```
# OUTPUT:
![Screenshot (40)](https://github.com/user-attachments/assets/2b357c71-f85e-476f-bf90-613ad6d4dd4a)
![Screenshot (41)](https://github.com/user-attachments/assets/665907e4-4a0b-4930-b0cc-8666ba98b22d)
![Screenshot (42)](https://github.com/user-attachments/assets/9c842b34-daaa-41b0-8032-e20d869d6ac2)
![Screenshot (43)](https://github.com/user-attachments/assets/cd9bc069-5472-4924-a855-3fcd041b7879)
![Screenshot (44)](https://github.com/user-attachments/assets/56b3465b-49a6-4d43-b82b-24106af67479)
![Screenshot (45)](https://github.com/user-attachments/assets/f9c39d6d-23bc-4c3e-8e41-2a79435b0018)








# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
