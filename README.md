alert("Boas-vindas ao Jogo do Número Secreto!");
let numeroMaximo = 500;
let numeroSecreto = parseInt(Math.random() * numeroMaximo + 1);
let chute;
let tentativas = 1;
console.log(numeroSecreto)
while (chute != numeroSecreto) {
    chute = prompt(`Escreva um número entre 1 e ${numeroMaximo}`);
    if (chute == numeroSecreto) {
        break;
    } else if (chute > numeroSecreto) {
        alert(`O número secreto é menor que ${chute}`);
    } else {
        alert(`O número secreto é maior que ${chute}`);
        tentativas++;
    }
}
let palavraTentativa = tentativas > 1 ? "Tentativas" : "Tentativa";
alert(`Você acertou o número secreto (${numeroSecreto}) em ${tentativas} ${palavraTentativa} `);

