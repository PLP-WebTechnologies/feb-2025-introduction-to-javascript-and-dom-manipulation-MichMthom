
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic DOM Manipulation</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1 id="title">Dynamic DOM Manipulation</h1>
    </header>
    <main>
        <p id="paragraph">This is a paragraph of text.</p>
        <button id="change-text-btn">Change Text</button>
        <button id="change-style-btn">Change Style</button>
        <button id="add-element-btn">Add Element</button>
        <button id="remove-element-btn">Remove Element</button>
        <div id="dynamic-element"></div>
    </main>
    <script src="script.js"></script>
</body>
</html>


// Get elements
const titleElement = document.getElementById('title');
const paragraphElement = document.getElementById('paragraph');
const changeTextBtn = document.getElementById('change-text-btn');
const changeStyleBtn = document.getElementById('change-style-btn');
const addElementBtn = document.getElementById('add-element-btn');
const removeElementBtn = document.getElementById('remove-element-btn');
const dynamicElement = document.getElementById('dynamic-element');

// Add event listeners
changeTextBtn.addEventListener('click', changeText);
changeStyleBtn.addEventListener('click', changeStyle);
addElementBtn.addEventListener('click', addElement);
removeElementBtn.addEventListener('click', removeElement);

// Functions
function changeText() {
    paragraphElement.textContent = 'New text content!';
}

function changeStyle() {
    titleElement.style.color = 'blue';
}

function addElement() {
    const newElement = document.createElement('p');
    newElement.textContent = 'New element added!';
    dynamicElement.appendChild(newElement);
}

function removeElement() {
    dynamicElement.removeChild(dynamicElement.lastChild);
}


styles.css (optional)

body {
    font-family: Arial, sans-serif;
}

header {
    background-color: #f0f0f0;
    padding: 20px;
    text-align: center;
}

main {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
}

button {
    margin-bottom: 10px;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    background-color: #4CAF50;
    color: #fff;
    cursor: pointer;
}

button:hover {
    background-color: #3e8e41;
}



