async function loadContent(lang = 'it') {
    try {
        const response = await fetch('content.json');
        const data = await response.json();

        // Aggiorna i contenuti della pagina
        document.getElementById('hero-title').textContent = data[lang].hero.title;
        document.getElementById('lifehacks-title').textContent = data[lang].lifehacks.title;
        document.getElementById('work-title').textContent = data[lang].work.title;
        document.getElementById('university-title').textContent = data[lang].university.title;

        // Aggiorna le voci del menu
        document.getElementById('menu-lifehacks').textContent = data[lang].menu.lifehacks;
        document.getElementById('menu-work').textContent = data[lang].menu.work;
        document.getElementById('menu-university').textContent = data[lang].menu.university;
        document.getElementById('menu-curiosity').textContent = data[lang].menu.curiosity;
        document.getElementById('menu-news').textContent = data[lang].menu.news;
        document.getElementById('menu-about').textContent = data[lang].menu.about;
    } catch (error) {
        console.error("Errore nel caricamento dei contenuti:", error);
    }
}

// Cambia lingua e ricarica i contenuti
function changeLanguage() {
    const selectedLang = document.getElementById('language-select').value;
    loadContent(selectedLang);
}

// Carica la lingua predefinita al caricamento della pagina
document.addEventListener('DOMContentLoaded', () => loadContent());

// Funzione per attivare/disattivare la modalità scura
function toggleDarkMode() {
    document.body.classList.toggle("dark-mode");
}

// Funzione per mostrare/nascondere il menu laterale
function toggleMenuSidebar() {
    const sidebar = document.getElementById("menuSidebar");
    const isDisplayed = sidebar.style.display === "block";
    sidebar.style.display = isDisplayed ? "none" : "block";
}

// Funzione per mostrare/nascondere la barra di ricerca
function toggleSearchBar() {
    const searchBar = document.getElementById("searchBar");
    const isDisplayed = searchBar.style.display === "block";
    searchBar.style.display = isDisplayed ? "none" : "block";
}

// Aggiunta degli Event Listener
document.querySelector(".menu-icon").addEventListener("click", toggleMenuSidebar);
document.querySelector(".search-icon").addEventListener("click", toggleSearchBar);
