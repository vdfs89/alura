# Meus Estudos na Alura

Repositorio com resumos e anotacoes dos cursos concluidos na Alura (Pos Tech).

---

## Cursos Concluidos

| # | Curso | Conclusao |
|---|---|---|
| 1 | Praticando Python: condicionais if, elif e else | 30/06/2026 |
| 2 | Praticando Python: lacos for e while | 30/06/2026 |
| 3 | Praticando Python: funcoes | 30/06/2026 |
| 4 | Pandas: conhecendo a biblioteca | 30/06/2026 |
| 5 | Python: Inteligência Artificial Aplicada | 30/06/2026 |

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

## Curso 3 — Funcoes em Python

### O que sao funcoes?

Funcoes sao blocos de codigo reutilizaveis que executam uma tarefa especifica. Sao definidas com a palavra-chave `def` e podem receber parametros e retornar valores.

### Estrutura basica

```python
def nome_da_funcao(parametro1, parametro2):
    # bloco de codigo
    return resultado
```

### Tipos de funcoes

#### Funcao simples
Recebe parametros e retorna um valor calculado.
```python
def calcular_idade(ano_nascimento, ano_atual):
    return ano_atual - ano_nascimento
```

#### Funcao lambda
Funcao anonima de uma linha, ideal para operacoes simples e rapidas.
```python
soma = lambda x, y: x + y
multiplica = lambda x, y: x * y
```

#### Closure
Funcao interna que lembra variaveis da funcao externa mesmo apos sua execucao.
```python
def criar_desconto(porcentagem):
    def aplicar(valor):
        return valor - (valor * porcentagem / 100)
    return aplicar

desconto10 = criar_desconto(10)
print(desconto10(200))  # 180.0
```

#### Funcao recursiva
Funcao que chama a si mesma. Precisa sempre de uma condicao de parada.
```python
def soma_recursiva(n):
    if n == 1:
        return 1
    return n + soma_recursiva(n - 1)
```

### Funcoes built-in utilizadas

| Funcao | Descricao |
|---|---|
| `len()` | Conta o numero de caracteres/elementos |
| `sum()` | Soma os elementos de uma lista |
| `map()` | Aplica uma funcao a cada elemento de uma sequencia |
| `filter()` | Filtra elementos de uma sequencia com base em uma condicao |
| `zip()` | Junta duas ou mais listas em pares |
| `int()`, `float()`, `str()` | Convertem tipos de dados |

### Exercicios praticados

| Exercicio | Conceito |
|---|---|
| Calculando a idade | Funcao simples com parametros e `return` |
| Contador de caracteres | Funcao com `len()` |
| Saudacao personalizada | Funcao + `if/elif/else` |
| Conversor de tipos | Duas funcoes: converter `str` -> `int` e verificar |
| Calculando total de vendas | `input().split()` + `map()` + `sum()` |
| Filtrando numeros pares | `filter()` + `lambda` + `join()` |
| Juntando listas de produtos | `zip()` para unir produtos e precos |
| Calculadora com lambda | `lambda` para as 4 operacoes matematicas |
| Gerador de funcoes personalizadas | Closure para calcular descontos |
| Somando numeros recursivamente | Funcao recursiva com condicao de parada |

### Exemplos de gabarito

```python
# Filtrando numeros pares com filter + lambda
numeros = input("Digite os numeros separados por espaco: ").split()
pares = filter(lambda x: int(x) % 2 == 0, numeros)
print("Numeros pares:", " ".join(pares))

# Juntando listas com zip
produtos = input("Digite os produtos separados por virgula: ").split(",")
precos = input("Digite os precos separados por virgula: ").split(",")
for produto, preco in zip(produtos, precos):
    print(f"{produto.strip()}: {preco.strip()}")

# Closure de desconto
def criar_desconto(porcentagem):
    def aplicar_desconto(valor):
        return valor * (1 - porcentagem / 100)
    return aplicar_desconto

desconto = int(input("Digite a porcentagem de desconto: "))
valor = float(input("Digite o valor da compra: "))
aplicar = criar_desconto(desconto)
print(f"Preco final com desconto: {aplicar(valor)}")
```

---

*Atualizado em: 30/06/2026*

---

## Curso 4 - Pandas: conhecendo a biblioteca

### Sobre o curso
Curso da Alura (Pos Tech) que ensina a usar a biblioteca Pandas para análise e manipulação de dados em Python, utilizando um dataset de imóveis para alugar.

### Aula 01 - Importando os dados
#### Conceitos
- O que é o Pandas e para que serve
- Estruturas de dados principais: **Series** (unidimensional, com índices) e **DataFrame** (tabular, bidimensional)
- Como importar um arquivo CSV com `pd.read_csv()`
- Explorando o DataFrame com `.head()`, `.tail()`, `.shape`, `.info()`, `.describe()`
- Selecionando colunas e usando `.value_counts()` e `.groupby()` para agrupar dados
- Filtrando linhas com o método `.query()`

---

