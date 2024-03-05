<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grade Calculator</title>
    <style>
        /* Add any custom styling here */
    </style>
</head>
<body>
    <h2>Grade Calculator</h2>
    <p>Please enter your grade for each section:</p>
    <table>
        <tr>
            <td>Type</td>
            <td>Weight</td>
            <td>Grade</td>
        </tr>
        <tr>
            <td>MC Grade</td>
            <td>25%</td>
            <td><input type="number" id="mcgrade" min="0" max="5" step="0.1"></td>
        </tr>
        <tr>
            <td>PT Grade</td>
            <td>25%</td>
            <td><input type="number" id="ptgrade" min="0" max="5" step="0.1"></td>
        </tr>
        <tr>
            <td>Exercise</td>
            <td>50%</td>
            <td><input type="number" id="exercise" min="0" max="5" step="0.1"></td>
        </tr>
    </table>
    <br>
    <input type="button" value="Calculate Your Grade" onclick="calculateGrade()">
    <hr>
    <div id="outputDiv"></div>

    <script>
        function calculateGrade() {
            const mcGrade = parseFloat(document.getElementById('mcgrade').value);
            const ptGrade = parseFloat(document.getElementById('ptgrade').value);
            const exerciseGrade = parseFloat(document.getElementById('exercise').value);

            // Calculate the weighted average
            const totalWeight = 0.25 + 0.25 + 0.5;
            const weightedSum = mcGrade * 0.25 + ptGrade * 0.25 + exerciseGrade * 0.5;
            const averageGrade = weightedSum / totalWeight;

            // Display the result
            const outputDiv = document.getElementById('outputDiv');
            outputDiv.innerHTML = `Your Final Grade Is: ${averageGrade.toFixed(2)}`;
        }
    </script>
</body>
</html>
