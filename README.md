
<head>
    <style>
        .grade-input-container {
            padding-bottom: 20px;
        }
        .step-by-step {
            line-height: 1.5
        }
        a[href="https://aheganovic.github.io/"] {
    display: none !important;
}
    </style>
   
<title>Curve Grades</title>
</head>

<h1 style="font-size: 60px;">Curving Grades</h1>
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

<div class="mean-reginput-contaner">
    <label for="displayValue5">Mean of Regular Grades:</label><br>
    <input type="text" name="display5" size="20" id="displayValue5">
</div>

<div class="mean-curveinput-container">
    <label for="displayValue1">Mean of Curved Grades:</label><br>
    <input type="text" name="display1" size="20" id="displayValue1">
</div>

<div class="range-input-container">
    <label for="displayValue2">Range of Curved Grades:</label><br>
    <input type="text" name="display2" size="20" id="displayValue2">
</div>

<div class="max-input-container">
    <label for="displayValue3">Max of Curved Grades:</label><br>
    <input type="text" name="display3" size="20" id="displayValue3">
</div>

<div class="min-input-container">
    <label for="displayValue4">Min of Curved Grades:</label><br>
    <input type="text" name="display4" size="20" id="displayValue4">
</div>

<script>
function SaveCurveGrades() {
    var obgrades = document.getElementsByName('grades')[0].value;
    var trimobgrades = obgrades.trim();
   
    const gradesArray = trimobgrades.split(' ');
   
    const curvedGrades = gradesArray.map(grade => {
        const numericGrade = parseFloat(grade);
        return Math.round(10 * Math.sqrt(numericGrade));
    });

    const sumOfCurvedGrades = curvedGrades.reduce((acc, value) => acc + value, 0);
    const meanCurveGrade = Math.round(sumOfCurvedGrades / curvedGrades.length);

    const range = Math.max(...curvedGrades) - Math.min(...curvedGrades);
    const max = Math.max(...curvedGrades); 
    const min = Math.min(...curvedGrades); 

    const parsedGrade = gradesArray.map(regrade => {
        const regNumericGrade = parseFloat(regrade);
    });
    const sumOfRegGrades = parsedGrade.reduce((acc, value) => acc + value, 0);
    const meanRegGrade = Math.round(sumOfRegGrades / sumOfRegGrades.length);
    

    document.getElementsByName('display')[0].value = curvedGrades.join(', ');
    document.getElementsByName('display1')[0].value = meanCurveGrade;
    document.getElementsByName('display2')[0].value = range;
    document.getElementsByName('display3')[0].value = max;
    document.getElementsByName('display4')[0].value = min;
    document.getElementsByName('display5')[0].value = meanRegGrade;
}
</script>
</body>
