

<head>
    <style>
        .grade-input-container {
            padding-bottom: 20px;
        }
    </style>
    <title>Curve Grades</title>
</head>

<body>
<div class="grade-input-container">
    <label for="Grades">Enter Grades:</label><br>
    <input type="text" id="ungrades" name="grades" size="50"><br>
    <button onclick="SaveCurveGrades()">Curve Grades!</button>
</div>


<div class="curved-input-container">
    <label for="displayValue">Curved Grades:</label><br>
    <input type="text" name="display" size="50" id="displayValue">
</div>

<div class="step-by-step">
    <p


<script>
function SaveCurveGrades() {
    const gradeslist = [];
    var obgrades = document.getElementsByName('grades')[0].value;

    
    const gradesArray = obgrades.split(' ');

   
    const curvedGrades = gradesArray.map(grade => {
        const numericGrade = parseFloat(grade);
        return Math.round(10 * Math.sqrt(numericGrade));
    });

    document.getElementsByName('display')[0].value = curvedGrades.join(' ');
}
</script>
</body>

















