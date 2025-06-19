<html>
    @import "{{ site.theme }}";

header {
  display: none;
}
<head>
    <meta charset="UTF-8">
    <title>Contact Us - Provision Bookkeeping LLC</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;800&display=swap" rel="stylesheet">
    <style>
        html, body {
            height: 100%;
            margin: 0;
            font-family: 'Montserrat', sans-serif;
            color: #333;
        }

        body {
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        main {
            flex: 1 0 auto;
        }

        /* Form Styles */
        .main-title {
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-weight: 800;
            font-size: 24px;
            margin-bottom: 10px;
            color: #0C4466;
        }

        .subtitle {
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-weight: 800;
            font-size: 18px;
            margin-bottom: 20px;
            color: #0C4466;
        }

        .form-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
            padding: 20px;
        }

        .input-container {
            position: relative;
            display: inline-flex;
            align-items: center;
            width: calc(50% - 10px);
        }

        input {
            height: 48px;
            width: 100%;
            border: 1px solid #c0c0c0;
            border-radius: 4px;
            box-sizing: border-box;
            padding: 16px;
        }

        .label {
            position: absolute;
            top: 0;
            bottom: 0;
            left: 16px;
            display: flex;
            align-items: center;
            pointer-events: none;
        }

        input, .label .text {
            font-family: 'Segoe UI';
            font-size: 16px;
        }

        .label .text {
            transition: all 0.15s ease-out;
            color: grey;
        }

        input:focus {
            outline: none;
            border: 2px solid blue;
        }

        input:focus + .label .text, :not(input[value=""]) + .label .text {
            font-size: 12px;
            transform: translate(0, -150%);
            background-color: white;
            padding-left: 4px;
            padding-right: 4px;
        }

        input:focus + .label .text {
            color: blue;
        }

        .button-container {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }

        button {
            background-color: #EFB523;
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 4px;
            font-family: 'Segoe UI';
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #D89E1C;
        }

        .recaptcha-notice {
            text-align: center;
            font-family: 'Segoe UI';
            font-size: 12px;
            color: #666;
            margin-top: 10px;
        }

        .form-box {
            border: 2px solid #0C4466;
            border-radius: 8px;
            padding: 20px;
            margin: 0 auto 0;
            max-width: 500px;
        }

        .contact-directly {
            font-family: 'Montserrat', sans-serif;
            font-weight: 800;
            font-size: 18px;
            color: #0C4466;
            margin-bottom: 10px;
            text-align: center;
        }

        .contact-info {
            text-align: center;
            font-family: 'Segoe UI';
            font-size: 18px;
            color: #333;
            margin-top: 20px;
        }

        .contact-info a {
            color: #0C4466;
            text-decoration: none;
        }

        .contact-info a:hover {
            text-decoration: underline;
        }

        .divider {
            border: 2px solid #0C4466;
            border-radius: 8px;
            height: 2px;
            margin: 20px 0;
            background: none;
            width: 100%;
        }

        .hours-box {
            border: 2px solid #0C4466;
            border-radius: 8px;
            padding: 20px;
            margin: 20px auto;
            max-width: 500px;
            text-align: center;
        }

        .hours-box h3 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 800;
            font-size: 24px;
            color: #0C4466;
            margin-bottom: 10px;
        }

        .hours-box p {
            font-family: 'Segoe UI';
            font-size: 16px;
            color: #666666;
            margin: 5px 0;
            line-height: 1.5;
        }

        /* Footer Styles */
        footer {
            padding: 40px 20px 40px 20px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            flex-shrink: 0;
            background-color: #f8f8f8;
        }

        footer .contact-info {
            margin: 5px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            font-family: 'Segoe UI';
            font-size: 18px;
            color: #333;
        }

        footer .contact-item {
            margin: 5px 0;
        }

        footer .privacy-link {
            margin-top: 5px;
        }

        footer .terms-link {
            margin-top: 5px;
        }

        footer a {
            color: #0C4466;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        @media (max-width: 600px) {
            .form-container {
                flex-direction: column;
                align-items: center;
            }
            
            .input-container {
                width: 100%;
                max-width: 280px;
            }

            .form-box {
                padding: 15px;
            }

            .hours-box {
                padding: 15px;
            }

            footer {
                padding: 20px 15px 20px 15px;
            }

            .hours-box h3 {
                font-size: 20px;
            }

            .hours-box p {
                font-size: 14px;
            }
        }
    </style>
