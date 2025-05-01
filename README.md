# bandeiras_GH-Copilot
Exercício para entrega da aula: Criando um Validador de Bandeiras de Cartão de Crédito com o GitHub Copilot

Utilizando o Github copilot, foi gerado o código abaixo com base na imagem do exercício:

function getBandeira(cardNumber) {
    const cardNumberStr = cardNumber.toString();

    if (cardNumberStr.startsWith('4')) {
        return 'Visa';
    } else if (/^5[1-5]/.test(cardNumberStr) || /^222[1-9]|22[3-9]\d|2[3-6]\d{2}|27[01]\d|2720/.test(cardNumberStr)) {
        return 'MasterCard';
    } else if (/^4011|4312|4389/.test(cardNumberStr)) {
        return 'Elo';
    } else if (/^34|37/.test(cardNumberStr)) {
        return 'American Express';
    } else if (/^6011|65|64[4-9]/.test(cardNumberStr)) {
        return 'Discover';
    } else if (cardNumberStr.startsWith('6062')) {
        return 'Hipercard';
    } else {
        return 'Unknown';
    }
}

// Example usage:
const cardNumber = 4111111111111111; // Replace with the card number to test
console.log(`Bandeira: ${getBandeira(cardNumber)}`);
