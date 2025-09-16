# Electronic Urn (Urna Eletrônica)

Este projeto é uma simulação de uma urna eletrônica brasileira, desenvolvida com HTML, CSS e JavaScript puro. A aplicação permite ao usuário votar em candidatos para diferentes cargos, seguindo um fluxo de etapas pré-definidas.

O projeto demonstra a manipulação do DOM, gerenciamento de estado (etapas de votação) e o uso de dados estruturados em JavaScript para popular a interface.

## Funcionalidades

  * **Interface de Votação:** Recria visualmente a tela e o teclado de uma urna eletrônica, incluindo a animação de "pisca" para a entrada de números.
  * **Etapas de Votação:** O fluxo de votação é controlado por um array de etapas no arquivo `etapas.js`. O sistema está configurado para dois turnos:
    1.  **Vereador** (5 dígitos).
    2.  **Prefeito** (2 dígitos), incluindo a exibição do vice.
  * **Carregamento Dinâmico de Candidatos:** Ao digitar um número, o script `script.js` consulta o arquivo `etapas.js` e exibe dinamicamente o nome, partido e fotos do candidato correspondente.
  * **Opções de Voto:** O usuário pode:
      * **Votar em um candidato:** Digitando os números e apertando "CONFIRMA".
      * **Voto Nulo:** Digitar um número que não corresponde a nenhum candidato resulta em "VOTO NULO".
      * **Voto em Branco:** Apertando o botão "BRANCO".
      * **Corrigir:** Apertando "CORRIGE" para limpar a etapa atual e recomeçar.
  * **Finalização:** Após a última etapa, o sistema exibe a palavra "FIM". Os votos são armazenados em um array e logados no console.

## Estrutura do Repositório

```
/
│
├── index.html          # A estrutura HTML da urna (tela e teclado)
├── style.css           # O arquivo de estilização (layout, cores, animações)
├── etapas.js           # O "banco de dados" da eleição (define cargos e candidatos)
├── script.js           # O cérebro da aplicação (controla a lógica e o estado)
│
├── images/             # (Pasta não incluída no upload, mas referenciada)
│   ├── 84.jpg
│   ├── 84_2.jpg
│   ├── 99.jpg
│   └── ... (outras fotos de candidatos)
│
└── README.md           # Este arquivo
```

## Como Usar

1.  **Clone ou baixe o repositório.**
2.  **Crie uma pasta `images/`:** O projeto espera que as fotos dos candidatos (mencionadas em `etapas.js`, ex: `38111.jpg`, `99.jpg`) estejam dentro de uma pasta chamada `images/`. Você precisará adicionar suas próprias imagens com esses nomes.
3.  **Abra o `index.html`** em qualquer navegador web moderno para iniciar a simulação.

## Observações

  * **Separação de Responsabilidades:** O projeto é bem estruturado, separando:
      * `index.html`: Apenas a estrutura (View).
      * `style.css`: Apenas a aparência (View).
      * `etapas.js`: Apenas os dados (Model).
      * `script.js`: Apenas a lógica (Controller).
