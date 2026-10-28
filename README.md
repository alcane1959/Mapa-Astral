# Mapa Astral

Aplicação web em arquivo único para geração de um estudo simbólico de mapa astral e numerologia. O projeto recebe dados de nascimento, calcula posições astrológicas aproximadas, organiza interpretações detalhadas e produz um relatório preparado para impressão ou salvamento em PDF.

> **Aviso importante:** este projeto é voltado a entretenimento, reflexão e autoconhecimento simbólico. Ele não determina personalidade, futuro ou compatibilidade e não substitui orientação médica, psicológica, jurídica ou financeira.

## Visão geral

O **Mapa Astral** funciona diretamente no navegador e reúne:

- mapa natal com posições aproximadas dos principais corpos celestes;
- Sol, Lua, Ascendente e Meio do Céu;
- planetas em signos e casas;
- aspectos astrológicos principais;
- escolha entre Casas Iguais e Signos Inteiros;
- análise numerológica pitagórica;
- comparação entre nome de nascimento e nome de uso;
- sugestões simbólicas de nomes harmonizados;
- análise de afinidades para relações próximas;
- orientações reflexivas e ciclos de 90 dias;
- relatório completo para impressão ou geração de PDF.

## Tecnologias

O projeto foi construído com tecnologias nativas da Web:

- HTML5;
- CSS3;
- JavaScript puro;
- API de impressão do navegador por `window.print()`.

Não há dependências externas, gerenciador de pacotes, banco de dados ou processo de compilação.

## Estrutura do projeto

```text
.
├── index.html
└── README.md
```

Toda a interface, os estilos, os cálculos e as interpretações estão concentrados em `index.html`.

## Como executar

### Execução direta

1. Baixe ou copie os arquivos do projeto.
2. Abra `index.html` em um navegador moderno.
3. Preencha os dados de nascimento.
4. Clique em **Gerar estudo completo**.

### Servidor local opcional

O arquivo pode ser aberto diretamente, mas também é possível servi-lo localmente:

```bash
python -m http.server 8000
```

Depois, acesse no navegador:

```text
http://localhost:8000
```

## Dados de entrada

A aplicação solicita:

- nome completo de nascimento;
- nome atual, artístico ou assinatura, opcional;
- data de nascimento;
- hora local de nascimento;
- cidade e país;
- latitude;
- longitude;
- fuso UTC vigente na data;
- sistema de casas.

### Convenção das coordenadas

- Latitude norte: positiva.
- Latitude sul: negativa.
- Longitude leste: positiva.
- Longitude oeste: negativa.

Exemplo para São Paulo:

```text
Latitude:  -23.5505
Longitude: -46.6333
Fuso:      -3
```

A precisão da hora, das coordenadas e do fuso influencia especialmente o Ascendente, o Meio do Céu e a distribuição dos planetas pelas casas.

## Sistemas de casas

### Casas Iguais

A Casa 1 começa no grau exato do Ascendente. Cada casa seguinte ocupa 30 graus.

Exemplo: se o Ascendente estiver a 18 graus de Touro, a Casa 1 começa em 18 graus de Touro e termina imediatamente antes de 18 graus de Gêmeos.

### Signos Inteiros

O signo no qual o Ascendente está localizado torna-se integralmente a Casa 1. Cada signo seguinte corresponde à casa seguinte.

Exemplo: se o Ascendente estiver em qualquer grau de Touro, todo o signo de Touro será a Casa 1, Gêmeos será a Casa 2 e Câncer será a Casa 3.

## Funcionalidades astrológicas

### Posições principais

O aplicativo trabalha com:

- Sol;
- Lua;
- Mercúrio;
- Vênus;
- Marte;
- Júpiter;
- Saturno;
- Urano;
- Netuno;
- Plutão;
- Ascendente;
- Meio do Céu.

### Aspectos

São considerados os aspectos maiores:

