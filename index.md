<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paraskevi Platanou</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            background-color: #fff;
            color: #333;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        header h1 {
            margin: 0;
        }
        nav {
            display: flex;
        }
      header img {
            border-radius: 50%;
            width: 50px; /* Set a fixed size for the image */
            height: 50px;
            object-fit: cover;
            margin-right: 20px; /* Add some spacing if needed */
        }
        nav a {
            color: #fff;
            text-decoration: none;
            padding: 10px 15px;
            margin: 0 5px;
            background-color: #555;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        nav a:hover {
            background-color: #777;
        }
        nav a.active {
            background-color: #007BFF;
        }
        section {
            margin: 20px auto;
            max-width: 800px;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            display: none; /* Hidden by default */
        }
        section.active {
            display: block; /* Show the active tab's content */
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: #fff;
            margin-top: 20px;
        }
    </style>
    <script>
        function showSection(id) {
            // Hide all sections
            const sections = document.querySelectorAll('section');
            sections.forEach(section => section.classList.remove('active'));
            
            // Show the clicked section
            const activeSection = document.getElementById(id);
            activeSection.classList.add('active');

            // Update active class in the nav bar
            const links = document.querySelectorAll('nav a');
            links.forEach(link => link.classList.remove('active'));
            document.querySelector(`nav a[href="#${id}"]`).classList.add('active');
        }

        // Initialize the page with the first tab active
        document.addEventListener('DOMContentLoaded', () => {
            showSection('about'); // Default tab
        });
    </script>
</head>
<body>
    <header>
       <img src="pic.jpg" alt="Paraskevi Platanou"> <!-- Add your image here -->
        <h1>Paraskevi Platanou</h1>
        <nav>
            <a href="#about" onclick="showSection('about')">About</a>
            <a href="#projects" onclick="showSection('projects')">Projects</a>
            <a href="#publications" onclick="showSection('publications')">Publications</a>
            <a href="#talks" onclick="showSection('talks')">Talks</a>
        </nav>
    </header>
    <section id="about" class="active">
        <h2>About Me</h2>
        <p>
            I am a Ph.D. candidate at the Department of Informatics at Athens University of Economics and Business and an Archimedes/Athena RC Research Fellow, specializing in machine learning for written material culture. My expertise lies in OCR for ancient Greek handwritten texts, with published work on Byzantine text recognition and error correction. I have contributed to Digital Papyrology and Palaeography as a visiting research fellow at Ghent University and received training on digital approaches to papyrology, palaeography, epigraphy, and sigillography from institutions like Heidelberg University, Oxford University, Cologne University and Dartmouth College. My research combines classical studies and digital innovation to enhance the study and scholarly analysis of cultural materials.
        </p>
    </section>
    <section id="projects">
        <h2>Projects</h2>
        <p>
Archimedes/Athena RC: Research collaboration in machine learning for Natural Language Processing (NLP).
          
Oxford University: Research collaboration on the PARSing and Multi-word Expressions project.

Ghent University: Database management and paleographic annotation for the ERC project “Everyday Writing in Graeco-Roman and Late Antique Egypt”.

Venice Centre for Digital and Public Humanities, Ca’ Foscari University of Venice: Participation in the HTREC 2022 project and the Venice Summer School for Digital and Public Humanities.

Institute for Classical Studies, University of London (UCL): Archival and library work, including curating the Michael Ventris collection.
        </p>
    </section>
    <section id="publications">
        <h2>Publications</h2>
        <p>
John Pavlopoulos, Vasiliki Kougia, Esteban Garces Arias, Paraskevi Platanou, Stepan Shabalin, Konstantina Liagkou, Emmanouil Papadatos, Holger Essler, Jean-Baptiste Camps, and Franz Fischer. 2024. Challenging Error Correction in Recognised Byzantine Greek. In Proceedings of the 1st Workshop on Machine Learning for Ancient Languages (ML4AL 2024), pp. 1–12, Bangkok, Thailand. Association for Computational Linguistics.

John Pavlopoulos, Vasiliki Kougia, Paraskevi Platanou, and Holger Essler. 2023. Detecting Erroneously Recognized Handwritten Byzantine Text. In Findings of the Association for Computational Linguistics: EMNLP 2023, pp. 7818–7828, Singapore. Association for Computational Linguistics.

P. Platanou, J. Pavlopoulos, G. Papaioannou, Handwritten Paleographic Greek Text Recognition: A Century-Based Approach, Proc. Conference on Language Resources and Evaluation (LREC 2022), pp. 6585–6589, 2022.
          
Academic Theses

"Conflictual Relationships in Papyrological Letters of Roman and Byzantine Egypt," supervised by Associate Professor A. Koroli and Professor A. Papathomas.

"Deep Learning-Based OCR for Greek Paleographic Manuscripts," supervised by Associate Professor G. Papaioannou and Assistant Professor I. Pavlopoulos.</p>
    </section>
    <section id="talks">
        <h2>Talks</h2>
        <p>
HTR and OCR from Papyrus to Codex. SunoikisisDC Summer 2024, Online.

HTR of Handwritten Paleographic Greek Text as a Function of Chronology. École nationale des chartes, Paris.

Machine Learning Applications in Old Greek Manuscripts. 

UCL Lyceum Classics Community Seminar, University College London.
        </p>
    </section>
    <footer>
        <p>Contact Information: E-mail: platanou at aueb dot gr, p.platanou at athenarc dot gr</p>
    </footer>
</body>
</html>
