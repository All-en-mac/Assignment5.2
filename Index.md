HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Selectors Practice</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header Section -->
    <header>
        <h1>CSS Selectors Mastery</h1>
        <p>Practicing element, class, ID, universal, grouping, and specificity rules.</p>
    </header>

    <main>
        <!-- Specific ID Section -->
        <section id="featured-section">
            <h2>Featured Section</h2>
            <p>This paragraph is inside an element styled specifically via an ID selector.</p>
        </section>

        <!-- Class Selector Cards -->
        <section class="card-container">
            <div class="card">
                <h3>Card One</h3>
                <p>This card shares a common class selector for consistent layout styling.</p>
            </div>
            <div class="card">
                <h3>Card Two</h3>
                <p>This card shares the exact same class selector, ensuring modular design.</p>
            </div>
        </section>

        <!-- Specificity & Cascade Demonstration Section -->
        <section>
            <h2>Specificity Test</h2>
            <!-- This paragraph will demonstrate conflicting rules -->
            <p class="special-text" id="demo-text">
                This text demonstrates CSS cascade and specificity rules in action!
            </p>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Web Development Practice</p>
    </footer>

</body>
</html>

CSS
/* 1. Universal Selector (*) */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

/* 2. Element Selector */
body {
    font-family: Arial, sans-serif;
    background-color: #f9f9f9;
    color: #333333;
    line-height: 1.6;
    padding: 20px;
}

/* 3. Grouping Selector */
h1, h2, h3 {
    color: #2c3e50;
    margin-bottom: 10px;
}

/* 4. Class Selector (.card) */
.card-container {
    display: flex;
    gap: 20px;
    margin: 20px 0;
}

.card {
    background-color: #ffffff;
    border: 1px solid #e0e0e0;
    padding: 20px;
    border-radius: 8px;
    flex: 1;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

/* 5. ID Selector (#featured-section) */
#featured-section {
    background-color: #e8f4fd;
    border-left: 5px solid #2980b9;
    padding: 20px;
    border-radius: 4px;
    margin-bottom: 20px;
}

/* 6. Conflicting Rules (Cascade & Specificity Demonstration) */
/* Rule A: Class Selector */
.special-text {
    color: green;
    font-size: 16px;
}

/* Rule B: ID Selector (Higher Specificity overrides Rule A's color) */
#demo-text {
    color: crimson;
    font-weight: bold;
}