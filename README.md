

<label for="Grades">Enter Grades:</label><br>
<input type="text" id="ungrades" name="grades"><br>

<body>
<button onclick = "SaveCurveGrades()" >Save Numbers and Curve Grades!</button>
</body>

<label for="displayValue">Curved Grades: </label><input type="textbox" name="display">

<script>
function SaveCurveGrades() {
    const gradeslist = new Array();
    var obgrades = parseInt(document.getElementsByName('grades')[0].value);
    gradeslist.push(obgrades);
    const [ ...grades ] = gradeslist[0];
    grades.forEach((grade, index) => {
        const curve = 10 * Math.sqrt(grade);
        document.getElementsByName('display')[0].value = curve;
    })
    
}
 </script>

















