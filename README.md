
//animation au scroll code principal

const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
        if (entry.isIntersecting) {
            entry.target.classList.add('show');
        } else {
            entry.target.classList.remove('show');
        }
    })
})


// animation au scroll code pour sélectionner les divers éléments
const elements = document.querySelectorAll('.hidden');
const hiddenElementsmax = document.querySelectorAll('.hidden_max');


// animation au scroll code pour exécuter l'animation sur les divers éléments sélectionnés
elements.forEach(element => {
    observer.observe(element);
})
hiddenElementsmax.forEach(element => {
    observer.observe(element);
})

// code css associé

.hidden {
    opacity: 0;
    transform: translateX(-100%);
}

.hidden_max {
    opacity: 0;
    transform: translateX(100%);
}

.show {
    opacity: 1;
    transform: none;
    transition: opacity 1s ease-in-out, transform 1s ease-in-out;
}

// dans le html je donne juste les classes .hidden et .hidden_max aux blocs associés


const header = document.querySelector('header');

window.addEventListener('scroll', () => {
    if (window.scrollY > 0) {
        header.classList.add('fixed');
    } else {
        header.classList.remove('fixed');
    }
});

// end animation fixed header on scroll page


Une API
Un WebSocket SOAP Restful JRPC etc
système design