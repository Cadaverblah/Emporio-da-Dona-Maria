# Empório-da-Dona-Clara

Projeto universitário de análise de caso e resolução do mesmo. O foco dessa atividade é compreender os problemas e dores de um cliente, e adaptá-los da melhor forma de acordo com a nossa interpretação.

Feito para a disciplina de Design Profissional (Produção de Portfólio & Desenvolvimento Empresarial), Estudo de Caso 1: Panificadora & Empório Dona Clara.

- Para usar o código: apenas baixe o zip e abra o index
- Licença MIT

---

## O caso (briefing)

A Dona Clara é uma panificadora artesanal de bairro com 12 anos de estrada, fundada por Clara Ramos e o marido, Roberto. É conhecida pelos pães de fermentação natural e pelos produtos coloniais, e sempre vendeu no balcão, com aquele clima de casa e o movimento cheio no café da manhã e no fim da tarde. A empresa é só do casal (Clara na produção, Roberto no financeiro) e tem 2 padeiros, 1 confeiteira e 3 atendentes de balcão.

O problema é que o bairro mudou:

- muita gente trabalha em home office, sai em horários alternativos e quer a conveniência de garantir o pão ou a encomenda sem pegar fila e sem o risco de chegar e estar esgotado;
- as encomendas de bolos e tábuas de frios para eventos ainda são anotadas no caderno da cozinha, e isso gera erro: atraso e troca de sabor;
- duas redes de padarias gourmet com forte presença digital abriram num raio de 2 km, e a Dona Clara está perdendo venda para elas;
- sem um canal digital, a padaria também não alcança moradores novos nem empresas da região que procuram coffee break;
- o casal sabe que precisa de uma solução digital, mas não sabe por onde começar.

## solução

Um **site MINIMALISTA UAU** (institucional + cardápio) onde cada produto tem um botão que abre o **WhatsApp com a mensagem de pedido já montada**. O cliente só completa os campos (sabor, quantidade, data, horário, nome) e a Dona Clara recebe tudo padronizado, em vez de anotação solta no caderno.

### Por que site, e não app ou sistema?

EU tinha liberdade pra escolher entre app, site ou sistema/dashboard. Escolhi o site porque:

- **App:** o cliente teria que baixar um aplicativo só pra pedir pão, e isso é uma barreira grande pra uma padaria de bairro. Ainda teria loja de apps, atualização e manutenção.
- **Sistema/dashboard:** ajudaria no controle interno, mas a dor principal é o cliente conseguir pedir de um jeito fácil. Além disso, um sistema pesado exigiria treinar a equipe toda e o casal nem sabe por onde começar.
- **Site:** abre por link em qualquer celular, pode ser achado no Google e divulgado no Instagram (o que ajuda a competir com as redes gourmet), tem custo praticamente zero e é um primeiro passo simples.
- **WhatsApp como canal de pedido:** é um app que a maioria das pessoas já tem no celular, e a mensagem pronta já pede as informações que mais deram erro nas encomendas.

### Dor do cliente x o que a gente fez

| Dor | Como o site resolve |
| --- | --- |
| Encomendas anotadas no caderno, com erro de sabor e atraso | Mensagem pronta por categoria, com os campos obrigatórios, e confirmação por escrito de tudo que foi combinado |
| Fila e risco de o produto esgotar | Pedido feito antes, com "Retirada expressa": o pedido fica separado, no nome do cliente, esperando |
| Clientes em home office e com horário alternativo | Encomenda pelo celular a qualquer hora, com retirada no balcão ou entrega |
| Perda de venda para as redes gourmet digitais | Presença online com a identidade da marca (tradição e qualidade artesanal) |
| Não alcança moradores novos e empresas | Seção de coffee break com pedido de orçamento, pensada pra reuniões e eventos |
| Casal não sabe por onde começar | Solução simples, que não exige sistema novo nem treinamento pesado |

## Telas

O site é uma página única com menu fixo no topo. As seções são:

