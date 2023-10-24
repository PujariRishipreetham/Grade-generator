document.getElementById("calculateButton").addEventListener("click", calculateGrades);

function calculateGrades() {
    const subjectCount = parseInt(document.getElementById("subjectCount").value);
    let totalMarks = 0;

    for (let i = 1; i <= subjectCount; i++) {
        const mark = parseInt(document.getElementById("subjectMark" + i).value);
        totalMarks += mark;
    }

    const averagePercentage = totalMarks / subjectCount;

    let grade = "N/A";
    if (averagePercentage >= 90) {
        grade = "A+";
    } else if (averagePercentage >= 80) {
        grade = "A";
    } else if (averagePercentage >= 70) {
        grade = "B";
    } else if (averagePercentage >= 60) {
        grade = "C";
    } else if (averagePercentage >= 50) {
        grade = "D";
    } else {
        grade = "F";
    }

    document.getElementById("totalMarks").textContent = totalMarks;
    document.getElementById("averagePercentage").textContent = averagePercentage.toFixed(2);
    document.getElementById("grade").textContent = grade;
    document.getElementById("results").style.display = "block";
}

// Dynamically create input fields for subject marks based on the subject count
document.getElementById("subjectCount").addEventListener("input", createSubjectMarkInputs);

function createSubjectMarkInputs() {
    const subjectCount = parseInt(document.getElementById("subjectCount").value);
    const subjectMarksDiv = document.getElementById("subjectMarks");
    subjectMarksDiv.innerHTML = "";

    for (let i = 1; i <= subjectCount; i++) {
        const input = document.createElement("input");
        input.type = "number";
        input.id = "subjectMark" + i;
        input.placeholder = "Enter Marks for Subject " + i;
        input.required = true;
        subjectMarksDiv.appendChild(input);
        subjectMarksDiv.appendChild(document.createElement("br"));
    }
}
