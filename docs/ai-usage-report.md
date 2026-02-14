# Tools Used & Use Cases

During this assignment, I used one AI tool primarily as supporting tool to enhance my workflow, problem-solving process, and design decisions, while all final implementation and design choices were my own.

## `ChatGPT`

ChatGPT was used as the main AI assistant during the project. Its use cases included:

- **Code generation & debugging:**
I used ChatGPT to help debug HTML, CSS, and JavaScript issues, such as layout problems, styling conflicts, and minor logic errors.

- **Code review & explanations:**
ChatGPT helped explain certain CSS and JavaScript concepts (e.g., flexbox behavior, animations, and styling structure), which supported my understanding before applying changes manually.

- **Documentation support:**
It assisted in structuring documentation sections (how to add pictures, organize content) and improving clarity and organization of explanations.

- **UI/UX design suggestions:**
ChatGPT provided minor UI/UX suggestions, such as spacing improvements, color contrast ideas, and hover/interaction enhancements. The final visual design, layout, and theme decisions were entirely my own.

## ChatGPT's detailed help
## 1. HTML
I wanted to add icons for the skills, AI assisted in adding an external icon library by suggesting the correct CDN link for Font Awesome. This allowed me to include icons in the Skills section to improve visual clarity and UI presentation.
  
```html 
  <!-- for icons ( I used AI help here) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">  
```
This is the `skills section` after the suggestion 
```html
<!--  SKILLS  -->
<section id="skills">
    <h2>Skills</h2>
<!-- UI/UX design suggestions from AI -->
    <div class="skills-grid">
        <div class="skill">
            <i class="fa-brands fa-html5"></i>
            <span>HTML</span>
        </div>

        <div class="skill">
            <i class="fa-brands fa-css3-alt"></i>
            <span>CSS</span>
        </div>

        <div class="skill">
            <i class="fa-brands fa-js"></i>
            <span>JavaScript</span>
        </div>

        <div class="skill">
            <i class="fa-brands fa-github"></i>
            <span>GitHub</span>
        </div>

        <div class="skill">
            <i class="fa-solid fa-pen-nib"></i>
            <span>UI Design</span>
        </div>
    </div>
</section>
```
The skill section after this suggestion 

![skilss](https://github.com/user-attachments/assets/f5de1264-9b2e-4088-9974-0c6e969652a8)

AI also helped in design, the background design was initially simple and static. 
After exploring portfolio examples, I chose to add an animated stars background to enhance visual appeal. 
AI assisted with the performing the idea and initial guidance, while the final implementation and styling decisions were done manually. Further details are explained in the `CSS section`.

```html
<!-- Stars background ( this was the designs idea , guided by ai help , UI/UX design suggestions) -->
<div class="stars"></div>
```
finally, AI helped me understand how to implement a dark/light mode toggle using JavaScript, including the logic behind theme switching and button interaction. The final implementation and customization were done manually. Further details are explained in the `JavaScript section`.

```html
<!-- Theme toggle button (  JavaScript feature) -->
 <button id="theme-toggle">🌙 Dark</button>
```
## 2. JavaScript
AI helped me understand how to structure a JavaScript function that controls theme switching.

Specifically, AI explained how a single function can be used to:

- Apply the selected theme to the document using a data attribute

- Update the button text dynamically based on the current theme

After understanding the logic, I adapted the function to fit my portfolio structure and UI requirements. This helped me better understand JavaScript functions, DOM manipulation, and state persistence.

```JavaScript
 function applyTheme(theme) {
    root.setAttribute("data-theme", theme);
    localStorage.setItem("theme", theme);
    themeToggle.textContent = theme === "dark" ? "☀️ Light" : "🌙 Dark";
  }
```
## 3. CSS
AI helped me conceptually in designing the animated stars background by explaining how CSS gradients and keyframe animations can be combined to create visual effects without using images or external libraries.

Specifically, it guided me to:

- Use multiple radial-gradient() layers to simulate stars at different positions and sizes.

- Apply position: fixed and z-index to keep the stars in the background without affecting page content.

- Use @keyframes with transform: translate() to create slow, smooth background movement.

- Adjust properties such as opacity, background-size, and animation duration to keep the effect subtle and non-distracting.

The idea and visual direction (adding stars to make the background more appealing instead of a plain color) were my own design choice after reviewing portfolio examples. AI support was mainly used to understand the CSS techniques and experiment with values, while the final styling, colors, timing, and layout decisions were manually refined by me.

```CSS
/*  STARS BACKGROUND - AI help */
.stars {
    position: fixed;
    inset: 0;
    background: 
    radial-gradient(5px 5px at 20% 30%, white, transparent),
    radial-gradient(6px 6px at 80% 70%, #c7d2fe, transparent),
    radial-gradient(7px 7px at 50% 50%, white, transparent),
    radial-gradient(5px 5px at 10% 80%, #e0e7ff, transparent),
    radial-gradient(6px 6px at 90% 20%, #a5b4fc, transparent),
    radial-gradient(5px 5px at 30% 60%, white, transparent);

        
    background-size: 300px 300px;
    animation: starsMove 80s linear infinite;
    opacity: 0.35;
    z-index: -1;
}

@keyframes starsMove {
    from { transform: translateY(0); }
    to { transform: translateY(-1200px); }
}
```

Also, AI helped me understand how I can change the website colors when clicking a Light or Dark mode button. At first, I didn’t understand how a button could control the entire website design. The AI explained that this can be done by changing a `data-theme` attribute using JavaScript, and then letting CSS automatically apply different colors based on that value.

Through this help, I learned how to switch between light and dark modes without rewriting the design, and how CSS reacts instantly when the theme changes. This made it much easier for me to control the website appearance and improve the user experience.

```CSS
/*  LIGHT MODE (AI Help)  */
/* Light mode */
[data-theme="light"] body {
  background: #ffffff;
  color: #020617;
}

/* Dark mode  */
[data-theme="dark"] body {
  background: #020617;
  color: #e5e7eb;
}


[data-theme="light"] .stars {
  display: none;
}

[data-theme="dark"] .stars {
  display: block;
}
```

## Benefits

- Improved efficiency when debugging styling and layout issues.

- Helped clarify CSS concepts related to positioning, responsiveness, and animations.

- Provided useful UI/UX suggestions that helped refine the visual quality of the portfolio.

- Supported clearer and more structured documentation writing.

## Challenges

- Some AI-generated suggestions required adjustment to better fit the project’s design goals.

- Not all generated code was optimal or directly usable, especially for styling and animations.

- Required careful review to ensure solutions aligned with course requirements and best practices.

## Learning Outcomes

Through using AI tools in this assignment, I learned:

How to better structure and debug HTML, CSS, and basic JavaScript code.

How to evaluate UI/UX suggestions critically instead of applying them blindly.

Improved understanding of layout techniques (Flexbox/Grid) and styling decisions.

How to integrate AI tools effectively as learning and support tools, not replacements for my own problem-solving.

## Responsible Use & Modifications

All AI-generated suggestions were carefully reviewed and modified before use.
I ensured:

- The final code and design decisions were my own work.

- AI suggestions were adapted, rewritten, or partially used rather than copied directly.

- The project maintains originality, correctness, and academic integrity.

- AI tools were used only to support learning, debugging, and refinement, not to fully generate the project.
