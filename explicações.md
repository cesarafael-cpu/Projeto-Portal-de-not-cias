- [ ] * { margin, padding, box-sizing: border-box}
- margin: 0;
Margin é um espaço vazio ao redor das coisas (como um colchão de ar).
0 significa remover esse espaço → tudo fica bem juntinho
Sem isso, cada elemento deixaria espaços estranhos na página

- padding: 0;
Padding é o espaço vazio dentro das coisas (como espaço dentro de uma caixa).
0 significa remover esse espaço interno também
Garante que tudo comece do zero

- box-sizing: border-box;
Isso é um "truque" importante! Diz como medir o tamanho das coisas:
Sem isso: se você diz "caixa de 100 pixels", ela fica maior por causa das bordas
Com border-box: ela fica exatamente 100 pixels, sem surpresas!

- [] Especificidade do asterisco *
ESPECIFICIDADE DO * (Seletor Universal)
O que é Especificidade?
Imagina uma escola com regras gerais para todos e regras especiais para algumas turmas:
🤔 Qual regra vence? A mais específica! (A turma A fica com vermelho)
Em CSS funciona igual:
* = Regra para TUDO (menos específica)
.classe = Regra para uma classe específica (mais específica)
#id = Regra para um ID específico (MUITO mais específica)
A Especificidade do * é ZERO ⭐
O que isso significa?
Seletor	Especificidade	Força
*	0	⚫⚫⚫ Mais fraco
p	1	🔵🔵🔴 Médio
.classe	10	🟢🟢🟢 Forte
#id	100	🟡🟡🟡 MUITO forte
Visualizando:
Por quê? Porque p é mais específico que *!
Por Que o * é Tão Fraco?
Comparação com a vida real:
Quem tem mais autoridade?

Professor (fala para TODOS) = Menos autoridade
Diretor (fala para UMA turma) = Mais autoridade
Mãe (fala para UMA pessoa) = MÁXIMA autoridade
Em CSS:

- fala para TODOS = Menos autoridade
.classe fala para ALGUNS = Mais autoridade
#id fala para UM = MÁXIMA autoridade
Exemplo Prático: O * Perdendo
Resultado: Parágrafo fica AZUL ✅

Por que?
- diz: "Fique vermelho" (força: 0)
p diz: "Fique azul" (força: 1)
1 > 0, então p ganha!
Outro Exemplo: * Perdendo Mais
Resultado:

Cor: VERDE (porque .especial é mais específico)
Tamanho: 12px (porque ninguém pediu para mudar)
A Cascata: Como CSS Decide Qual Regra Vale
Exemplo da Cascata:
Resultado: Parágrafo fica VERDE porque é o mais específico!

Por Que Usamos o * se é Tão Fraco?
Resposta: Exatamente PORQUE é fraco! 💡
É como se disséssemos:

"Remova espaços de TUDO, MAS deixo aberto para outras regras mudarem depois se quiserem"
Dica Final: Quando o * é Útil
O * é perfeito para:

Reset (limpar espaços padrão)
Base (começar do zero)
Fallback (valor padrão, facilmente sobrescrito)
Porque deixa espaço para regras mais específicas vencerem! 🏆

Resumo em Uma Frase
"O * é o policial que avisa: 'ATENÇÃO A TODOS', mas qualquer comando mais específico ignora o aviso!"

* <nav> é um menu de navegação
* <div> é como uma caixa de ferramenta onde se coloca algo como uma imagem, por exemplo
* <strong> é colocar algo em negrito
* tag <a> vem de "anchor" (âncora). É como fazer um clique que te leva para outro lugar
* <a href="#"> É onde o link vai levar. O # sozinho significa "não vai para lugar nenhum ainda"
* .grid é como ter um molde pronto para organizar coisas em  linha e coluna.

* O que é .grid?
Primeiro, o .grid é como se você criasse uma grade (tipo um tabuleiro de xadrez) dentro dessa caixa. Essa grade ajuda a colocar os brinquedos em linhas e colunas de forma organizada.
* O que é .grid-flow-col?
Agora, o .grid-flow-col é uma regra especial que diz:
"Coloca os brinquedos um ao lado do outro, em colunas (na horizontal), em vez de um embaixo do outro (na vertical)"
Exemplo prático:
Sem o grid-flow-col (um embaixo do outro):
🧩
🧩
🧩
Com o grid-flow-col (um do lado do outro):
🧩 🧩 🧩

