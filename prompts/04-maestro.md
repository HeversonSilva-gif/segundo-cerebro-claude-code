# Passo 4: o maestro e os dois agentes

Separa quem faz de quem confere: um agente executa o trabalho pesado e outro revisa, enquanto a conversa principal só decide.

Copie tudo o que está no bloco abaixo e cole numa conversa nova do Claude Code. O que está entre `<` e `>` é com você: troque pelo seu.

```
Quero que esta conversa vire o maestro: ela conversa comigo, decide e confere, e o trabalho pesado vai pra outros agentes.

1. Crie dois subagentes em ~/.claude/agents:
   - executor.md (model: sonnet): faz o trabalho pesado a partir de um pedido completo (ler muitos arquivos, implementar, rodar testes). Não muda o pedido por conta própria. Devolve só um resumo de até 10 linhas: o que fez, o resultado dos testes e onde estão os detalhes.
   - revisor.md (model: opus): revisa o que o executor entregou, sem mudar nada: se está certo, se é seguro, os casos de borda e os testes. Termina com um veredito (Aprovado, Aprovado com detalhes ou Precisa de correção) e cada problema com arquivo e linha.
2. No ~/.claude/CLAUDE.md, escreva a regra do maestro:
   - Coisa pequena você faz aqui mesmo. Trabalho pesado vai pro executor, com o pedido completo, porque ele não vê esta conversa.
   - Toda entrega passa pelo revisor antes de você me dizer que está pronto.
   - O que mexe com segurança, senha ou dinheiro, o executor faz com o Opus (model: opus no despacho).
   - Correção vai pra um executor novo, junto com o relatório do revisor.

Me mostre os dois arquivos e a regra antes de salvar.

Depois de salvar, abra de novo o executor.md, o revisor.md e o CLAUDE.md e confirme que cada um está como combinamos, inclusive o model de cada agente.
```
