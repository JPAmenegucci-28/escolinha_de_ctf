# write-up

* **Plataforma:** Escolinha CTF
* **Categoria:** Web

* **Flag:** FLAG{...}

* **Objetivo:** Conseguir encontrar a flag por meio da descriptografia de um texto em código na linguagem brainfuck.

# ANÁLISE INICIAL

O desafio começa com um arquivo do tipo 'txt' de uma mensagem composta por símbolos como +, -, <, >, [ , ] e .. e pede para que encontremos a flag.

*Código:*

+++++++[<++++++++++>-]<.[-]>+++++++[<++++++++++>-]<++++++.[-]>++++++[<++++++++++>-]<+++++.[-]>+++++++[<++++++++++>-]<+.[-]>++++++++++++[<++++++++++>-]<+++.[-]>+++++++++[<++++++++++>-]<+++++++++.[-]>++++[<++++++++++>-]<++++++++.[-]>++++++++++[<++++++++++>-]<.[-]>++++[<++++++++++>-]<+++++++++.[-]>++++++++++[<++++++++++>-]<+++.[-]>++++[<++++++++++>-]<++++++++.[-]>+++++++++[<++++++++++>-]<+++++.[-]>+++++[<++++++++++>-]<+.[-]>+++++++++++[<++++++++++>-]<+++++.[-]>++++[<++++++++++>-]<++++++++.[-]>+++++++++++[<++++++++++>-]<++++++.[-]>+++++[<++++++++++>-]<+.[-]>+++++++++++[<++++++++++>-]<++++.[-]>++++[<++++++++++>-]<+++++++++.[-]>+++++++++[<++++++++++>-]<+++++++++.[-]>++++[<++++++++++>-]<++++++++.[-]>++++++++++++[<++++++++++>-]<+++++.

# RESOLUÇÃO

Para resolvermos esse problema é necessário utilizar o dcode [ https://www.dcode.fr/brainfuck-language ] , um site de identificação e decriptografia de textos que são as dois únicos métodos necessários para resolver esse desafio. Dada a introdução da ferramenta utilizada basta colocar o texto que queremos decriptografar primeiro no identificador de linguagem e descobrimos que se trata da linguagem brainfuck, sabendo disso vamos para a descriptografia

<img width="477" height="241" alt="Captura de tela 2026-09-15 212050" src="https://github.com/user-attachments/assets/7a431e80-fbd1-453b-964b-b722127818d0" />


<img width="366" height="137" alt="Captura de tela 2026-09-15 212737" src="https://github.com/user-attachments/assets/9d1e8a9c-d8ab-481b-82bd-1509c30fb304" />


Após esses passos é possível notar que a decriptografia entregou a flag no formato certo assim resolvendo o problema.

# CONCLUSÃO

Conclui-se que se trata de um problema de descriptografia básico somente de identificar a linguagem do texto e descriptografando o mesmo para obter a flag. Ilustrando que informações importantes podem estar somente criptografadas e podem ser resolvidas para serem usadas por alguém.
 

