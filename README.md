<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WiFi Check</title>
</head>
<body>
    <h1 id="status"></h1>
</body>
</html>

<style>
    body {
        background-color: black;
    }
    #status {
        color: white;
    }
</style>

<script>
    window.addEventListener("load", (event) =>{
        const statusDisplay = document.getElementById("status");
        statusDisplay.textContent = navigator.onLine ? "Online" : "Offline";
    });

    window.addEventListener("offline", (event) =>{
        const statusDisplay = document.getElementById("status");
        statusDisplay.textContent = "Offline";
    });

    window.addEventListener("online", (event) =>{
        const statusDisplay = document.getElementById("status");
        statusDisplay.textContent = "Online";
    });
    
</script>
