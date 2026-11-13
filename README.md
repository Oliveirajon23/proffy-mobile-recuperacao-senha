\# Proffy Mobile — Recuperação de Senha



\## Aluno

\- \*\*Nome:\*\* Jonathan Rosa de Oliveira

\- \*\*Turma:\*\* 6º Período — Sistemas de Informação (UEMG)



\## Como foi implementada a validação e a navegação



\- \*\*Validação em tempo real:\*\* Utilizei o `addTextChangedListener` no campo de e-mail junto com o `Patterns.EMAIL\_ADDRESS` para verificar o formato enquanto o usuário digita.

\- \*\*Exibição de erros:\*\* Se o e-mail estiver em formato inválido ou vazio, o campo exibe a mensagem de erro correspondente usando os textos definidos no `strings.xml`.

\- \*\*Estados do botão:\*\* 

&#x20; - \*\*Inválido/Inicial:\*\* Botão desabilitado, na cor cinza e com o texto \*\*"Entrar"\*\*.

&#x20; - \*\*Válido:\*\* Quando o e-mail é válido, o erro é removido e o botão fica habilitado, na cor verde e com o texto \*\*"Enviar"\*\*.

\- \*\*Navegação para o `FinallyActivity`:\*\* Ao clicar em "Enviar", uma `Intent` abre a `FinallyActivity` passando os textos da tela (\*"Redefinição enviada!"\*, subtítulo e texto do botão) via `putExtra`.

\- \*\*Retorno ao Login:\*\* Na tela de conclusão, o botão \*\*"Voltar ao login"\*\* redireciona para a `LoginActivity` limpando a pilha de telas anteriores (`FLAG\_ACTIVITY\_NEW\_TASK` e `FLAG\_ACTIVITY\_CLEAR\_TASK`).

