# AHEGANOVIC.github.io
Website for curving grades

<html>
<head>
    <label for="Name">Enter Grades Here:</label>
    <input type="text" id="grades:" name="grade">
</head>

<body>
<button onclick="getGrades()" id="saveButton" type="button">Save Numbers! </button>
</body>

<script>
    function getGrades() {
        const gradeslist = new Array();
var grades = document.getElementById('grades').value;
gradeslist.push(grades)
}
</script>

<script>
var button = document.getElementById("saveButton");
button.addEventListener("click", getGrades());
button.classList.toggle("show")
</script>















