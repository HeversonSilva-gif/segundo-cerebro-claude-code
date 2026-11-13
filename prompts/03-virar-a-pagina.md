# Passo 3: virar a página

Cria a regra de escrever o retomar.md e começar uma conversa nova quando a atual fica grande ou muda de assunto.

Copie tudo o que está no bloco abaixo e cole numa conversa nova do Claude Code. O que está entre `<` e `>` é com você: troque pelo seu.

```
Coloque no ~/.claude/CLAUDE.md uma regra chamada "Virar a página":

Quando eu disser "vira a página", quando eu trocar de assunto ou quando a conversa passar de 300 mil tokens, escreva o arquivo <caminho da pasta de cima>/retomar.md com:
- o que a gente estava fazendo;
- o próximo passo;
- os arquivos envolvidos;
- o que espera decisão minha;
- uma seção "Não conferi", com tudo o que veio de cabeça e não foi lido nem testado agora (se não tiver nada, escreva "nada").

O retomar cabe numa página e traz tudo o que ainda está pendente, porque cada versão substitui a anterior. Depois de escrever, me peça pra digitar /clear.

Quando uma conversa nova começar com "retoma", leia o retomar.md antes de qualquer coisa. O que estiver em "Não conferi" é suspeita, não fato: confira antes de usar.

Me mostre como vai ficar antes de salvar e espere o meu ok.

Depois de salvar a regra, abra o ~/.claude/CLAUDE.md de novo e confirme que ela está lá, com os cinco itens do retomar, e, comparando com a cópia do começo, confirme que nada do que já estava no CLAUDE.md sumiu.
```
