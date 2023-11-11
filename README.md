


<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        label, input, button, label {
            margin-bottom: 10px; /* Add space below labels, inputs, and buttons */
        }
    </style>
    <title>Grade Curving</title>
</head>
<body>

<label for="Grades">Enter Grades:</label><br>
<input type="text" id="ungrades" name="grades"><br>

<button onclick="SaveCurveGrades()">Save Numbers and Curve Grades!</button>

<label for="displayValue">Curved Grades: </label>

<input type="text" name="display">

</body>

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


















