# Passo 1: a memória

Dá ao Claude uma memória entre conversas, com um fato por arquivo e um índice pequeno que ele lê toda vez.

Copie tudo o que está no bloco abaixo e cole numa conversa nova do Claude Code. O que está entre `<` e `>` é com você: troque pelo seu.

```
Quero que você passe a ter memória entre conversas, com uma memória por arquivo. Monte assim:

1. Crie a pasta ~/.claude/memoria e, dentro dela, o arquivo indice.md.
2. No ~/.claude/CLAUDE.md, acrescente a linha @~/.claude/memoria/indice.md, pra você ler o índice em toda conversa.
3. Logo abaixo, escreva estas regras:
   - Quando eu te corrigir ou disser "guarda isso", crie um arquivo novo em ~/.claude/memoria com um fato só: a regra, o porquê e a data de hoje.
   - Acrescente no indice.md uma linha apontando pra ele: - [título](arquivo.md) — do que se trata, em uma frase.
   - Antes de criar, veja se já existe um arquivo sobre o assunto. Se existir, atualize esse em vez de criar outro.
   - Se uma memória ficar errada, corrija ou apague, e tire a linha do índice.
   - O índice tem só uma linha por memória. O detalhe fica no arquivo, que você só abre quando precisar.
   - Não guarde o que já está no código nem o que só importa pra esta conversa.

Me mostre como vai ficar o CLAUDE.md antes de salvar.
```
