# vitacheck.netlify.app
# SymptoCheck – Early Disease Detection Demo App  **SymptoCheck** is a simple, educational web app that helps users check possible common health conditions based on selected symptoms. It's built with HTML, CSS, JavaScript, and Bootstrap for a modern, responsive, and visually engaging experience.  ### 🌟 Features - Select from a list 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Early Disease Detection App</title>

    <!-- Bootstrap -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- Custom CSS -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="container">
    <div class="header text-center mb-5 animate-fade-in">
        <h1 class="display-4 fw-bold text-primary">Early Disease Detection App</h1>
        <p class="lead text-muted">Select symptoms and check results!</p>
    </div>

    <div class="disclaimer p-4 rounded shadow-sm bg-light border border-warning animate-slide-up">
        <strong class="text-danger">Disclaimer:</strong> Educational demo only • Not medical advice • Consult a doctor
    </div>

    <form id="symptomForm" class="mt-4">
        <div class="row g-4">

            <div class="col-lg-6">
                <h5 class="mb-3 text-primary fw-bold">Common Symptoms</h5>
                <div class="form-check animate-slide-up delay-1"><input class="form-check-input" type="checkbox" value="fever"> Fever</div>
                <div class="form-check animate-slide-up delay-2"><input class="form-check-input" type="checkbox" value="cough"> Cough</div>
                <div class="form-check animate-slide-up delay-3"><input class="form-check-input" type="checkbox" value="headache"> Headache</div>
                <div class="form-check animate-slide-up delay-4"><input class="form-check-input" type="checkbox" value="fatigue"> Fatigue</div>
                <div class="form-check animate-slide-up delay-5"><input class="form-check-input" type="checkbox" value="sore_throat"> Sore Throat</div>
                <div class="form-check animate-slide-up delay-6"><input class="form-check-input" type="checkbox" value="nausea"> Nausea</div>
                <div class="form-check animate-slide-up delay-7"><input class="form-check-input" type="checkbox" value="shortness_of_breath"> Shortness of Breath</div>
            </div>

            <div class="col-lg-6">
                <h5 class="mb-3 text-primary fw-bold">More Symptoms</h5>
                <div class="form-check animate-slide-up delay-8"><input class="form-check-input" type="checkbox" value="chest_pain"> Chest Pain</div>
                <div class="form-check animate-slide-up delay-9"><input class="form-check-input" type="checkbox" value="diarrhea"> Diarrhea</div>
                <div class="form-check animate-slide-up delay-10"><input class="form-check-input" type="checkbox" value="joint_pain"> Joint Pain</div>
                <div class="form-check animate-slide-up delay-11"><input class="form-check-input" type="checkbox" value="rash"> Skin Rash</div>
                <div class="form-check animate-slide-up delay-12"><input class="form-check-input" type="checkbox" value="loss_of_taste"> Loss of Taste/Smell</div>
                <div class="form-check animate-slide-up delay-13"><input class="form-check-input" type="checkbox" value="dizziness"> Dizziness</div>
            </div>

        </div>

        <div class="text-center mt-5">
            <button type="button" class="btn btn-primary btn-lg px-5 me-3 shadow animate-pulse" onclick="checkSymptoms()">Check Conditions</button>
            <button type="button" class="btn btn-outline-secondary btn-lg px-5 shadow" onclick="resetSymptoms()">Reset</button>
        </div>
    </form>

    <div id="results" class="mt-5"></div>
</div>

<!-- JavaScript -->
<script src="script.js"></script>
</body>
</html>
body {
    background: linear-gradient(135deg, #f5f7fa, #c3cfe2);
    min-height: 100vh;
    font-family: 'Segoe UI', sans-serif;
}

.container {
    max-width: 1000px;
    padding: 20px;
}

/* Animations */
.animate-fade-in {
    animation: fadeIn 1.2s ease-out;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
}

.animate-slide-up {
    opacity: 0;
    animation: slideUp 0.6s ease-out forwards;
}

@keyframes slideUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}

.animate-pulse {
    animation: pulse 2s infinite;
}

