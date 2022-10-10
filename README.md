```sql
# Jogo_da_velha_python


1. A lógica do jogo da velha foi feita através de uma matriz, ou seja uma lista dentro de lista, no tam 3x3 de inteiros.
O jogador tem a opção de escolha de linha e coluna para jogar.
1. Caso o jogador 1 irá marcar a opção x e o jogador 2,a opção 0.
3. O x só poderá ser preenchido caso a posição esteja vazia.
4. Deve atentar-se se a linha, coluna está preenchida, após o término do jogo irá visualizar quem ganhou e em quantas rodadas.
5. O tabuleiro é iniciado com valores iguais a 0.
6. Logo em seguida criamos a função menu, criando uma variável com o nome de "continuar", inciando com valor 1.
7. Enquanto esse valor não for nulo, um laço while vai continuar perguntando se o jogador deseja jogar novamente, novamente e novamente.
8. Criamos a função "exibir menu" para mostrar o tabuleiro.

9. O jogador 1 insere o número 1 em um local escolhido no tabuleiro,o mesmo acontece quando o jogador 2 insere um número inteiro, desta forma aparecerá no tabuleiro.
10. Utilizamos 2 laços for aninhados, o primeiro para linha, outro para coluna.
11. O valor 0 irá mostrar que está vazio.
Para jogador 1 = x
Para jogador 2 = o

12. A variável jogada contabilizar o número de rodadas.Iniciada por 0.
Essa variável vai ser incrementada de um em um, a cada rodada.

13. Se pegarmos o resto dessa divisão dessa variável por 2, teremos valor 0 e 1 alternando.
Se somarmos 1, teremos valores 1 e 2 alternando. Vamos avisar ao usuário se é o jogador 1 ou jogador 2 através dessa lógica.

Ou seja, cada jogador é simbolizado por: (jogada%2 + 1)

Primeiro, exibimos o tabuleiro, chamando a função exibe().

14. A seguir, pede uma linha e uma coluna.
Detalhe: o usuário vai digitar 1, 2 ou 3, mas nosso tabuleiro tem as posições 0, 1 e 2. Ou seja, quando o usuário fornecer esses números, temos que subtrair o valor de 1.

Em seguida, testamos se o valor que ele assinalou está vazio, ou seja, se tem um 0 naquela posição do tabuleiro.

Se sim, insere um 1 caso seja vez do jogador um ou -1 se for o jogador dois.

Se não for 0 a posição do tabuleiro, cai no ELSE, avisamos que não pode e subtraímos 1 da variável jogada, pois lá embaixo essa variável é sempre incrementada.

Após cada jogada, chamamos a função ganhou() dentro de um teste condicional.
Essa função checa se alguma linha, coluna ou diagonal está completa.
Se sim, termina o jogo e mostra quem ganhou, em quantas rodadas, se foi linha, coluna ou diagonal que se completou, e exibimos o tabuleiro final.

Caso a função ganhou() retorne 0, é porque ninguém ganhou, incrementamos a variável jogada e o loop while roda novamente uma outra rodada com o outro jogador.

## Quem ganha o jogo da velha

Dentro da função ganhou(), fazemos três checagens.

Primeiro, se alguma linha tem soma de valor 3 ou -3, alguém ganhou e retornamos o valor 1.
Se alguma coluna tem soma 3 ou -3, alguém ganhou e retornamos o valor 2.
Por fim, somamos as diagonais, se alguma tiver valor 3 ou -3, retornamos o valor 3.

Se passar batido por esses testes, retornamos o valor 0, pra simbolizar que ninguém ganhou.