- conjunção;
- sextil;
- quadratura;
- trígono;
- oposição.

Os aspectos são organizados pelo orbe calculado. A interpretação procura apresentar potenciais de fluidez, fusão ou tensão criativa.

### Eixos estruturais

O relatório inclui referências a:

- Ascendente e Descendente;
- Meio do Céu e Fundo do Céu.

### Roda zodiacal

A interface apresenta uma roda visual com glifos planetários e indicação do Ascendente. Ela funciona como resumo gráfico e não substitui uma roda profissional com cúspides, aspectos desenhados e escala completa de graus.

## Numerologia

O módulo numerológico utiliza uma tabela pitagórica, na qual as letras são associadas ciclicamente aos números de 1 a 9.

O relatório calcula:

- **Caminho de Vida:** derivado da data de nascimento;
- **Expressão:** calculada com todas as letras do nome;
- **Alma:** calculada pelas vogais;
- **Personalidade:** calculada pelas consoantes;
- **Ano Pessoal:** calculado a partir do dia, mês e ano civil atual.

Os números mestres 11, 22 e 33 são preservados em reduções compatíveis com a implementação atual.

## Harmonização e sugestões de nomes

A aplicação compara o nome completo de nascimento com um nome atual, artístico, profissional ou assinatura.

Também são geradas duas categorias de sugestão:

### Nome de uso

O sistema avalia formas como:

- primeiro nome e último sobrenome;
- nomes com iniciais intermediárias;
- assinatura abreviada;
- combinações naturais de partes do nome.

### Nome completo com alteração pontual

O sistema preserva todas as partes do nome e simula inserções pontuais de letras. As opções são classificadas simbolicamente pela aproximação entre:

- Expressão;
- Alma;
- Personalidade;
- Caminho de Vida.

Essas sugestões não garantem sorte, prosperidade ou mudança de destino. Antes de adotar qualquer forma, devem ser avaliadas pronúncia, ortografia, identidade pessoal, uso social e eventuais consequências documentais.

## Afinidades para relações próximas

O relatório apresenta:

- signo com maior facilidade simbólica;
- signo com maior potencial de desafio;
- justificativas relacionadas à Lua, Vênus, Marte e Descendente;
- ranking relativo dos 12 signos.

Esse resultado é apenas uma triagem baseada no signo solar hipotético da outra pessoa. Uma análise de sinastria completa exigiria os dados natais das duas pessoas.

O índice exibido não representa porcentagem, probabilidade ou avaliação científica.

## Relatório gerado

O estudo é dividido nas seguintes partes:

1. Síntese integrada;
2. Planetas nos signos e casas;
3. Aspectos principais;
4. Casas astrológicas;
5. Numerologia;
6. Harmonização e comparação de nomes;
7. Afinidades para relações próximas;
8. Ciclos, previsões reflexivas e aconselhamentos;
9. Perguntas para integração;
10. Qualidade dos dados de entrada;
11. Método e limites.

## Impressão e PDF

Depois de gerar o estudo:

1. Clique em **Imprimir / Salvar em PDF**.
2. Na janela de impressão, escolha uma impressora ou a opção de salvar como PDF.
3. Ajuste margens, escala e cabeçalhos conforme necessário.

O CSS possui regras específicas para impressão, removendo o formulário e os controles de navegação do relatório final.

## Validação dos dados

A aplicação valida:

- preenchimento dos campos obrigatórios;
- latitude entre -90 e 90;
- longitude entre -180 e 180;
- presença de data, hora, cidade e nome.

O relatório também alerta quando a hora está definida como `12:00`, pois esse valor pode ter sido usado apenas como horário padrão e não como hora confirmada do nascimento.

## Privacidade

Na versão atual, os cálculos são executados no próprio navegador. O código não contém envio de formulários, autenticação, banco de dados, cookies ou chamadas de rede.

Mesmo assim, antes de publicar uma versão modificada, revise o código e qualquer serviço externo que venha a ser adicionado.

