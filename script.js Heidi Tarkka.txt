// a) Muuttuja ja konsolitulostus
let nimi = "Heidi";

console.log("Tervetuloa sivulleni, " + nimi + "!");

// b) Ehtolause
let ika = 20;

if (ika >= 18) {
    console.log("Olet täysi-ikäinen.");
} else {
    console.log("Olet alaikäinen.");
}

// c) Funktio
function laskeAlv(hinta) {
    return hinta * 1.25;
}

console.log("Tuotteen hinta ALV:n kanssa: " + laskeAlv(100));

// d) Taulukko ja silmukka
const osaamisalueet = [
    "Projektijohtaminen",
    "Liiketoiminnan kehittäminen",
    "Fasilitointi",
    "Myynti"
];

osaamisalueet.forEach(function(osaaminen) {
    console.log(osaaminen);
});

function haeNeuvo() {
    fetch("https://api.adviceslip.com/advice")
        .then(response => response.json())
        .then(data => {
            console.log(data);
        })
        .catch(error => {
            console.log("Virhe:", error);
        });
}