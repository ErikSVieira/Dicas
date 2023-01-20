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

# Máscaras

### CEP
    function validarCEP(v) {
        console.log(v.value);
        // Removendo os caracteres que não forem números
        v.value = v.value.replace(/\D/g, "");
        // Adicionando o hífen na 6ª posição
        v.value = v.value.replace(/^(\d{5})(\d)/, "$1-$2");
    }

### Data
    function validarData(v) {
        v.value = v.value.replace(/\D/g, "");
        //Adiciona a barra entre o dia e o mês
        v.value = v.value.replace(/^(\d{2})(\d)/, "$1/$2");
        //Adiciona a barra entre o mês e o ano
        v.value = v.value.replace(/(\d{2})(\d)/, "$1/$2");
    }

### Telefone
    function validarTel(v) {
        v.value = v.value.replace(/\D/g, "");
        //Adiciona parênteses no DDD
        v.value = v.value.replace(/^(\d\d)(\d)/g, "($1) $2");
        //Adiciona hífen no número do telefone
        v.value = v.value.replace(/(\d{5})(\d)/, "$1-$2");
    }

### CPF
    function validarCPF(v) {
        v.value = v.value.replace(/\D/g, "");
        //Adiciona ponto após os três primeiros números
        v.value = v.value.replace(/^(\d{3})(\d)/, "$1.$2");
        //Adiciona ponto após os seis primeiros números
        v.value = v.value.replace(/(\d{3})(\d)/, "$1.$2");
        //Adiciona o hífen antes dos últimos 2 caracteres
        v.value = v.value.replace(/(\d{3})(\d{1,2})$/, "$1-$2");
    }

# Criando um Cookie em JavaSscript
### Salva o Cookie
    function setCookie(nome, valor, expira) {
        //Cria um objeto da classe data (classe nativa do javascript)
        dia = new Date();
        //Adiciona a quantidade de dias que o cookie estará válido à data atual
        dia.setDate(dia.getDate() + expira);
        //Prepara a string que armazenará o cookie
        var valor = escape(valor) + ((expira === null) ? "" : "; expires=" + dia.toUTCString());
        //Adiciona a string ao cookie
        document.cookie = nome + "=" + valor;
    }

### Verifica se  o Cookie já está salvo
    function getCookie(nome) {
        //Obtém a string com os cookies
        var cookies = document.cookie;
        //Localiza onde está o cookie cujo nome foi passado por parâmetro
        var inicio = cookies.indexOf(" " + nome + "=");
        //Se estiver no início
        if (inicio === -1) {
            //Posiciona no início do cookie
            inicio = cookies.indexOf(nome + "=");
        }
        //Ou se não foi localizado (não existe)
        if (inicio === -1) {
            cookies = null;
        } else {
            //Localiza a posição inicial onde está o valor do cookie
            inicio = cookies.indexOf("=", inicio) + 1;
            //Localiza a posição final onde está o valor do cookie
            var fim = cookies.indexof(";", inicio);
            if (fim === -1) {
                fim = cookies.length;
            }
            //Enfim, obtém o valor do cookie
            cookies = unescape(cookies.substring(inicio, fim));
        }
        //Retorna o valor
        return cookies;
    }

### Deve se validar alguns campos antes de criar o cookie
    function validarForm(form) {
        // Pode ter uma expressão regular para verificar se o email é válido (mantenha a expressão em uma linha única e contínua)
        erEmail = /^[\w!#$%&'*+\/=?^`{|}~-]+(\.[\w!#$%&'*+\/=?^`{|}~-]+)*@(([\w-]+\.)+[A-Za-z]{2,6}|\[\d{1,3}(\.\d{1,3}){3}\])$/;
        
        // Verifica se o campo está vazio ou não corresponde ao email válido

        // Verifica se a senha está correta com banco de dados
        if (form.senha.value !== "senha_do_DB") {
            alert("Preencha o campo SENHA corretamente");
            return false;
        }
        // Verifica se a opção de manter conectado foi selecionada
        if (form.conectado.checked) {
            // Em caso afirmativo, cria um cookie com o email do usuário
            setCookie("email", form.email.value, 1);
        }
        return true;
    }

### Também ao carregar a página, verificamos se o usuário já acessou o site anteriormente e optou por mantê-lo conectado.
    function verificarLogado() {
        // Verifica a existência do login
        if (getCookie("email") !== null) {
            // Em caso afirmativo, direciona para a página restrita
            window.location.href = "pagina_de_acesso.html";
        }
    }