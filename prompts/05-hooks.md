# Passo 5: os hooks

Cria dois hooks: um que avisa quando a conversa passa de 300 mil tokens e outro que lembra a data, a hora e as suas regras a cada mensagem.

Copie tudo o que está no bloco abaixo e cole numa conversa nova do Claude Code. O que está entre `<` e `>` é com você: troque pelo seu.

```
Quero dois hooks no Claude Code. Antes de mexer, faça uma cópia do ~/.claude/settings.json e me mostre o que vai mudar.

1. O teto (evento Stop): um script em Python que lê o JSON da entrada, abre o arquivo do transcript_path, pega o usage da última resposta e soma input_tokens, cache_creation_input_tokens e cache_read_input_tokens. Se passar de 300 mil, responde {"decision": "block", "reason": "A conversa passou de 300 mil tokens. Vire a página: escreva o retomar e me peça /clear."}. Depois disso, só avisa de novo a cada 100 mil a mais (guarde o último aviso num arquivo com o session_id). Se a entrada vier com stop_hook_active verdadeiro, ou se der qualquer erro, ele sai sem dizer nada.
2. O lembrete (evento UserPromptSubmit): um script que imprime a data e a hora do meu PC e um lembrete de no máximo três linhas com as regras que eu mais quero que você siga numa conversa longa. Me pergunte quais são essas regras antes de escrever. Tudo o que ele imprime é relido a cada mensagem, então tem que ser curto.

Antes de escrever, veja qual comando do Python existe neste PC (python3, python ou py: rode cada um com --version e use o que responder uma versão; se não houver, me diga e pare) e use esse no settings.json, com o caminho do script entre aspas. Abra os arquivos e escreva a saída em UTF-8. Teste os dois rodando à mão exatamente o comando que ficou no settings.json, com um JSON de exemplo na entrada; no teto, use o transcript desta conversa e um limite de teste de 1000 tokens pra ver o aviso sair, e depois volte pra 300 mil. Me diga como conferir em /hooks.

Depois de salvar, confira que o settings.json é um JSON válido e, comparando com a cópia, que nada do que já estava lá sumiu; rode de novo, à mão, o comando de cada hook copiado do settings.json e me mostre a saída.
```
