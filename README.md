

<head>
    <style>
        .grade-input-container {
            padding-bottom: 20px;
        }
        .step-by-step {
            line-height: 1.5
        }
    </style>
    <title>Curve Grades</title>
</head>

<body>
<div class="step-by-step">
    <h1>How To Use:</h1>
        <p>
        (1) Put in your grades, separated by spaces, into the first input box <br>
        (2) Click the button to curve the grades <br>
        (3) Enjoy your curved grades!
        </p>
</div>
    
<div class="grade-input-container">
    <label for="Grades">Enter Grades:</label><br>
    <input type="text" id="ungrades" name="grades" size="100"><br>
    <button onclick="SaveCurveGrades()">Curve Grades!</button>
</div>

<div class="curved-input-container">
    <label for="displayValue">Curved Grades:</label><br>
    <input type="text" name="display" size="100" id="displayValue">
</div>

<div class="mean-input-container">
    <label for="displayValue1">Mean of Curved Grades:</label><br>
    <input type="text" name="display1" size="20" id="displayValue1">
</div>


<script>
function SaveCurveGrades() {
    const gradeslist = [];
    var obgrades = document.getElementsByName('grades')[0].value;
   
    const gradesArray = obgrades.split(' ');
   
    const curvedGrades = gradesArray.map(grade => {
        const numericGrade = parseFloat(grade);
        return Math.round(10 * Math.sqrt(numericGrade));
    });

    const meanCurveGrades = gradesArray.map(grades => {
      const sum = grades.reduce((acc, value) => acc + parseFloat(value), 0);
          const mean = sum / grades.length;
              return mean;
    });
    
    document.getElementsByName('display')[0].value = curvedGrades.join(', ');
    document.getElementsByName('display1')[0].value = meanCurveGrades
}
</script>
</body>

















