// Array de fuentes disponibles
const fonts = [
    "Arial",
    "Verdana",
    "Helvetica",
    "Georgia",
    "Times New Roman",
    "Courier New",
    "Tahoma",
    "Trebuchet MS"
];

// Función para cargar las opciones de fuente en el select
function loadFonts() {
    const fontSelect = document.getElementById('fontSelect');
    fonts.forEach(font => {
        const option = document.createElement('option');
        option.text = font;
        fontSelect.add(option);
    });
}

// Función para cambiar la fuente del texto
function changeFont() {
    const selectedFont = document.getElementById('fontSelect').value;
    const inputText = document.getElementById('inputText').value;
    const textDisplay = document.getElementById('textDisplay');
    textDisplay.style.fontFamily = selectedFont;
    textDisplay.textContent = inputText;
}

// Llamada a la función para cargar las fuentes al cargar la página
window.onload = loadFonts;