@keyframes pulse {
    0% { box-shadow: 0 0 0 0 rgba(13,110,253,0.4); }
    70% { box-shadow: 0 0 0 15px rgba(13,110,253,0); }
    100% { box-shadow: 0 0 0 0 rgba(13,110,253,0); }
}

/* Delay classes */
.delay-1 { animation-delay: .1s; }
.delay-2 { animation-delay: .2s; }
.delay-3 { animation-delay: .3s; }
.delay-4 { animation-delay: .4s; }
.delay-5 { animation-delay: .5s; }
.delay-6 { animation-delay: .6s; }
.delay-7 { animation-delay: .7s; }
.delay-8 { animation-delay: .8s; }
.delay-9 { animation-delay: .9s; }
.delay-10 { animation-delay: 1s; }
.delay-11 { animation-delay: 1.1s; }
.delay-12 { animation-delay: 1.2s; }
.delay-13 { animation-delay: 1.3s; }

/* Cards */
.disease-card {
    border-radius: 20px;
    margin-bottom: 30px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    transition: all 0.6s ease;
}

.disease-card:hover {
    transform: translateY(-15px) scale(1.05);
}

/* Card colors */
.card-1 { background: linear-gradient(135deg, #ff9a9e, #fad0c4); }
.card-2 { background: linear-gradient(135deg, #a1c4fd, #c2e9fb); }
.card-3 { background: linear-gradient(135deg, #d4fc79, #96e6a1); }
.card-4 { background: linear-gradient(135deg, #89f7fe, #66a6ff); }
.card-5 { background: linear-gradient(135deg, #fcb69f, #ffecd2); }
.card-6 { background: linear-gradient(135deg, #ff9a9e, #fecfef); }
.card-7 { background: linear-gradient(135deg, #b3ffab, #12fff7); }
.card-8 { background: linear-gradient(135deg, #f093fb, #f5576c); }
const diseases = [
    { name: "Common Cold", symptoms: ["cough", "sore_throat", "headache", "fatigue", "fever"] },
    { name: "Influenza (Flu)", symptoms: ["fever", "cough", "fatigue", "headache", "joint_pain", "sore_throat"] },
    { name: "COVID-19", symptoms: ["fever", "cough", "shortness_of_breath", "fatigue", "loss_of_taste", "headache"] },
    { name: "Gastroenteritis", symptoms: ["nausea", "diarrhea", "fever", "headache"] },
    { name: "Migraine", symptoms: ["headache", "nausea", "dizziness", "fatigue"] },
    { name: "Pneumonia", symptoms: ["cough", "fever", "shortness_of_breath", "chest_pain", "fatigue"] },
    { name: "Allergic Reaction", symptoms: ["rash", "cough", "shortness_of_breath", "dizziness"] },
    { name: "Heart Issue", symptoms: ["chest_pain", "shortness_of_breath", "fatigue", "dizziness"] }
];

function checkSymptoms() {
    const selected = [...document.querySelectorAll('input[type="checkbox"]:checked')]
        .map(cb => cb.value);

    if (!selected.length) {
        alert("Select at least one symptom");
        return;
    }

    const matches = diseases.map(d => {
        const count = d.symptoms.filter(s => selected.includes(s)).length;
        const percent = Math.round((count / d.symptoms.length) * 100);
        return { ...d, count, percent };
    }).filter(d => d.count > 0).sort((a, b) => b.percent - a.percent);

    let html = `<h3 class="text-center text-primary fw-bold">Possible Conditions</h3>`;

    matches.forEach((m, i) => {
        html += `
        <div class="card disease-card card-${(i % 8) + 1}">
            <div class="card-body text-center py-5">
                <h2 class="fw-bold">${m.name}</h2>
                <p class="text-danger fs-3">${m.percent}% Match</p>
                <p>(${m.count} of ${m.symptoms.length} symptoms)</p>
                <small class="text-muted">Educational only</small>
            </div>
        </div>`;
    });

    document.getElementById("results").innerHTML = html;
}

function resetSymptoms() {
    document.querySelectorAll('input[type="checkbox"]').forEach(cb => cb.checked = false);
    document.getElementById("results").innerHTML = "";
}
