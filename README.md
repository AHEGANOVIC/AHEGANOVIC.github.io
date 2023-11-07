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

<body>
<button onclick="curveGrades()" id="curveButton" type="button">Curve Numbers! </button>
</body>

<body>
<button onclick="clearGrades()"> id="clearButton" type="button">Clear Numbers! </button>
</body>

<script>
function getGrades(){
    const gradeslist = new Array();
    var grades = document.getElementById('grades').value;
    gradeslist.push(grades)
    var button = document.getElementById("saveButton");
    button.addEventListener("click", getGrades());
    button.classList.toggle("show")
}
</script>

<script>
    function curveGrades() {
    }
</script>

<script>
    function clearGrades() {
    }
</script>