### Aula 02 - Analisando e filtrando os dados
#### Conceitos
- Cálculo de médias por categoria com `.groupby().mean()`
- Análise de percentuais com `.value_counts(normalize=True)`
- Filtros com operadores booleanos `&` (e) e `|` (ou)
- Uso do método `.query()` para seleções expressivas
- Renomeando colunas com `.rename()`

---

### Aula 03 - Tratando e filtrando dados
#### Conceitos
- Identificar dados nulos com `.isnull().sum()`
- Preencher valores nulos com `.fillna()`
- Remover linhas com dados nulos com `.dropna()`
- Remover linhas e colunas com `.drop(indices, axis=0)` e `.drop(colunas, axis=1)`
- Aplicar filtros combinados com `&` e `|`
- Salvar DataFrames em CSV com `.to_csv('arquivo.csv', index=False)`
- Salvar em outros formatos: `.to_excel()`, `.to_json()`

---

### Aula 04 - Manipulando os dados
#### Conceitos
- Criar colunas numéricas com operações aritméticas: `df['nova'] = df['a'] + df['b']`
- Criar colunas categóricas com `np.select()` ou condições
- Criar colunas binarias com `.apply(lambda x: True if condicao else False)`
- Usar `.assign()` para criar colunas de forma encadeada
- Usar `.apply()` com funções lambda para transformações
- Substituir valores com `.replace(valor_antigo, valor_novo)`

---

*Atualizado em: 30/06/2026*

---

## Curso 5 - Python: Inteligência Artificial Aplicada

### Sobre o curso
Curso da Alura (Pos Tech) que ensina Python do zero com foco prático em Inteligência Artificial, integrando a API Gemini do Google para criar chatbots e automatizar tarefas usando Google Colab.

### Aula 01 - Fundamentos de Python para iniciantes
#### Conceitos
- Introdução ao Python e configuração do **Google Colab** como ambiente de desenvolvimento
- Células de código e texto no Colab; uso da função `print()`
- **Variáveis**: criação, atribuição e atualização de valores
- **Tipos de dados**: `int`, `float`, `str`, `bool`
- Operações matemáticas: `+`, `-`, `*`, `/`, `//`, `%`, `**`
- **Concatenação de strings** com `+` e conversão de tipos com `str()`, `int()`, `float()`
- Métodos de strings: `.lower()`, `.upper()`, `.strip()`, `.replace()`
- Captura de dados do usuário com `input()` e formatação com **f-strings**
- **Condicionais**: `if`, `elif`, `else` e operadores lógicos (`and`, `or`, `not`)
- **Indentação** em Python como parte da sintaxe (4 espaços por nível)

---

### Aula 02 - Conectando Python e IA com Google Colab
#### Conceitos
- Instalação e configuração da biblioteca `google-genai`
- Autenticação com `GOOGLE_API_KEY` via `userdata.get()`
- Envio de prompts para o modelo **Gemini** com `client.models.generate_content()`
- **Loops `while`**: repetição com condição, `break` para sair do loop
- Criação de **chatbots** com histórico de mensagens em lista
- **Estruturas de dados**: listas (`list`), dicionários (`dict`)
- Função `len()` para contar elementos
- **Índices negativos** em listas para acessar do final
- Uso da API Gemini com contexto de conversa

---

### Aula 03 - Estruturas de repetição e funções em Python
#### Conceitos
- **Loop `for`**: iterar sobre listas, strings e ranges
- **Funções**: definição com `def`, parâmetros, `return`
- Simplificação de código com funções reutilizáveis
- **Operador de resto** `%` para verificar paridade e ciclos
- Resumo de e-mails e textos usando a API Gemini
- Padronização de descrições de produtos com LLMs
- Integração de funções Python com chamadas de API

---

### Aula 04 - Manipulação de arquivos e dados em Python
#### Conceitos
- Leitura e escrita de arquivos com `open()`, `read()`, `write()`, `with`
- Importação e uso da biblioteca **Pandas** para leitura de CSV
- Manipulação de DataFrames: selecionar colunas, filtrar linhas
- Desafios de gerenciamento de dados financeiros (Bytebank)
- Salvamento de resultados em CSV com `.to_csv()`

---

### Aula 05 - Manipulação e filtragem de dados com Pandas
#### Conceitos
- Filtragem avançada com condições booleanas
- Métodos `.loc[]` e `.iloc[]` para seleção de linhas e colunas
- Análise de sentimento de textos usando a API Gemini
- Filtragem de recompensas por critérios
- Definição de índice personalizado com `.set_index()`

---

### Aula 06 - Processamento de resenhas com Inteligência Artificial
#### Conceitos
- **Tratamento de erros** com `try`, `except`, `finally`
- Categorização automática de resenhas negativas com Gemini
- Execução local de modelos de IA (Ollama)
- **Modularização** de código com funções e módulos Python
- Pipeline completo: leitura de CSV → processamento com IA → salvamento de resultados

---

*Atualizado em: 30/06/2026*

*Atualizado em: 30/06/2026*
