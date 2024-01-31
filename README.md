<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f2f2f2;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }

        #loginForm {
            background-color: #ffffff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            max-width: 400px;
            width: 100%;
            opacity: 1;
            transition: opacity 0.5s;
        }

        #loginForm.hidden {
            opacity: 0;
            pointer-events: none;
        }

        #loginForm h2 {
            background-color: #007bff;
            color: #ffffff;
            margin: 0;
            padding: 20px;
            text-align: center;
        }

        #loginForm form {
            padding: 20px;
        }

        #loginForm label {
            display: block;
            font-size: 14px;
            margin-bottom: 8px;
        }

        #loginForm input {
            width: 100%;
            padding: 10px;
            margin-bottom: 16px;
            box-sizing: border-box;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
        }

        #loginForm button {
            background-color: #007bff;
            color: #ffffff;
            padding: 12px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
        }

        @keyframes fadeOut {
            from {
                opacity: 1;
            }
            to {
                opacity: 0;
            }
        }

        .fadeOut {
            animation: fadeOut 0.5s ease-in-out;
        }
    </style>
    <title>Login Form</title>
</head>
<body>

<div id="loginForm">
    <h2>Login</h2>
    <form onsubmit="submitForm(event)">
        <label for="username">Username:</label>
        <input type="text" id="username" name="username" required>

        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>

        <button type="submit">Login</button>
    </form>
</div>

<script>
    function submitForm(event) {
        event.preventDefault();

        const loginForm = document.getElementById('loginForm');
        loginForm.classList.add('fadeOut');

        setTimeout(() => {
            loginForm.classList.add('hidden');
            loginForm.classList.remove('fadeOut');
        }, 500); // Adjust the timeout to match the animation duration
    }
</script>

</body>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>welcome</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
            text-align: center;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 1em;
        }

        section {
            margin: 20px;
        }

        h1 {
            color: #333;
        }

        p {
            color: #555;
        }

        footer {
            background-color: #333;
            color: #fff;
            padding: 1em;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to the website</h1>
    </header>

    <section>
        <h2>About Us</h2>
        <p>This is a cool website</p>
    </section>

    <section>
        <h2>Features</h2>
        <ul>
            <li>(blank)</li>
            <li>(blank)</li>
            <li>(blank)</li>
        </ul>
    </section>

    <footer>
        <p>&copy; 2024 website. All rights reserved.</p>
    </footer>
</body>
</html>
