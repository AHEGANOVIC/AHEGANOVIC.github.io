

<label for="Grades">Enter Grades:</label><br>
<input type="text" id="ungrades" name="grades"><br>

<body>
<button onclick="SaveCurveGrades()">Save Numbers and Curve Grades!</button>
</body>

<label for="displayValue">Curved Grades: </label><input type="textbox" name="display">

<script>
function SaveCurveGrades() {
    const gradeslist = [];
    var obgrades = document.getElementsByName('grades')[0].value;

    const gradesArray = obgrades.split(',');

    const curvedGrades = gradesArray.map(grade => {
        const numericGrade = parseFloat(grade);
        return Math.round(10 * Math.sqrt(numericGrade));
    });

    document.getElementsByName('display')[0].value = curvedGrades.join(', ');
}
</script>
















