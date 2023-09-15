<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DV Internationals - Survey</title>
    <style>
        body {
            background-image: url(login.jpg);
            background-size: cover; /* Replace with your desired background color */
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            font-family: 'Inter', sans-serif; /* Use the Inter font */
        }

        h1 {
            color: white;
            font-weight: bold;
            font-size: 36px;
            text-align: center;
        }

        .form-container {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid white;
            border-radius: 10px;
            padding: 20px;
            max-width: 400px;
            width: 100%;
        }

        .question {
            margin-bottom: 15px;
            color: white;
        }

        .input-field {
            width: 100%;
            padding: 10px;
            border: 1px solid white;
            border-radius: 5px;
        }

        .radio-label {
            color: white;
        }

        .continue-button {
            background: transparent;
            border: 2px solid white;
            color: white;
            font-weight: bold;
            font-size: 24px;
            padding: 15px 30px;
            margin: 20px 0;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s, color 0.3s;
        }

        .continue-button:hover {
            background-color: white;
            color: black;
        }
    </style>
</head>
<body>
    <h1>DV Internationals - Survey</h1>
    <div class="form-container">
        <form id="survey-form" >
            <div class="question">
                <label for="name">Question 1: What is your name?</label>
                <input type="text" id="name" class="input-field" name="name" required>
            </div>

            <div class="question">
                <label for="age">Question 2: Enter your age</label>
                <input type="number" id="age" class="input-field" name="age">
            </div>

            <div class="question">
                <label for="date">Question 3: Enter today's date</label>
                <input type="date" id="date" class="input-field" name="date"  required>
            </div>

            <div class="question">
                <label for="how-know">Question 4: How did you hear about us?</label>
                <input type="text" id="how-know" class="input-field" name="how" required>
            </div>

            <div class="question">
                <label>Question 5: Have you subscribed?</label><br>
                <input type="radio" id="yes" name="subscription" value="Yes" class="radio-input" name="yes" >
                <label class="radio-label" for="yes">Yes</label>
                <input type="radio" id="no" name="subscription" value="No" class="radio-input">
                <label class="radio-label" for="no">No</label>
            </div>

            <button type="button" class="continue-button" onclick="openNewWindow()">Continue</button>
        </form>
    </div>

    <script>
        function openNewWindow() {
            const subscription = document.querySelector('input[name="subscription"]:checked').value;
            if (subscription === "No") {
                window.open('file:///C:/Users/shivs/Downloads/NO.html'); // Replace with the link you want to open
            } else {
                window.open('file:///C:/Users/shivs/Downloads/welcome.html')
            }
        }
    </script>
</body>
</html>