| Seção | O que tem |
| --- | --- |
| Cabeçalho | Logo circular com o nome "Empório Dona Clara" em texto curvado, com faixas marrons em cima e embaixo |
| Menu | Fixo no topo, com links para Início, Cardápio, Como encomendar, Coffee break, Sobre e Contato |
| Início | Selo "Panificadora artesanal há 12 anos", chamada principal, botões "Encomendar pelo WhatsApp" e "Ver cardápio" e a imagem do pão |
| Cardápio | 4 cartões: pães artesanais, produtos coloniais, bolos e doces artesanais e tábuas de frios. Cada botão "Encomendar" abre o WhatsApp com a mensagem daquela categoria |
| Como encomendar | 4 passos (escolha, complete, receba a confirmação, retire) e o cartão "Retirada expressa" |
| Coffee break | Chamada para empresas e botão "Pedir orçamento", com mensagem pedindo empresa, número de pessoas, data, local e contato |
| Sobre | A história dos 12 anos da padaria e os números da equipe |
| Contato (rodapé) | Endereço, telefone, WhatsApp, horários de funcionamento e redes sociais |

<!--
Prints das telas: coloque as imagens numa pasta (ex: img/prints/) e descomente as linhas abaixo.

![Tela inicial](./img/prints/inicio.png)
![Cardápio](./img/prints/cardapio.png)
![Como encomendar e coffee break](./img/prints/encomendar.png)
-->

O visual usa as cores do próprio empório: azul `#0F4E77`, amarelo `#FBD271`, marrom `#372516` e creme `#fdf6e9`. Os títulos usam a fonte Kavoon, os títulos dos cartões e do rodapé usam a Gabriela, e o texto corrido fica em Arial.

## Arquitetura

Site estático. Não tem backend, não tem banco de dados e não precisa de build.

- **HTML5**: estrutura da página
- **CSS3**: estilo próprio em `css/stylesheet.css`
- **Bootstrap 5.3.8**: grid e responsividade (via CDN, com verificação de integridade)
- **Google Fonts**: Gabriela e Kavoon
- **Imagens**: ilustrações em SVG e uma em PNG
- **WhatsApp**: links `wa.me` com a mensagem de pedido já codificada na URL

```
Emporio-da-Dona-Clara/
├── index.html
├── css/
│   └── stylesheet.css
├── img/
│   ├── bread.svg
│   ├── qjo.svg
│   ├── CAKE.svg
│   ├── chesse2.png
│   ├── car-racing.svg
│   ├── veio-cafe.svg
│   └── ftasskid.svg
├── LICENSE
└── README.md
```

## Como executar

1. Clique em **Code > Download ZIP** aqui no GitHub e extraia a pasta.
2. Abra o arquivo `index.html` no navegador.

Pronto. Não precisa instalar nada, nem npm, nem servidor. Só precisa de internet, porque o Bootstrap e as fontes vêm de CDN.

### Antes de usar de verdade

O telefone, o endereço e as redes sociais do site são **dados de exemplo**. Pra usar de verdade, troque no `index.html`:

- o número `5541900000000` (aparece nos links do WhatsApp e no telefone do rodapé);
- o endereço, os horários e os links do Instagram e do Facebook no rodapé.

## Segurança

Nenhuma credencial, senha, token ou chave de API no código nem no histórico de commits.

## O que ainda não tem

A dor principal de um jeito simples, então algumas coisas ficaram de fora:

- o site não mostra estoque em tempo real, então a ideia é o cliente encomendar antes, e não consultar o que ainda tem;
- não tem pagamento online;
- o pedido ainda depende de alguém da equipe responder o WhatsApp;
- o cardápio ainda não tem preços.

Os próximos passos naturais seriam cardápio com preços, pagamento por Pix e algum controle dos pedidos recebidos.

## Autor

Gabriel Rezende

## Licença

Licença MIT. Veja o arquivo [LICENSE](./LICENSE).