</head>
<body>
    <main>
        <form action="https://formspree.io/f/xnnpzbgq" method="POST">
            <div class="main-title">Contact us</div>
            <div class="form-box">
                <div class="subtitle">Enter your information below and we will reach out:</div>
                <div class="form-container">
                    <!-- First Name -->
                    <div class="input-container">
                        <input
                            type="text"
                            id="fname"
                            name="fname"
                            value=""
                            aria-labelledby="label-fname"
                            required
                        />
                        <label class="label" for="fname" id="label-fname">
                            <div class="text">First Name</div>
                        </label>
                    </div>

                    <!-- Last Name -->
                    <div class="input-container">
                        <input
                            type="text"
                            id="lname"
                            name="lname"
                            value=""
                            aria-labelledby="label-lname"
                            required
                        />
                        <label class="label" for="lname" id="label-lname">
                            <div class="text">Last Name</div>
                        </label>
                    </div>

                    <!-- Email -->
                    <div class="input-container">
                        <input
                            type="email"
                            id="email"
                            name="email"
                            value=""
                            aria-labelledby="label-email"
                            required
                        />
                        <label class="label" for="email" id="label-email">
                            <div class="text">Email</div>
                        </label>
                    </div>

                    <!-- Phone Number -->
                    <div class="input-container">
                        <input
                            type="tel"
                            id="phone"
                            name="phone"
                            value=""
                            aria-labelledby="label-phone"
                            required
                        />
                        <label class="label" for="phone" id="label-phone">
                            <div class="text">Phone Number</div>
                        </label>
                    </div>
                </div>

                <div class="button-container">
                    <button type="submit">Submit</button>
                </div>

                <div class="recaptcha-notice">
                    This site is protected by reCAPTCHA and the Google 
                    <a href="https://policies.google.com/privacy">Privacy Policy</a> and 
                    <a href="https://policies.google.com/terms">Terms of Service</a> apply.
                </div>

                <div class="divider"></div>

                <div class="contact-directly">Or contact us directly:</div>
                <div class="contact-info">
                    <p>Phone number: <a href="tel:760-525-4583">760-525-4583</a></p>
                    <p>Email: <a href="mailto:contact@provisionbk.com">contact@provisionbk.com</a></p>
                </div>
            </div>
        </form>

        <div class="hours-box">
            <h3>Hours of operation</h3>
            <p>Mon 9 AM – 5:00 PM</p>
            <p>Tues 9 AM – 5:00 PM</p>
            <p>Wed 9 AM – 5:00 PM</p>
            <p>Thu 9 AM – 5:00 PM</p>
            <p>Fri 9 AM – 5:00 PM</p>
            <p>Sat Closed</p>
            <p>Sun Closed</p>
        </div>
    </main>

    <footer>
        <div>© 2025 Provision Bookkeeping LLC</div>
        <div class="contact-info">
            <span class="contact-item">
                Email: <a href="mailto:contact@provisionbk.com" aria-label="Email Provision Bookkeeping">contact@provisionbk.com</a>
            </span>
            <span class="contact-item">
                Phone: <a href="tel:7605254583" aria-label="Call Provision Bookkeeping">760-525-4583</a>
            </span>
        </div>
        <div class="privacy-link">
            <a href="https://www.provisionbk.com/private-policy">Privacy Policy</a>
        </div>
        <div class="terms-link">
            <a href="https://www.provisionbk.com/terms-of-use">Terms of Service</a>
        </div>
    </footer>

    <script>
        // Array of input IDs
        const inputIds = ['fname', 'lname', 'email', 'phone'];
        
        // Add event listener to each input
        inputIds.forEach(id => {
            const input = document.getElementById(id);
            input.addEventListener('input', () => {
                input.setAttribute('value', input.value);
            });
        });
    </script>


</body>
</html>
