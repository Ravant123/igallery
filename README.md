# Ex.08 Design of Interactive Image Gallery
## Date:11-12-2024

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
    <title>Interactive Photo Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: #9d4877d8;
        }

        h1 {
            margin: 20px 0;
            color: #333;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            max-width: 1200px;
        }

        .gallery img {
            width: 180px;
            height: 120px;
            object-fit: cover;
            cursor: pointer;
            border: 3px solid transparent;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s, border-color 0.3s, box-shadow 0.3s;
        }

        .gallery img:hover, .gallery img:active {
            transform: scale(1.2);
            border-color: #007BFF;
            box-shadow: 0 8px 16px rgba(0, 123, 255, 0.4);
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .modal img {
            width: 90%;
            height: auto;
            max-width: 1000px;
            max-height: 80%;
            border-radius: 8px;
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.7);
            transition: transform 0.3s ease-in-out;
        }

        .modal img:hover {
            transform: scale(1.05);
        }

        .modal .close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 32px;
            color: white;
            cursor: pointer;
            transition: color 0.3s;
        }

        .modal .close:hover {
            color: #ff4757;
        }

        .modal .caption {
            color: white;
            margin-top: 20px;
            font-size: 18px;
            text-align: center;
            max-width: 80%;
        }

        footer {
            margin-top: 30px;
            padding: 20px;
            background-color: #333;
            color: white;
            text-align: center;
            width: 100%;
        }

        footer a {
            color: #007BFF;
            text-decoration: none;
            transition: color 0.3s;
        }

        footer a:hover {
            color: #ff4757;
        }
    </style>
</head>
<body>
    <h1>Interactive Photo Gallery</h1>
    <div class="gallery">
        <img src="1.webp" alt="Photo 1" data-caption="JESUS">
        <img src="2.webp" alt="Photo 2" data-caption="Prince of Peace">
        <img src="3.webp" alt="Photo 3" data-caption="Lamb of God">
        <img src="4.webp" alt="Photo 4" data-caption="Messiah ">
        <img src="5.webp" alt="Photo 5" data-caption="son of god">
    </div>

    <div class="modal" id="photoModal">
        <span class="close" id="closeModal">&times;</span>
        <img src="" alt="" id="modalImg">
        <div class="caption" id="modalCaption"></div>
    </div>

    <footer>
        <p>&copy; 2024 Interactive Photo Gallery. Designed with ❤️ by <a href="#">S.Ravant Vignesh</a>.</p>
    </footer>

    <script>
        // Select elements
        const gallery = document.querySelector('.gallery');
        const modal = document.getElementById('photoModal');
        const modalImg = document.getElementById('modalImg');
        const modalCaption = document.getElementById('modalCaption');
        const closeModal = document.getElementById('closeModal');

        // Open modal on photo click
        gallery.addEventListener('click', (e) => {
            if (e.target.tagName === 'IMG') {
                modal.style.display = 'flex';
                modalImg.src = e.target.src;
                modalCaption.textContent = e.target.getAttribute('data-caption');
            }
        });

        // Close modal on close button click
        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        // Close modal on outside click
        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                modal.style.display = 'none';
            }
        });
    </script>
</body>
</html>


```
## OUTPUT:
![alt text](<Screenshot (73).png>)
![alt text](<Screenshot (74).png>)
![alt text](<Screenshot (75).png>)
![alt text](<Screenshot (76).png>)
![alt text](<Screenshot (77).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
