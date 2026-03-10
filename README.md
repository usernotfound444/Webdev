# Webdev
I created my first  website
<br>
Author- B D CHANDAN BEHERA
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blood Donation Registration | Save a Life</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #e63946;
            --secondary-color: #1d3557;
            --bg-color: #f1faee;
            --text-color: #333;
            --white: #ffffff;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        header {
            background-color: var(--white);
            padding: 1rem 5%;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--primary-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo span {
            color: var(--secondary-color);
        }

        main {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 2rem;
        }

        .container {
            background: var(--white);
            width: 100%;
            max-width: 500px;
            padding: 2.5rem;
            border-radius: 12px;
            box-shadow: var(--shadow);
            border-top: 5px solid var(--primary-color);
        }

        .header-text {
            text-align: center;
            margin-bottom: 2rem;
        }

        .header-text h1 {
            color: var(--secondary-color);
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .header-text p {
            color: #666;
            font-size: 0.9rem;
        }

        .form-group {
            margin-bottom: 1.2rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            font-size: 0.9rem;
            color: var(--secondary-color);
        }

        input, select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        input:focus, select:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(230, 57, 70, 0.1);
        }

        .btn-submit {
            width: 100%;
            padding: 14px;
            background-color: var(--primary-color);
            color: var(--white);
            border: none;
            border-radius: 6px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
            margin-top: 1rem;
        }

        .btn-submit:hover {
            background-color: #c92a36;
        }

        footer {
            text-align: center;
            padding: 1.5rem;
            background-color: var(--secondary-color);
            color: var(--white);
            font-size: 0.9rem;
        }

        footer a {
            color: #8ecae6;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        #success-message {
            display: none;
            text-align: center;
            padding: 2rem;
        }

        .success-icon {
            color: #2a9d8f;
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        @media (max-width: 600px) {
            .container {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">
            ❤️ <span>BloodConnect</span>
        </div>
    </header>

    <main>
        <div class="container">
            
            <div id="registration-form">
                <div class="header-text">
                    <h1>Donor Registration</h1>
                    <p>Join our community of lifesavers. Please fill in your details below.</p>
                </div>

                <!-- FORMSPREE FORM START -->
                <!-- IMPORTANT: Replace YOUR_FORMSPREE_ID with your actual Formspree ID -->
                <form action="https://formspree.io/f/meerakqj" method="POST">
                    
                    <div class="form-group">
                        <label for="fullname">Full Name</label>
                        <input type="text" id="fullname" name="fullname" placeholder="e.g. John Doe" required>
                    </div>

                    <div class="form-group">
                        <label for="rollno">Roll Number / ID</label>
                        <input type="text" id="rollno" name="rollno" placeholder="e.g. 2023001" required>
                    </div>

                    <div class="form-group">
                        <label for="branch">Branch / Department</label>
                        <input type="text" id="branch" name="branch" placeholder="e.g. Computer Science" required>
                    </div>

                    <div class="form-group">
                        <label for="contact">Contact Number</label>
                        <input type="tel" id="contact" name="contact" placeholder="e.g. +91 98765 43210" required>
                    </div>

                    <div class="form-group">
                        <label for="bloodgroup">Blood Group</label>
                        <select id="bloodgroup" name="bloodgroup" required>
                            <option value="" disabled selected>Select your blood group</option>
                            <option value="A+">A+</option>
                            <option value="A-">A-</option>
                            <option value="B+">B+</option>
                            <option value="B-">B-</option>
                            <option value="AB+">AB+</option>
                            <option value="AB-">AB-</option>
                            <option value="O+">O+</option>
                            <option value="O-">O-</option>
                        </select>
                    </div>

                    <button type="submit" class="btn-submit">Register as Donor</button>
                </form>
                <!-- FORMSPREE FORM END -->

            </div>

            <div id="success-message">
                <div class="success-icon">✓</div>
                <h2>Registration Successful!</h2>
                <p>Thank you for registering. We have received your details.</p>
                <p style="margin-top: 10px; font-size: 0.9rem; color: #666;">For any assistance, please contact us.</p>
                <a href="mailto:chandanff0000@gmail.com" style="color: var(--primary-color); font-weight: bold; text-decoration: none; margin-top: 10px; display: inline-block;">
                    chandanff0000@gmail.com
                </a>
                <button onclick="location.reload()" class="btn-submit" style="margin-top: 20px; background-color: var(--secondary-color);">Register Another</button>
            </div>

        </div>
    </main>

    <footer>
        <p>&copy; 2023 BloodConnect. All rights reserved.</p>
        <p style="margin-top: 5px;">Need Help? Email us at <a href="mailto:chandanff0000@gmail.com">chandanff0000@gmail.com</a></p>
    </footer>

    <script>
        // This script handles the success message display
        document.getElementById('registration-form').addEventListener('submit', function(e) {
            // Formspree will handle the actual submission
            // We just show the success message after submission
            const form = document.getElementById('registration-form');
            const successMsg = document.getElementById('success-message');
            
            // Show loading state
            const submitBtn = form.querySelector('.btn-submit');
            submitBtn.textContent = 'Sending...';
            submitBtn.disabled = true;
        });
    </script>

</body>
</html>
