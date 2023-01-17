# Como montar um validador de Cartão de Credito
### Com uma estrutura simples montei um codigo que valida os cartões Visa, Master Card e American Express, com JavaScript.

#### Inicio da Function
    function validarCard(cardNumber, visa, masterCard, ameExp) {

#### Criando as variaveis e montando a estrutura de verificação do numero

        const numero = cardNumber.value;

        const valVisa = /^4[0-9]{12,15}$/;
        const valMasterCard = /^5[1-5]{1}[0-9]{14}$/;
        const valAmeExp =  /^3(4|7){1}[0-9]{13}$/;

        const cardNumberArray = numero.split("");
        var reverse = cardNumberArray.reverse();

        reverse = reverse.map(Number);

        const digitto = reverse[0];

        reverse = reverse.splice(1);

#### Multiplicando valores e somando todos os valores

        for (let i = 0; i < reverse.length; i++) {
            if ((i + 1) % 2 !== 0) {
                reverse[i] = reverse[i] * 2;
                if (reverse[i] > 9) {
                    reverse[i] = reverse[i] - 9;
                }
            }
        }
        
        reverse = reverse.reduce(function(total, soma){return total + soma;});

#### Validando os dados se são verdadeiros

        if (visa.checked) {
            if (cardNumber.value.match(valVisa)) {
                if ((10 - (reverse % 10)) === digitto){
                    console.log("True - Nº Cartão");
                    visa.setCustomValidity('');
                    masterCard.setCustomValidity('');
                    ameExp.setCustomValidity('');
                    cardNumber.setCustomValidity('');
                } else {
                    visa.setCustomValidity('');
                    masterCard.setCustomValidity('');
                    ameExp.setCustomValidity('');
                    cardNumber.setCustomValidity('Numero de Cartão invalid');
                }
            } else {
                visa.setCustomValidity('Numero do cartão não confere com a bandeira');
                masterCard.setCustomValidity('');
                ameExp.setCustomValidity('')
                cardNumber.setCustomValidity('');
            }
        } else if (masterCard.checked) {
            if (cardNumber.value.match(valMasterCard)) {
                if ((10 - (reverse % 10)) === digitto){
                    console.log("True - Nº Cartão");
                    visa.setCustomValidity('');
                    masterCard.setCustomValidity('');
                    ameExp.setCustomValidity('');
                    cardNumber.setCustomValidity('');
                } else {
                    visa.setCustomValidity('');
                    masterCard.setCustomValidity('');
                    ameExp.setCustomValidity('');
                    cardNumber.setCustomValidity('Numero de Cartão invalid');
                }
            } else {
                visa.setCustomValidity('');
                masterCard.setCustomValidity('Numero do cartão não confere com a bandeira');
                ameExp.setCustomValidity('')
                cardNumber.setCustomValidity('');
            }        
        } else if (ameExp.checked){
            if (cardNumber.value.match(valAmeExp)) {
                if ((10 - (reverse % 10)) === digitto){
                    console.log("True - Nº Cartão");
                    visa.setCustomValidity('');
                    masterCard.setCustomValidity('');
                    ameExp.setCustomValidity('');
                    cardNumber.setCustomValidity('');
                } else {
                    visa.setCustomValidity('');
                    masterCard.setCustomValidity('');
                    ameExp.setCustomValidity('');
                    cardNumber.setCustomValidity('Numero de Cartão invalid');
                }
            } else {
                visa.setCustomValidity('');
                masterCard.setCustomValidity('');
                ameExp.setCustomValidity('Numero do cartão não confere com a bandeira');
                cardNumber.setCustomValidity('');
            }
        } else {
            visa.setCustomValidity("Please select a card");
        }
#### Fim da Function        
    }