- O que é CSS Nesting?
Nesting quer dizer "aninhar" ou "colocar uma coisa dentro da outra", como bonecas russas!
Exemplo fácil:
Pense em uma caixa grande (#primary) que tem uma caixa pequena dentro (div):
┌─────────────────────────┐
│  #primary (caixa grande)│
│                         │
│  ┌──────────────────┐   │
│  │ div (caixa pequena)  │
│  │ (2º filho)       │   │
│  └──────────────────┘   │
│                         │
└─────────────────────────┘

O que o código faz:
#primary {
  padding-block: 20px;  /* Deixa espaço em cima e embaixo da caixa grande */
  
  /* Agora, mexemos só com a caixa pequena que está DENTRO */
  div: nth-child(2) {
    /* Aqui você coloca as regras só para essa caixa pequena */
  }
}

📝 Resumindo:
#primary = caixa grande (todo o cabeçalho)
div: nth-child(2) = a 2ª caixa dentro da caixa grande
Tudo isso junto = suas regras ficam organizadas e fáceis de entender!

- O que é .container?
.container { max-width: 1280px; }
.container é uma classe (um rótulo para agrupar coisas)
max-width: 1280px = "nunca fique mais largo que 1280 pixels"
padding-inline: 32px = coloca espaço nas laterais (32 pixels de cada lado)
margin-inline: auto = centra tudo na tela!

- O que cada linha faz:
div { display: flex; align-items: center; }
div = É como uma caixa invisível que contém coisas
display: flex = É como se você dissesse: "Quero que as coisas dentro dessa caixa fiquem em linha, como soldadinhos em fila"
align-items: center = Significa "coloca tudo no meio" - tipo quando você quer que todos os seus amigos fiquem na mesma altura, nem um em cima nem embaixo

- 1. O que é #featured?
É um "ID" no CSS. Pense nele como um nome especial para uma caixa no site. Só uma coisa no site pode ter esse nome. É como dar um apelido único para o seu brinquedo favorito.
Tudo dentro das chaves {} depois de #featured são regras só para essa caixa.
2. img { height: 100%; object-fit: cover; }
img é a imagem dentro da caixa #featured. É como uma foto que você cola no quadro.
height: 100%; significa que a altura da imagem vai ocupar 100% da altura da caixa. Se a caixa é alta como uma porta, a imagem cresce para caber toda a altura.
object-fit: cover; é uma mágica para a imagem. Se a imagem for maior ou menor que a caixa, ela "corta" as partes extras para caber perfeitamente, sem deformar. É como cortar uma foto para encaixar em um porta-retratos sem deixar buracos.
3. .card { ... }
.card é uma classe (tipo um grupo de coisas parecidas). É como um cartão de visita ou um cartão de jogo que fica em cima da imagem.
border-radius: 4px; arredonda os cantos do cartão, como fazer um quadrado virar um retângulo com cantinhos suaves. 4px é um pouquinho, tipo o tamanho de uma borracha pequena.
overflow: hidden; esconde qualquer coisa que saia para fora do cartão. É como cortar as bordas de um papel para não sair da mesa.
position: relative; diz que o cartão pode se mover um pouco em relação ao resto da página. É como posicionar um boneco em um cenário.
4. &::before { ... }
&::before é um truque para adicionar algo invisível antes do cartão. É como colocar um vidro transparente em cima da imagem.
content: ""; cria esse vidro vazio (sem texto).
position: absolute; faz ele flutuar em cima, como uma camada extra.
inset: 0; cobre toda a área do cartão, como uma folha de papel em cima de outro.
top: 50%; começa no meio da altura (50% para cima).
background: linear-gradient(...); pinta um fundo que vai de transparente (invisível) no topo para uma cor escura (#020617, tipo azul-escuro) embaixo. É como um filtro que escurece a parte de baixo da imagem, para que o texto fique legível.
No geral: Esse código faz a imagem de destaque ficar bonita e coberta por um cartão com cantos arredondados e um efeito de sombra escura embaixo. É para tornar a notícia principal mais atraente, como uma capa de revista!

- A REGRA ESPECIAL &:has(.text-lg)
Isso é tipo uma regra com condição:

& = "se for ESTE elemento..."
:has(.text-lg) = "...E se TIVER dentro dele uma coisa chamada .text-lg..."
padding: 12px; = "...então muda o espaço para 12 passinhos!" (menor que 24)
Traduzindo em linguagem de criança:

"Se o título for GRANDE, coloca menos espaço. Se for pequeno, coloca mais espaço." É como ajustar a roupa: se sua mochila é pesada, você ajusta o espaço.