

<label for="Grades">Enter Grades:</label><br>
<input type="text" id="ungrades" name="grades"><br>

<body>
<button onclick = "saveGrades()" >Save Numbers!</button>
</body>


<script>
function saveGrades(){
    const gradeslist = new Array(); 
    var obgrades = document.getElementById("ungrades").value; 
    gradeslist.push(obgrades);  
    for (const grades of gradeslist) {
        for (const grade of grades) {
            var x = grade;
        }
    }
}
 </script>

<script>
function curveGrades(){
    
}
</script>



document.getElementById("ungrades").value










