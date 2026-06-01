# Desafio Codeforces — Mentoria Codificadas | Além do Código
 
## Sobre este repositório
 
Este repositório contém minha resolução para o desafio de programação proposto na mentoria, utilizando problemas da plataforma [Codeforces](https://codeforces.com/) com auxílio de Inteligência Artificial.
 
---
 
## Problemas escolhidos
 
| # | Nome do problema | Link | Dificuldade |
|---|-----------------|------|-------------|
| 1 | A. Round Down the Price | [Ver no Codeforces](https://codeforces.com/problemset/problem/1702/A) | 800 |
| 2 | B. Queue at the School | [Ver no Codeforces](https://codeforces.com/problemset/problem/266/B) | 800 |

---
 
## Problema 1 — A. Round Down the Price
 
### O que o problema pede?
O problema pede para arredondar os preços para os vendedores usando a base 10. Depois de colocar um numero tem que achar a potencia de base 10 menor ou igual e calcular a diferença do numero proposto inicialmente.
 
 
### Como eu resolvi?
Primeiro li o número de casos de teste. Usei um for para repetir o processo para cada caso. Dentro do for, usei um while para encontrar a maior potência de 10 que cabe em m. No final, calculei a diferença entre m e a potência encontrada e mostrei a resposta.
 
 
### Código
```python
t = int(input())

for _ in range(t):
    m = int(input())

    potencia = 1 
    while potencia * 10 <= m:
        potencia *= 10

    print(m - potencia)
```
 
---
 
## Problema 2 — B. Queue at the School
 
### O que o problema pede?
Em uma fila de escola onde os meninos trocam de lugares com as meninas, o problema pede pra dizer como estará a fila após tantos segundos.
 
### Como eu resolvi?
Primeiro li o tamanho da fila e o número de segundos. Usei um for para repetir o processo a cada segundo. Dentro do for usei um while para percorrer a fila procurando o par "BG". Quando encontrava, trocava para "GB" e pulava duas posições para não trocar a mesma posição duas vezes. No final, juntei a lista de volta em uma string e mostrei a fila resultante.
 
### Código
```python
def resolver_fila():
    n, t = map(int, input().split())
    fila = list(input())
    
    for _ in range(t):
        i = 0
        while i < n - 1:
            if fila[i] == 'B' and fila[i+1] == 'G':
                fila[i], fila[i+1] = fila[i+1], fila[i]
                i += 2
            else:
                i += 1
                
    print("".join(fila))

if __name__ == "__main__":
    resolver_fila()
```
---
 
## IA utilizada
 
**Qual IA você usou?**
Claude e Gemini
 
**Como a IA te ajudou?**
Usei primeiro para me ajudar a traduzir e entender de fato o problema, depois pedi ajuda com a estratégia e fui tentando montar o codigo recebendo ajuda para corrigir os erros. No segundo desafio tive um problema e estava sendo dificil de entender o erro, então usei o Gemini, para tentar de outra forma e deu certo.
 
---
 
## Reflexão
 
### Dificuldades encontradas
Tive mais dificuldade em escrever o codigo, por mais que eu tivesse uma noção do que poderia fazer, tive alguns erros na hora de escrever o codigo.
 
 
### O que aprendi
Aprendi uma nova maneira de usar o for, junto com o while e o if, nunca tinha feito nada com o uso dos três, tambem aprendi sobre o conceito de listas e join. Gostei muito da explicação da IA, me ajudou bastante a entender os erros e o proprio problema, e ir fazendo passo a passo. 
 
 
### Como foi a experiência?
Eu gostei bastante, senti que consegui praticar e aprender, achei que sentiria mais dificuldades no processo, mas com a ajuda da IA, consegui ter um suporte e nao fiquei totalmente perdida.
