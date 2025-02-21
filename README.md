<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IT Skill Booster</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&family=Ubuntu:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(45deg, #F1F3F4, #8A4F1D);
            color: #fff;
            transition: background-color 0.5s ease;
            overflow-x: hidden;
        }

        /* Navbar */
        .navbar {
            display: flex;
            justify-content: space-between;
            padding: 20px;
            background-color: #0088cc;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 10;
            transition: background-color 0.3s;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo-img {
            width: 40px;
            margin-right: 10px;
        }

        h1 {
            color: white;
            font-size: 28px;
            font-weight: 500;
            text-transform: uppercase;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-weight: 500;
            font-size: 18px;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #ffdc00;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #FF6F00, #FFDC00);
            color: white;
            padding: 120px 20px;
            text-align: center;
            animation: fadeIn 1s ease-out;
            position: relative;
            z-index: 5;
        }

        .hero h2 {
            font-size: 50px;
            margin-bottom: 20px;
            font-family: 'Ubuntu', sans-serif;
            font-weight: 700;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 40px;
        }

        .btn-primary {
            background-color: #ffdc00;
            color: #0088cc;
            padding: 15px 40px;
            text-decoration: none;
            font-weight: 700;
            font-size: 18px;
            border-radius: 30px;
            transition: background-color 0.3s ease;
        }

        .btn-primary:hover {
            background-color: #ffbb00;
        }

        /* Courses Section */
        .section {
            padding: 80px 20px;
            text-align: center;
            background: #6B3A16;
            border-radius: 15px;
            margin-top: 100px;
            animation: fadeIn 1.5s ease-out;
        }

        .section h2 {
            font-size: 40px;
            font-weight: 700;
            margin-bottom: 30px;
        }

        .courses-container {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }

        .course-card {
            background-color: #fff;
            border-radius: 12px;
            width: 300px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            margin-bottom: 40px;
        }

        .course-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }

        .course-card h3 {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .course-card p {
            font-size: 16px;
            margin-bottom: 25px;
            color: #333;
        }

        .btn-secondary {
            background-color: #0088cc;
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            font-weight: 500;
            border-radius: 30px;
            transition: background-color 0.3s ease;
        }

        .btn-secondary:hover {
            background-color: #006fa6;
        }

        /* Course Details */
        .course-details {
            display: none;
            padding: 50px 20px;
            background: #333;
            color: #fff;
            margin-top: 40px;
            border-radius: 15px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            animation: fadeIn 1.5s ease-out;
        }

        .course-details h3 {
            font-size: 36px;
            margin-bottom: 20px;
        }

        .course-details ol {
            text-align: left;
            font-size: 18px;
            margin-bottom: 40px;
        }

        /* Footer */
        .footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 30px;
            position: relative;
        }

        /* Animations */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

    </style>
</head>
<body>

    <header class="navbar">
        <div class="logo">
            <img src="telegram-logo.png" alt="Telegram Logo" class="logo-img">
            <h1>IT Skill Booster</h1>
        </div>
        <nav>
            <a href="#courses">Курсы</a>
            <a href="#speakers">Спикеры</a>
            <a href="#promo">Канал</a>
        </nav>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h2>Boost Your IT Skills</h2>
            <p>Start your learning journey with interactive courses and challenges!</p>
            <a href="#courses" class="btn-primary">Start Now 👇</a>
        </div>
    </section>

    <section id="courses" class="section">
        <h2>Available Courses</h2>
        <div class="courses-container">
            <div class="course-card">
                <h3>Web Development 🚀</h3>
                <p>Learn the basics of HTML, CSS, and JavaScript.</p>
                <a href="#web-development" class="btn-secondary" onclick="showCourse('web-development')">Start Learning</a>
            </div>
            <div class="course-card">
                <h3>Machine Learning 🤖</h3>
                <p>Understand algorithms and data processing for AI development.</p>
                <a href="#machine-learning" class="btn-secondary" onclick="showCourse('machine-learning')">Start Learning</a>
            </div>
            <div class="course-card">
                <h3>Python Programming 🐍</h3>
                <p>Get hands-on with Python programming and problem-solving.</p>
                <a href="#python-programming" class="btn-secondary" onclick="showCourse('python-programming')">Start Learning</a>
            </div>
        </div>
    </section>

    <section id="web-development" class="course-details">
        <h3>Web Development 🚀</h3>
        <p>Welcome to the Web Development course! In this section, you will learn the fundamentals of building websites using HTML, CSS, and JavaScript.</p>
        <h4>Step-by-Step Guide</h4>
        <ol>
            <li>Learn HTML structure and tags.</li>
            <li>Style with CSS to make your website beautiful.</li>
            <li>Interactive JavaScript to add dynamic functionality.</li>
            <li>Deploy your site using platforms like GitHub Pages.</li>
        </ol>
    </section>

    <section id="machine-learning" class="course-details">
        <h3>Machine Learning 🤖</h3>
        <p>Machine learning helps computers to learn from data. We will start by understanding the basics of machine learning and building simple models.</p>
        <h4>Step-by-Step Guide</h4>
        <ol>
            <li>Understand machine learning algorithms.</li>
            <li>Process data using Python and pandas.</li>
            <li>Train models with libraries like scikit-learn.</li>
            <li>Evaluate model performance and improve.</li>
        </ol>
    </section>

    <section id="python-programming" class="course-details">
        <h3>Python Programming 🐍</h3>
        <p>Python is a versatile language great for web development, data analysis, AI, and much more. Let’s start with the basics and move to advanced topics!</p>
        <h4>Step-by-Step Guide</h4>
        <ol>
            <li>Learn Python syntax and variables.</li>
            <li>Work with loops and functions to solve problems.</li>
            <li>Build a small project like a calculator.</li>
            <li>Deploy your Python projects to the cloud.</li>
        </ol>
    </section>

    <footer class="footer">
        <p>&copy; 2025 IT Skill Booster | Designed with Modern Style</p>
    </footer>

    <script>
        function showCourse(courseId) {
            document.querySelectorAll('.course-details').forEach(function(course) {
                course.style.display = 'none';
            });
            document.getElementById(courseId).style.display = 'block';
            window.scrollTo({
                top: document.getElementById(courseId).offsetTop,
                behavior: 'smooth'
            });
        }

        // Simple animation for the hero section
        document.addEventListener('DOMContentLoaded', () => {
            const hero = document.querySelector('.hero');
            hero.classList.add('fadeIn');
        });
    </script>
</body>
</html>
