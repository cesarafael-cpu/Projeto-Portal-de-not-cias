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

* fala para TODOS = Menos autoridade
.classe fala para ALGUNS = Mais autoridade
#id fala para UM = MÁXIMA autoridade
Exemplo Prático: O * Perdendo
Resultado: Parágrafo fica AZUL ✅

Por que?
* diz: "Fique vermelho" (força: 0)
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