# Project Responsive Web Design using Bootstrap
# Date:20-05-2025
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
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Unleash Your Creative Genius</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" />
  <style>
    /* Reset body and base font */
    body {
      margin: 0;
      background: #003146; /* Deep teal gradient background */
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: #e8e8e8;
    }

    /* Navbar styling */
    nav.navbar {
      background-color: #0a1e2c; /* Very dark navy */
      padding: 0.75rem 2rem;
    }
    nav.navbar .navbar-brand {
      display: flex;
      align-items: center;
      font-weight: 700;
      font-size: 1.25rem;
      color: white;
      gap: 0.5rem;
      text-transform: uppercase;
      letter-spacing: 1.2px;
    }
    nav.navbar .navbar-brand img {
      height: 28px;
      width: 28px;
      border-radius: 50%;
      background-color: #1abc9c; /* Teal circle */
      padding: 4px;
    }
    nav.navbar .ms-auto button {
      font-weight: 600;
      font-size: 1rem;
      border-radius: 6px;
      padding: 6px 18px;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    nav.navbar .ms-auto .btn-outline-light {
      color: white;
      background: transparent;
      border: 1.8px solid white;
      margin-right: 10px;
    }
    nav.navbar .ms-auto .btn-outline-light:hover {
      background-color: #1abc9c;
      border-color: #1abc9c;
      color: #003146;
    }
    nav.navbar .ms-auto .btn-light {
      background-color: #f6f1e7;
      color: #003146;
      font-weight: 700;
    }
    nav.navbar .ms-auto .btn-light:hover {
      background-color: #d3c9b8;
      color: #003146;
    }

    header {
      text-align: center;
      padding: 4rem 1rem 3rem 1rem;
      color: white;
      max-width: 680px;
      margin: 0 auto 2rem auto;
    }
    header h1 {
      font-weight: 800;
      font-size: 3rem;
      letter-spacing: 0.8px;
      margin-bottom: 0.5rem;
    }
    header p {
      font-size: 1.15rem;
      font-weight: 400;
      color: #d3d3d3;
      line-height: 1.4;
    }

    .search-bar {
      max-width: 500px;
      margin: 1.5rem auto 4rem;
      display: flex;
      border-radius: 40px;
      overflow: hidden;
      box-shadow: 0 4px 20px rgba(0,0,0,0.5);
      background-color: #152a3a;
    }
    .search-bar input {
      border: none;
      padding: 12px 20px;
      flex: 1;
      font-size: 1rem;
      outline: none;
      background-color: transparent;
      color: #e0e0e0;
    }
    .search-bar input::placeholder {
      color: #9bb4c0;
    }
    .search-bar button {
      background-color: #1abc9c;
      border: none;
      padding: 0 28px;
      color: white;
      font-weight: 700;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .search-bar button:hover {
      background-color: #15987f;
    }

    /* Projects Section */
    .projects-section {
      max-width: 1140px;
      margin: 0 auto 6rem;
      padding: 0 1rem;
      color: white;
    }
    .projects-section h3 {
      text-align: center;
      font-weight: 700;
      font-size: 2.25rem;
      margin-bottom: 2.5rem;
      color: #d9f2ef;
      letter-spacing: 1.1px;
    }
    .project-card {
      border-radius: 12px;
      background-color: #0a1e2c;
      box-shadow: 0 8px 16px rgba(0,0,0,0.45);
      cursor: pointer;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      overflow: hidden;
    }
    .project-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 20px 32px rgba(26, 188, 156, 0.5);
    }
    .project-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-bottom: 4px solid #1abc9c;
      transition: filter 0.3s ease;
    }
    .project-card:hover img {
      filter: brightness(0.85);
    }
    .project-info {
      padding: 1rem 1.25rem;
    }
    .project-info h5 {
      font-weight: 700;
      margin-bottom: 0.5rem;
      color: #1abc9c;
      font-size: 1.1rem;
    }
    .project-info p {
      font-size: 0.9rem;
      color: #a7c8ca;
      margin: 0;
      line-height: 1.3;
    }

    /* Footer */
    footer {
      background-color: #0a1e2c;
      color: #9bb4c0;
      padding: 2rem 1rem;
      text-align: center;
      font-size: 1rem;
      border-top: 3px solid #1abc9c;
      margin-top: 4rem;
      font-weight: 500;
    }
    footer h4 {
      color: #1abc9c;
      font-weight: 700;
      margin-bottom: 0.5rem;
    }
    footer p {
      margin: 0.2rem 0;
      font-style: italic;
      font-weight: 400;
    }
  </style>
</head>
<body>

<nav class="navbar navbar-expand-lg">
  <a class="navbar-brand" href="#">
    <img src="srivatsan_logo.png" alt="Srivatsan Logo" />
    Dribbble
  </a>
  <div class="ms-auto">
    <button class="btn btn-outline-light me-2" data-bs-toggle="modal" data-bs-target="#loginModal">Login</button>
    <button class="btn btn-light" data-bs-toggle="modal" data-bs-target="#signupModal">Sign Up</button>
  </div>
</nav>

<header>
  <h1>Unleash Your Creative Genius</h1>
  <p>Showcasing visionary designers and their cutting-edge projects from around the world. Find your next inspiration here.</p>
  <div class="search-bar">
    <input type="search" placeholder="Search designs, projects, or designers..." aria-label="Search projects" />
    <button>Go</button>
  </div>
</header>

