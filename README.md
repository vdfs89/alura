# Meus Estudos na Alura

Repositorio com resumos e anotacoes dos cursos concluidos na Alura (Pos Tech).

---

## Cursos Concluidos

| # | Curso | Conclusao |
|---|---|---|
| 1 | Praticando Python: condicionais if, elif e else | 30/06/2026 |
| 2 | Praticando Python: lacos for e while | 30/06/2026 |

---

## Curso 1 — Condicionais if, elif e else

### O que sao estruturas condicionais?

Sao estruturas que permitem que o programa tome decisoes diferentes dependendo de uma condicao ser verdadeira ou falsa.

### As 3 estruturas principais

#### `if` — Se
Avalia uma condicao. Se verdadeira, executa o bloco de codigo abaixo.

```python
if temperatura > 25:
    print("Alerta! Temperatura acima do limite.")
```

#### `elif` — Senao se
Usado quando ha multiplas condicoes a verificar. So e avaliado se o `if` anterior foi falso.

```python
if imc < 18.5:
    print("Abaixo do peso.")
elif imc < 25:
    print("Peso normal.")
```

#### `else` — Senao
Captura todos os casos restantes que nao foram cobertos pelo `if` nem pelo `elif`. E opcional.

```python
else:
    print("Acima do peso.")
```

### Regras importantes

- Os **dois pontos `:` sao obrigatorios** apos cada condicao
- O bloco de codigo deve estar **indentado** (4 espacos ou 1 tab)
- O `else` e **opcional**
- Pode haver **varios `elif`s** encadeados, mas apenas **um `if`** e **um `else`** por estrutura

### Operadores de comparacao

| Operador | Significado |
|---|---|
| `>` | Maior que |
| `<` | Menor que |
| `>=` | Maior ou igual |
| `<=` | Menor ou igual |
| `==` | Igual a |
| `!=` | Diferente de |
| `and` | E (ambas verdadeiras) |
| `or` | Ou (pelo menos uma verdadeira) |
| `%` | Modulo (resto da divisao) |

### Exercicios praticados

| Exercicio | Conceito |
|---|---|
| Monitorando vendas no comercio | `if / elif / else` para comparar valores |
| Calculando tempo total de projeto | Validacao de valores negativos |
| Temperatura dos servidores | Condicao simples com limite maximo |
| Calculando o IMC | Multiplos `elif` para faixas de valores |
| Controlando o orcamento mensal | Comparacao com limite financeiro |
| Controle de acesso ao escritorio | Intervalo com `<=` e `<` |
| Classificando estudantes por media | Calculo + multiplas faixas |
| Calculando pedagio | `elif` com ranges de distancia |
| Verificando paridade de numero | Operador modulo `%` |
| Aprovando emprestimo | Combinacao com `and` |

---

## Curso 2 — Lacos for e while

### O que sao lacos de repeticao?

Sao estruturas que permitem executar um bloco de codigo multiplas vezes, enquanto uma condicao for verdadeira ou percorrendo uma sequencia de elementos.

### Os 2 lacos principais

#### `for` — Laco de iteracao
Usado quando se sabe quantas vezes o codigo deve repetir, ou para percorrer uma sequencia (lista, string, range).

```python
for cliente in clientes:
    print(cliente)
```

#### `while` — Laco condicional
Usado quando nao se sabe quantas repeticoes serao necessarias — repete enquanto a condicao for `True`.

```python
while estoque > 0:
    estoque -= 1
```

### Conceitos importantes

| Conceito | Descricao |
|---|---|
| `range(n)` | Gera sequencia de 0 ate n-1 |
| `range(a, b, passo)` | Sequencia de `a` ate `b-1` com passo definido |
| `break` | Interrompe o laco imediatamente |
| `continue` | Pula a iteracao atual e vai para a proxima |
| Loop infinito | Ocorre quando a condicao do `while` nunca se torna falsa |

### Exercicios praticados

| Exercicio | Conceito |
|---|---|
| Compreendendo lacos | `for` vs `while` |
| O que e um loop infinito? | Identificar e corrigir loops sem parada |
| Quantas vezes a mensagem sera exibida? | `for` com `range()` |
| Calculando a soma de numeros | Acumulador com `for` |
| Organizando seu portfolio | `for` + `if/else` para filtrar `None` |
| Entendendo o uso do `break` | Parar laco ao encontrar item |
| Controle de estoque | `while` para decrementar ate zero |
| Contagem Regressiva | `for` + `range()` decrescente |
| Utilidade do `continue` | Ignorar itens com estoque zero |
| Validacao de entrada para login | `while True` + validacoes com `break` |

### Exemplos de gabarito

```python
# Contagem regressiva
for segundos in range(10, 0, -1):
    if segundos % 2 == 0:
        print(f"Faltam apenas {segundos} segundos - Nao perca essa oportunidade!")
    else:
        print(f"A contagem continua: {segundos} segundos restantes.")
print("Aproveite a promocao agora!")

# Controle de estoque com while
estoque = 5
while estoque > 0:
    estoque -= 1
    print(f"Venda realizada! Estoque restante: {estoque}")
print("Estoque esgotado")

# Validacao de login com while True
while True:
    nome_usuario = input("Digite seu nome de usuario: ")
    senha = input("Digite sua senha: ")
    if len(nome_usuario) < 5:
        print("O nome de usuario deve ter pelo menos 5 caracteres.")
    elif len(senha) < 8:
        print("A senha deve ter pelo menos 8 caracteres.")
    else:
        print("Cadastro realizado com sucesso!")
        break
```

---

*Atualizado em: 30/06/2026*
