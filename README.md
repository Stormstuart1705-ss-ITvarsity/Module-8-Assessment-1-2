<!DOCTYPE html>
<html>
    <head> 
        <link rel="stylesheet" type="text/css" href="style.css"> 
    </head>
    <body>
        <p>Welcome. Please log in</p>

        <form>
            <label for="usernameInput">Username:</label><input type="text" id="usernameInput"/><br/>
            <label for="passwordInput">Password:</label><input type="password" id="passwordInput"/><br/>
            <p id="message"></p>
            <br/><br/>
            <a href="#" onclick="verifyUser()">Log in</a>
        </form>

        <script>

            function verifyUser(){
                var username = document.getElementById("usernameInput").value;
                var password = document.getElementById("passwordInput").value;

                checkUserCreds(username, password);
            }


             function checkUserCreds(username, password){
                var systemUsername = "Stuart";
                var systemPassword = "1997";

                if(username == systemUsername && password == systemPassword){
                    document.getElementById("message").innerHTML = "Correct. logging you in...";
                } else{
                    document.getElementById("message").innerHTML = "Incorrect Username or Password";
                }
            }

             </script>
    </body>
</html> 