<section class="projects-section">
  <h3>Featured Creations</h3>
  <div class="row g-4">
    <div class="col-md-4">
      <div class="project-card">
        <img src="1.w.png" alt="Abstract Waves" />
        <div class="project-info">
          <h5>Abstract Waves</h5>
          <p>Dynamic waveforms inspired by nature and movement.</p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="project-card">
        <img src="2.w.png" alt="Modern Typography" />
        <div class="project-info">
          <h5>Modern Typography</h5>
          <p>A fresh take on classic typography with geometric balance.</p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="project-card">
        <img src="3.w.jpg" alt="Pixel Artscape" />
        <div class="project-info">
          <h5>Pixel Artscape</h5>
          <p>Colorful pixel art landscapes blending retro with modern.</p>
        </div>
      </div>
    </div>
  </div>
  <div class="row g-4 mt-3">
    <div class="col-md-4">
      <div class="project-card">
        <img src="4.w.jpg" alt="Neo Futurism" />
        <div class="project-info">
          <h5>Neo Futurism</h5>
          <p>Exploring future cityscapes through bold design elements.</p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="project-card">
        <img src="5.w.jpg" alt="Organic Shapes" />
        <div class="project-info">
          <h5>Organic Shapes</h5>
          <p>Smooth and natural forms inspired by biology and nature.</p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="project-card">
        <img src="6.w.jpg" alt="Vintage Posters" />
        <div class="project-info">
          <h5>Vintage Posters</h5>
          <p>Retro poster designs bringing back the charm of old times.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="modal fade" id="loginModal" tabindex="-1" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered">
    <div class="modal-content p-4 text-center" style="background: #0e2433; color: #d0f0f7; border-radius: 1rem;">
      
      <div class="modal-header border-0 justify-content-center">
        <h5 class="modal-title fw-bold text-info">🔓 Welcome Back!</h5>
        <button type="button" class="btn-close btn-close-white position-absolute end-0 me-3" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      
      <div class="modal-body">
        <form class="mx-auto" style="max-width: 400px;">
          <div class="mb-3 text-start">
            <label for="loginUserID" class="form-label">User ID</label>
            <input type="text" class="form-control bg-dark text-light border-info" id="loginUserID" placeholder="Enter your user ID" />
          </div>
          
          <div class="mb-4 text-start">
            <label for="loginPassword" class="form-label">Password</label>
            <input type="password" class="form-control bg-dark text-light border-info" id="loginPassword" placeholder="••••••••" />
          </div>
          
          <button type="submit" class="btn btn-info w-100 fw-bold py-2 mb-3">Login Securely</button>
          
          <div class="text-center">
            <small class="text-muted">
              Don't have an account? 
              <a href="#" class="text-info" data-bs-toggle="modal" data-bs-target="#signupModal" data-bs-dismiss="modal">Sign Up</a>
            </small>
          </div>
        </form>
      </div>
    </div>
  </div>
</div>




<div class="modal fade" id="signupModal" tabindex="-1" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered">
    <div class="modal-content p-4" style="background: #0e2433; color: #d0f0f7; border-radius: 1rem;">
      <div class="modal-header border-0">
        <h5 class="modal-title fw-bold text-info">🚀 Join the Creative Revolution</h5>
        <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <form>
          <div class="row g-3">
            <div class="col-md-6">
              <label for="fullName" class="form-label">Full Name</label>
              <input type="text" class="form-control bg-dark text-light border-info" id="fullName" placeholder="e.g. Arya Stark" />
            </div>
            <div class="col-md-6">
              <label for="signupUserID" class="form-label">User ID</label>
              <input type="text" class="form-control bg-dark text-light border-info" id="signupUserID" placeholder="Choose a user ID" />
            </div>
            <div class="col-md-6">
              <label for="emailAddress" class="form-label">Email</label>
              <input type="email" class="form-control bg-dark text-light border-info" id="emailAddress" placeholder="you@example.com" />
            </div>
            <div class="col-md-6">
              <label for="dob" class="form-label">Date of Birth</label>
              <input type="date" class="form-control bg-dark text-light border-info" id="dob" />
            </div>
            <div class="col-md-6">
              <label for="signupPassword" class="form-label">Password</label>
              <input type="password" class="form-control bg-dark text-light border-info" id="signupPassword" placeholder="••••••••" />
            </div>
            <div class="col-md-6">
              <label for="confirmPassword" class="form-label">Confirm Password</label>
              <input type="password" class="form-control bg-dark text-light border-info" id="confirmPassword" placeholder="••••••••" />
            </div>
          </div>
          <div class="form-check mt-3">
            <input class="form-check-input bg-info border-info" type="checkbox" id="termsCheck" />
            <label class="form-check-label" for="termsCheck">
              I agree to the <a href="#" class="text-info">terms and conditions</a>
            </label>
          </div>
          <button type="submit" class="btn btn-info mt-4 w-100 fw-bold py-2">Create Account</button>
        </form>
      </div>
    </div>
  </div>
</div>


<footer>
  <h4>Contact Us</h4>
  <p>Email: contact@srivatsanhub.com</p>
  <p>Phone: +91 9876543210</p>
  <p>Address: 123 Creative Lane, Chennai, India</p>
  <p>© 2025 Srivatsan Creative Hub. All rights reserved.</p>
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>






```



# OUTPUT:

![alt text](<Screenshot 2025-05-20 154116.png>)
![alt text](<Screenshot 2025-05-20 154132.png>)
![alt text](<Screenshot 2025-05-20 153842.png>)
![alt text](<Screenshot 2025-05-20 153718.png>)



# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
