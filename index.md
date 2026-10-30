CSS
/* --- 1 & 2. Design Tokens / CSS Variables in :root --- */
:root {
    /* Color Palette */
    --primary-color: #2563eb;       /* Royal Blue */
    --secondary-color: #38bdf8;     /* Sky Blue */
    --bg-color: #f8fafc;            /* Light Background */
    --card-bg: #ffffff;             /* White Card Background */
    --text-color: #1e293b;          /* Dark Slate Text */
    --text-muted: #64748b;          /* Muted Gray Text */
    --accent-color: #f59e0b;        /* Amber Accent */

    /* 3. Spacing Variables */
    --space-sm: 0.5rem;             /* Small spacing (8px) */
    --space-md: 1rem;               /* Medium spacing (16px) */
    --space-lg: 2rem;               /* Large spacing (32px) */

    /* 4. Font-Size Variables */
    --font-size-sm: 0.875rem;       /* Small text (~14px) */
    --font-size-base: 1rem;         /* Base text (16px) */
    --font-size-lg: 1.25rem;        /* Large text (~20px) */
    --font-size-xl: 2rem;           /* Extra large heading (~32px) */
}

/* --- Global Reset & Usage of Base Variables --- */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: var(--bg-color);
    color: var(--text-color);
    line-height: 1.6;
    padding: var(--space-lg);
}

/* --- Header Layout --- */
header {
    text-align: center;
    margin-bottom: var(--space-lg);
}

header h1 {
    font-size: var(--font-size-xl);
    color: var(--primary-color);
    margin-bottom: var(--space-sm);
}

header p {
    font-size: var(--font-size-base);
    color: var(--text-muted);
}

/* --- Main Container --- */
.container {
    max-width: 800px;
    margin: 0 auto;
}

/* --- 5. Using Variables in Cards --- */
.design-card {
    background-color: var(--card-bg);
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    padding: var(--space-lg);
    margin-bottom: var(--space-lg);
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
}

.design-card h2 {
    font-size: var(--font-size-lg);
    color: var(--primary-color);
    margin-bottom: var(--space-md);
}

.design-card p {
    font-size: var(--font-size-base);
    color: var(--text-muted);
    margin-bottom: var(--space-md);
}

/* --- 5. Using Variables in Buttons --- */
.btn-primary {
    background-color: var(--primary-color);
    color: #ffffff;
    padding: var(--space-sm) var(--space-md);
    font-size: var(--font-size-base);
    font-weight: 600;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

.btn-primary:hover {
    background-color: var(--secondary-color);
    color: #0f172a;
}

/* --- Footer --- */
footer {
    text-align: center;
    padding-top: var(--space-md);
    font-size: var(--font-size-sm);
    color: var(--text-muted);
    border-top: 1px solid #e2e8f0;
}
File 2: design-tokens.html (Sample Webpage)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 5.4 — CSS Variables & Design Tokens</title>
    <!-- Link to Design Token Stylesheet -->
    <link rel="stylesheet" href="tokens.css">
</head>
<body>

    <div class="container">
        <!-- Header -->
        <header>
            <h1>Design Systems & Tokens</h1>
            <p>Demonstrating centralized styling using CSS custom properties (`--variables`).</p>
        </header>

        <main>
            <!-- Card Component 1 -->
            <section class="design-card">
                <h2>Primary Button Component</h2>
                <p>This card and its button inherit color, padding, and font-size variables defined globally in the <code>:root</code> block. Changing a token updates all linked elements instantly.</p>
                <button class="btn-primary">Click Me</button>
            </section>

            <!-- Card Component 2 -->
            <section class="design-card">
                <h2>Spacing & Typography Consistency</h2>
                <p>By using design tokens like <code>var(--space-lg)</code> and <code>var(--font-size-lg)</code>, layouts maintain strict proportions and visual harmony across the entire application.</p>
                <button class="btn-primary">Learn More</button>
            </section>
        </main>

        <!-- Footer -->
        <footer>
            <p>&copy; 2026 Student Design System. All rights reserved.</p>
        </footer>
    </div>

</body>
</html>