## Limitações técnicas

Esta implementação utiliza fórmulas e elementos orbitais simplificados. Portanto:

- as posições planetárias são aproximadas;
- Plutão utiliza uma aproximação especialmente simplificada;
- as casas disponíveis são aproximações de Casas Iguais e Signos Inteiros;
- o fuso histórico e o horário de verão não são determinados automaticamente;
- a cidade informada não é convertida automaticamente em coordenadas;
- não há validação contra uma efeméride profissional;
- retrogradação, velocidade, latitude e distância planetária não são exibidas;
- nodos lunares, Lilith, Quíron, asteroides e partes árabes não estão incluídos;
- as interpretações são simbólicas e não possuem validação científica.

## Caminho recomendado para maior precisão

Para transformar este protótipo em uma aplicação profissional, recomenda-se:

1. substituir os cálculos planetários simplificados por uma efeméride validada;
2. integrar um banco histórico de fusos e horário de verão;
3. adicionar busca de cidade e geocodificação;
4. validar resultados contra mapas de referência;
5. incluir mais sistemas de casas;
6. separar o motor astronômico do motor interpretativo;
7. criar testes automatizados para datas, coordenadas e limites;
8. documentar claramente a escola astrológica e numerológica utilizada;
9. revisar as condições de licença de qualquer biblioteca adicionada;
10. tratar dados pessoais conforme a legislação aplicável caso sejam armazenados ou transmitidos.

## Ideias para futuras versões

- sinastria entre duas pessoas;
- trânsitos calculados para datas específicas;
- revolução solar;
- progressões e direções simbólicas;
- nodos lunares, Lilith e Quíron;
- seleção entre zodíaco tropical e sideral;
- mais sistemas de casas;
- exportação estruturada em JSON;
- armazenamento local opcional de mapas;
- temas claro e escuro;
- roda astrológica completa em SVG ou Canvas;
- relatório paginado com capa e sumário;
- testes de regressão para cálculos numerológicos e astrológicos.

## Acessibilidade

O projeto inclui:

- rótulos associados aos campos;
- foco visível nos controles;
- região com `aria-live` para mensagens de validação;
- layout responsivo;
- controles utilizáveis por teclado;
- contraste visual adequado ao tema escuro.

Melhorias futuras podem incluir testes com leitores de tela, revisão completa da ordem de foco e opções de alto contraste.

## Uso responsável

Astrologia e numerologia devem ser tratadas neste projeto como linguagens simbólicas. O relatório não deve ser utilizado para:

- diagnosticar condições de saúde;
- substituir terapia ou atendimento profissional;
- orientar investimentos ou decisões financeiras críticas;
- determinar sozinho a continuidade de relacionamentos;
- classificar pessoas como boas, ruins ou incompatíveis;
- prometer sorte por alteração de nome;
- tomar decisões jurídicas ou documentais sem orientação adequada.

---

### Instalação no computador

### No Google Chrome ou Microsoft Edge:

  1. Abra o endereço publicado do projeto.
  2. Aguarde o carregamento completo da página.
  3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
  4. Selecione Instalar aplicativo ou Instalar este site como aplicativo.
  5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

### Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione Instalar aplicativo ou Adicionar à tela inicial.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

**Observações**

A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
Abrir somente o arquivo index.html pelo computador não garante a instalação como PWA.
O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
O funcionamento offline depende da configuração do service-worker.js e dos arquivos adicionados ao cache.
Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

---

## Autoria

Projeto desenvolvido por **Alberto de Campos Neto**.

## Licença

Nenhuma licença de uso foi definida no código atual. Antes de redistribuir, modificar ou publicar o projeto, adicione um arquivo `LICENSE` com os termos escolhidos.

Se bibliotecas externas forem integradas futuramente, mantenha os avisos de copyright e cumpra as respectivas condições de licenciamento.

## Aviso

> Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.
