# jogo-RPG
jogo rpg em javascript 
<script>
    function portaMisteriosa() {
        alert("Você entrou em uma sala");

        alert("Você encontrou um baú misterioso e nesse baú havia 3 itens: uma espada longa e dourada, uma armadura linda e reluzente como as estrelas, e um pequeno cogomelo misterioso vermelho com bolinhas brancas");

        let escolhaItem = prompt("Ao abrir o baú, qual item você gostaria de pegar:\n1 - Espada longa e dourada\n2 - Armadura linda e reluzente com pedras de diamante brilhosas\n3 - Um pequeno cogomelo misterioso vermelho com bolinhas brancas");

        while (escolhaItem < 1 || escolhaItem > 3) {
            escolhaItem = prompt("Escolha um item válido, senão você ficará sem nada:\n1 - Espada longa e dourada\n2 - Armadura linda e reluzente como as estrelas\n3 - Um pequeno cogomelo misterioso vermelho com bolinhas brancas muito suspeito");
        }

        alert("Ao escolher o item, todo baú se fechou e você não conseguiu mais abrir ele para pegar o restante dos itens");

        return escolhaItem;
    }

    function corredorEscuro() {
        let escolha = prompt("Você decidiu ir até o corredor escuro. Andando mais à frente, você se depara com um 'pequeno slime' misterioso. Quando ele se depara com você, ele começa a gritar: 'Você não vai passar pelo slime, slime vai impedir você'\n1 - Sair correndo\n2 - Chorar\n3 - Sacar sua espada");

        if (escolha == '3') {
            alert("O slime começou a vir correndo em sua direção. Você sacou sua arma e foi de frente com ele para eliminar o pequeno slime");

            let danoSlime = 15;
            let defSlime = 10;
            let vidaSlime = 20;

            let danoJogador = atkJogador - defSlime;
            vidaSlime -= danoJogador;

            let danoSlimeAoJogador = danoSlime - defJogador;
            if (danoSlimeAoJogador > 0) {
                vidaJogador -= danoSlimeAoJogador;
                alert("O slime deu " + danoSlimeAoJogador + " de dano em " + nome);
                alert("voce acaba ficando com " + vidaJogador + " de vida");
                alert("logo apos de " + nome + " tomar 5 de dano, ele toma coragem e revida o atak dando " + atkJogador + " de dano no slime");
                vidaSlime = vidaSlime - atkJogador
                if (vidaSlime < 0) {
                    vidaSlime = 0
                }
                alert("O slime acaba ficando com " + vidaSlime + " de vida e acaba morrendo")
            } else {
                alert("O slime não conseguiu dar dano em " + nome);
            }

            if (vidaSlime <= 0 || vidaJogador <= 0) {
                alert(vidaSlime <= 0 ? "Parabens você acabou de derrotar o slime!" : "Você foi derrotado pelo slime.");
                alert("Logo apos de " + nome + "  ter travdo uma briga tensa com o islime ele acaba conseguindo recuperar a sua vida como estava entes,  e ápos isso " + nome + " retorna para o corredor escuro com sua espada dourada")


                while (true) {
                    tocha = prompt("Andando em diante no corredor escuro " + nome + " acaba achando uma tocha🔥" + nome + " decide pegar a tocha para ver o caminho melhor ou seguir em diante? \n1-sim \n2-não")

                    if (tocha == "1") {

                        alert("Após " + nome + " pegar a tocha ele acaba vendo um buraco grande e acaba desviando")
                        break;

                    } else if (tocha == "2") {
                        alert("Após " + nome + " não pegar a tocha e seguir em diante acaba caindo em um boraco grande e fundo e morre");
                        acabar()
                    }

                }
                // e decide pegar para ver melhor o caminho e os perigos afrente

                alert("Após uma boa caminhada " + nome + " acaba achando uma pequena luz no corredor e acaba saindo correndo para o fim do corredor assim que " + nome + " vai se aproximando, Vai percebendo que tem algo de errado, áte que...")
                alert(nome + " acaba se deparando com uma  aranha enorme e gigante que gritava " + nome + " VOU TE PEGARRRRR!!!")


                while (true) {
                    correr = prompt("logo em diante, a aranha gigante corre em sua direção voce deseja desviar ou continuar como um bravo cavaleiro \n1-desviar \n2-continuar como um cavaleiro")

                    if (correr == "1") {

                        alert("Após " + nome + " deviar da sua teia ele acaba sobrevivendo")
                        alert("logo em seguida " + nome + " acaba vendo uma grande oportunidade de cortar uma perna da aranha")


                    } else if (correr == "2") {
                        alert("Após " + nome + " continuar como um cavaleiro acaba morendo facilmente para a aranha");
                        acabar()
                    }

                    while (true) {
                        bater = prompt("você decide cortar a perna da aranha? \n1-cortar a perna da aranha \n2-não cortar a perna da aranha ")

                        if (bater == "1") {

                            alert("ápos " + nome + " arrancar uma perna da aranha ela acaba ficando com " + atkJogador + " de vida");

                        } else if (bater == "2") {

                            alert("ápos " + nome + " optar por nao querer arrancar a perna da aranha, ela acaba virando rapidamente e destroça a acabeça dele  ");
                            saida()


                        }

                        alert("logo em seguida a aranha recua sentindo muita dor")
                        alert("ápos um tempo os dois se emcarando, " + nome + " toma uma iniciativa e vai para cima da aranha com toda sua força, a aranha acaba vendo uma boa oportunidade de atakar " + nome + " e consegue gerar um dano quase grave em " + nome + ", ápos isso " + nome + " acaba ficando com " + vidaJogador + " de vida")

                        alert("Agora ambos estão com bem pouco de vida quase um hit de dano...")
                        alert(" a aranha vem correndo loucamente em sua direçao literalmente se inportando com nada, agora " + nome + " precisa tomar uma decisão, uma que vai decidir sua vida... ")

                        while (true) {
                            decisao = prompt("Oque você decide? (importante! sua resposta vai ser decisiva) \n1-ficar na reta da aranha \n2-tentar achar uma escapatoria para correr da aranha")


                            if (decisao == 1) {
                                alert("ápos " + nome + " ficar na reta da aranha e encarar a morte,  e logo em seguida levantar sua espada na reta da cabeça da aranha ele surpreendentemente acaba com a vida da aranha deixando a espada cravada na cabeça da aranha conseguindo derrotar-la, e logo em seguida consegue ver o fecho de luz no fim do corredor e saindo como um bravo cavalheiro ")
                            }
                            else if (decisao == 2) {
                                alert("ápos " + nome + " tentar achar uma escapatoria acaba sendo só uma presa dentre varias outras que tentou correr do seu medo...");
                                morreu()
                            }

                            alert("Parabens apos você conseguiu finalizar o jogo :) ")


                        }
                    }


                }

                alert("voce decide cortatr a perna da aranha ")

                alert("lkrgbçragbçoiuvqgeriufqwebsfiurbfiqrgfi9igufiur")

                return; // Termina a função se o jogo acabou
            }
        } else if (escolha == '1' || escolha == '2') {
            alert("voce acaba saindo correndo para a porta misteriosa com medo do slime");
            portaMisteriosa()
        }
    }

    let nome = '';
    let atkJogador = 15;
    let defJogador = 10;
    let vidaJogador = 30;

    nome = prompt("Olá jovem aventureiro, qual é o seu nome?");
    alert(nome + " seja bem-vindo a caverna do jabuti 🔥");

    alert("Você caiu em um buraco e ao se levantar, você se deparou com a seguinte escolha: ao seu lado direito você nota uma porta grande com madeira avermelhada e com aspecto de velha, caindo aos pedaços; e do lado esquerdo você nota um corredor longo e escuro, sem conseguir ver o final");

    let escolha = prompt("Qual vai ser sua decisão❓:\n1 - Você escolhe seguir à direita (porta misteriosa)\n2 - Você escolhe seguir à esquerda (corredor escuro)");

    if (escolha == "1") {
        let item = portaMisteriosa();
        if (item == 1) {
            atkJogador += 5;
            alert("Ao segurar a espada, você sente uma força de vontade percorrendo seu corpo com a sabedoria e destreza do rei antigo");
        } else if (item == 2) {
            defJogador += 10;
            alert("Ao vestir a armadura, você sente um cosmo entrando em seu corpo com as almas do submundo e fica paralizado com a tamnha forca, pois " + nome + " não é capas de aguentar tantos poderes do submundo e pela ganância ");
            nobru();
        } else if (item == 3) {
            vidaJogador += 30;
            alert("Você consumiu o cogomelo (você é doido comendo coisas achadas assim do nada). Você sente como se tivesse duplicado de tamanho");
        }

        alert('Você sente sua força aumentando\n\nAtaque: ' + atkJogador + '\nDefesa: ' + defJogador + '\nVida: ' + vidaJogador);

        corredorEscuro();
    } else if (escolha == "2") {
        while (vidaJogador > 0) {
            corredorEscuro();
            if (vidaJogador <= 0) {
                alert("Você foi derrotado.");
                break; // Sai do loop se o jogador for derrotado
            }
        }
    }

    function aranha01() {
        var vidaAranha = 50
        var defAranha = 10
        var atkAranha = 15
    }
</script>
