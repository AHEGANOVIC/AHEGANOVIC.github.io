# AHEGANOVIC.github.io
Website for curving grades

<html>
<head>
    <label for="Name">Enter Grades Here:</label>
    <input type="text" id="grades:" name="grade">
</head>

<button id="pythonButton" type="button">Save Numbers!</button>
<script>
    document.getElementById("pythonButton").addEventListener("click", getinput() {
        fetch('http://127.0.0.1:5000', {
            method: 'GET',
        })
        .then(response => response.json())
        .then(data => {
            console.log(data);
        })
        .catch(error => {
            console.error('Error:', error);
        });
    });
</script>












