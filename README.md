
<html>
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <label for="grades">Enter Grades Here:</label>
    <input type="text" id="grades" name="grade">
    
<button onclick="getGrades()" id="saveButton" type="button">Save Numbers!</button>
<button onclick="curveGrades()" id="curveButton" type="button">Curve Numbers!</button>
<button onclick="clearGrades()" id="clearButton" type="button">Clear Numbers!</button>
<button id="showPopupButton" onclick="showPopup()">Show Popup</button>
    
 <div id="popup" class="popup">
        <div class="popup-content">
            <span class="close" id="closePopupButton" onclick="closePopup()">×</span>
            <p>This is a simple popup!</p>
        </div>
    </div>

 <script>
        function getGrades() {
            const gradeslist = new Array();
            var grades = document.getElementById('grades').value;
            gradeslist.push(grades);
            var button = document.getElementById("saveButton");
        }
    </script>

 <script>
        function showPopup() {
            const popup = document.getElementById("popup");
            popup.style.display = "block";
        }
    </script>

 <script>
        function closePopup() {
            const popup = document.getElementById("popup");
            popup.style.display = "none";
        }
    </script>

 <script>
        function curveGrades() {
            // Define the functionality for curving grades here
        }
    </script>

 <script>
        function clearGrades() {
            // Define the functionality for clearing grades here
        }
    </script>
</body>













