# Write-up: Cookie Monster

* **Plataforma:** Escolinha CTF
* **Categoria:** Web
* **Flag:** FLAG{...}
* **Objetivo:** Conseguir encontrar a flag por meio das permissões de cookies do site.

## Análise Inicial
* Ao entrar no site do desafio, a interface exibia uma mensagem informando que eu não possuía privilégios de administrador (*"Você não é admin!"*).
* Como o nome do desafio faz referência direta a "Cookies" e o foco era exploração web, o próximo passo foi inspecionar o armazenamento do navegador para ver como os dados da sessão eram guardados.

##  Resolução
1. Utilizei as Ferramentas do Desenvolvedor do navegador (F12) e fui até a aba **Application** (ou armazenamento / cookies).
2. Localizei o cookie associado à sessão e encontrei uma chave/parâmetro chamada `admin` com o valor inicial setado como `nao`.
3. Percebi que a aplicação validava o acesso administrativo verificando diretamente essa informação armazenada no lado do cliente (*client-side*).
4. Para testar a vulnerabilidade, alterei o valor da chave `admin` de `nao` para `sim`.
5. Atualizei a página e o sistema reconheceu o novo valor, liberando o acesso restrito e exibindo a *flag* na tela.

## Conclusão
Esse desafio ilustra o perigo de confiar em dados controlados pelo usuário (como cookies ou parâmetros locais) para definir permissões de segurança. Níveis de acesso e privilégios devem sempre ser validados e processados com segurança no lado do servidor (*back-end*).
