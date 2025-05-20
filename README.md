# Project Responsive Web Design using Bootstrap
# Date:20-05-25
# reg : 212224040055
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sports Shop</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: 'Pacifico', cursive;
            margin: 0;
            padding: 0;
            background-color: #e3f2fd;
            color: #2c3e50;
        }

        .navbar {
            background-color: #0d47a1;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }

        .navbar-brand, .navbar-nav .nav-link {
            color: #ffffff !important;
        }

        .navbar-nav {
            flex-direction: row;
        }

        .navbar-nav .nav-link {
            padding: 0 15px;
        }

        .nav-item .btn-primary {
            background-color: #ff6f00;
            border-color: #ff6f00;
        }

        .nav-item .btn-primary:hover {
            background-color: #e65100;
            border-color: #e65100;
        }

        .header-section h3 {
            font-weight: bold;
            color: #0d47a1;
        }

        .header-section p {
            font-size: 1.2em;
            color: #37474f;
        }

        .gallery-section {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .card {
            background-color: #ffffff;
            border: 1px solid #cfd8dc;
            border-radius: 10px;
            box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.15);
        }

        .gallery-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px 10px 0 0;
        }

        .card-title {
            font-weight: bold;
            font-size: 1.1rem;
            color: #0d47a1;
            text-align: center;
            margin-top: 15px;
        }

        .card-body {
            padding: 20px;
            text-align: center;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        footer {
            background-color: #0d47a1;
            color: #ffffff;
            text-align: center;
            padding: 25px;
            font-size: 0.9em;
            margin-top: 40px;
            box-shadow: 0px -2px 5px rgba(0, 0, 0, 0.1);
        }

        @media (max-width: 768px) {
            .navbar-nav {
                flex-direction: column;
                text-align: center;
                padding: 10px 0;
            }

            .gallery-section {
                margin-top: 20px;
            }

            .card-body {
                padding: 10px;
            }
        }

        @media (max-width: 480px) {
            .header-section h3 {
                font-size: 1.5em;
            }

            .header-section p {
                font-size: 1em;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark">
        <a class="navbar-brand" href="#">Sports Shop</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ml-auto">
                <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Products</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Offers</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
                <li class="nav-item"><a class="btn btn-primary" href="#">Sign Up</a></li>
            </ul>
        </div>
    </nav>

    <div class="container mt-4">
        <div class="text-center mb-4 header-section">
            <h4>Sports Galore</h4>
            <h3>"Gear Up for Your Next Adventure!"</h3>
            <p class="lead">"Discover Top Quality Sports Equipment and Apparel"</p>
        </div>

        <div class="gallery-section">
            <div class="card">
                <img src="football.jpeg" class="gallery-img" alt="Football">
                <div class="card-body">
                    <p class="card-title">FOOTBALL</p>
                    <small class="text-muted">Adidas</small>
                </div>
            </div>
            <div class="card">
                <img src="basketball.jpeg" class="gallery-img" alt="Basketball">
                <div class="card-body">
                    <p class="card-title">BASKETBALL</p>
                    <small class="text-muted">Nike</small>
                </div>
            </div>
            <div class="card">
                <img src="running.jpeg" class="gallery-img" alt="Running Shoes">
                <div class="card-body">
                    <p class="card-title">RUNNING SHOES</p>
                    <small class="text-muted">Asics</small>
                </div>
            </div>
            <div class="card">
                <img src="bat.jpeg" class="gallery-img" alt="Cricket Bat">
                <div class="card-body">
                    <p class="card-title">CRICKET BAT</p>
                    <small class="text-muted">SG</small>
                </div>
            </div>
            <div class="card">
                <img src="tennis.avif" class="gallery-img" alt="Tennis Racket">
                <div class="card-body">
                    <p class="card-title">TENNIS RACKET</p>
                    <small class="text-muted">Wilson</small>
                </div>
            </div>
            <div class="card">
                <img src="cycling.webp" class="gallery-img" alt="Cycling Helmet">
                <div class="card-body">
                    <p class="card-title">CYCLING HELMET</p>
                    <small class="text-muted">Giro</small>
                </div>
            </div>
            <div class="card">
                <img src="golf.jpg" class="gallery-img" alt="Golf Clubs">
                <div class="card-body">
                    <p class="card-title">GOLF CLUBS</p>
                    <small class="text-muted">Callaway</small>
                </div>
            </div>
            <div class="card">
                <img src="swimming.jpeg" class="gallery-img" alt="Swimming Gear">
                <div class="card-body">
                    <p class="card-title">SWIMMING GEAR</p>
                    <small class="text-muted">Speedo</small>
                </div>
            </div>
        </div>
    </div>
    <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
# OUTPUT:
![Screenshot 2025-05-20 113617](https://github.com/user-attachments/assets/67a1d399-93fc-442b-8df7-ee645ac79047)

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
