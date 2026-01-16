<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>ICME 2026 Grand Challenge | JND Prediction for Point Cloud Compression</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- MathJax for equations -->
  <script>
    MathJax = {
      tex: { inlineMath: [['$', '$'], ['\\(', '\\)']] }
    };
  </script>
  <script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

  <style>
    body {
      font-family: Arial, Helvetica, sans-serif;
      margin: 0;
      padding: 0;
      line-height: 1.6;
      color: #222;
      background-color: #ffffff;
    }

    header {
      background: #003366;
      color: #fff;
      padding: 1.2rem 0;
    }

    header h1 {
      margin: 0;
      text-align: center;
      font-size: 1.8rem;
    }

    header h2 {
      margin: 0.4rem 0 0;
      text-align: center;
      font-weight: normal;
      font-size: 1.1rem;
    }

    nav {
      background: #f2f2f2;
      padding: 0.6rem;
      text-align: center;
      border-bottom: 1px solid #ddd;
    }

    nav a {
      margin: 0 10px;
      color: #003366;
      text-decoration: none;
      font-weight: bold;
    }

    nav a:hover {
      text-decoration: underline;
    }

    .container {
      max-width: 1100px;
      margin: auto;
      padding: 2rem;
    }

    section {
      margin-bottom: 3rem;
    }

    section h2 {
      border-bottom: 2px solid #003366;
      padding-bottom: 0.4rem;
      color: #003366;
    }

    ul {
      margin-left: 1.2rem;
    }

    table {
      border-collapse: collapse;
      width: 100%;
      margin-top: 1rem;
    }

    table, th, td {
      border: 1px solid #aaa;
    }

    th, td {
      padding: 0.6rem;
      text-align: left;
    }

    footer {
      background: #f2f2f2;
      text-align: center;
      padding: 1rem;
      color: #555;
      font-size: 0.9rem;
    }

    .note {
      background: #eef5ff;
      padding: 1rem;
      border-left: 4px solid #003366;
      margin: 1rem 0;
    }
  </style>
</head>

<body>

<header>
  <h1>ICME 2026 Grand Challenge</h1>
  <h2>Perceptual JND Prediction for 3D Point Cloud Compression</h2>
</header>

<nav>
  <a href="#home">Home</a>
  <a href="#introduction">Introduction</a>
  <a href="#dataset">Dataset</a>
  <a href="#tasks">Tasks</a>
  <a href="#evaluation">Evaluation</a>
  <a href="#submission">Submission</a>
  <a href="#dates">Dates</a>
  <a href="#organizers">Organizers</a>
</nav>

<div class="container">

<section id="home">
  <h2>Home</h2>
  <p>
    This Grand Challenge focuses on <strong>Just Noticeable Difference (JND)</strong>
    modeling for perceptual quality assessment in <strong>3D point cloud compression</strong>.
    The challenge promotes human-centric perceptual modeling and perceptually optimized
    compression techniques.
  </p>
</section>

<section id="introduction">
  <h2>Introduction</h2>
  <p>
    Point clouds are a fundamental 3D representation for immersive media, autonomous driving,
    digital twins, AR/VR, and telepresence. In practical systems, compression is unavoidable,
    leading to perceptual quality degradation.
  </p>
  <p>
    Just Noticeable Difference (JND) characterizes the minimum distortion level that becomes
    perceptible to human observers. Accurate JND modeling enables perceptually optimized
    compression by removing imperceptible redundancies while preserving visually critical
    information.
  </p>
  <p>
    JND modeling for point clouds is challenging due to irregular spatial distributions,
    complex geometry, varying densities, and rich attributes such as color.
  </p>
</section>

<section id="dataset">
  <h2>Dataset: PKU-JND</h2>
  <ul>
    <li>230 reference point cloud models across 5 content categories</li>
    <li>5,750 geometry-distorted samples</li>
    <li>7,130 attribute-distorted samples</li>
    <li>Distortions generated using MPEG G-PCC</li>
    <li>Subjective experiments with 20–31 participants</li>
  </ul>

  <div class="note">
    Dataset download links will be released with the official challenge announcement.
  </div>
</section>

<section id="tasks">
  <h2>Tasks</h2>
  <p>
    Participants are invited to develop algorithms to predict subjective JND thresholds
    for compressed point clouds, including:
  </p>
  <ul>
    <li>Geometry JND prediction</li>
    <li>Attribute (color) JND prediction</li>
    <li>Unified perceptual JND modeling</li>
  </ul>
</section>

<section id="evaluation">
  <h2>Evaluation</h2>
  <p>
    Submissions will be evaluated on a held-out test set using correlation-based and
    error-based metrics:
  </p>

  <ul>
    <li>Pearson Linear Correlation Coefficient (PLCC)</li>
    <li>Spearman Rank-Order Correlation Coefficient (SRCC)</li>
    <li>Kendall Rank Correlation Coefficient (KRCC)</li>
    <li>Root Mean Squared Error (RMSE)</li>
  </ul>

  <p>
    Final ranking score:
    $$\text{Score} = \frac{\text{PLCC} + \text{SRCC}}{2}$$
  </p>

  <div class="note">
    Participants must use only the official training data. External data usage is prohibited.
  </div>
</section>

<section id="submission">
  <h2>Submission</h2>
  <p>
    Participants must submit predicted JND values for the official test set in the provided
    JSON format. Each team may submit up to three results per day.
  </p>

  <div class="note">
    The official competition platform and submission instructions will be announced.
  </div>
</section>

<section id="dates">
  <h2>Challenge Dates</h2>
  <table>
    <tr><th>Event</th><th>Date (UTC)</th></tr>
    <tr><td>Registration Open</td><td>2026-02-15</td></tr>
    <tr><td>Training Data Release</td><td>2026-03-10</td></tr>
    <tr><td>Result Submission Deadline</td><td>2026-04-25</td></tr>
    <tr><td>Technical Paper Deadline</td><td>2026-05-10</td></tr>
    <tr><td>Final Decisions</td><td>2026-05-15</td></tr>
    <tr><td>Camera Ready Deadline</td><td>2026-05-25</td></tr>
  </table>
</section>

<section id="organizers">
  <h2>Organizers</h2>
  <ul>
    <li>Liang Xie – Guangdong University of Technology (LXie5201@outlook.com)</li>
    <li>Wei Gao – Peking University, Shenzhen (gaowei262@pku.edu.cn)</li>
    <li>Ge Li – Peking University, Shenzhen (geli@pku.edu.cn)</li>
    <li>Yanting Li – Guangdong University of Technology (1209847234@qq.com)</li>
  </ul>
</section>

</div>

<footer>
  © ICME 2026 Grand Challenge – JND Prediction for Point Cloud Compression
</footer>

</body>
</html>
