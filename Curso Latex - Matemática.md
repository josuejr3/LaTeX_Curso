
O Latex é bastante conhecido por ser bom para escrever equações e símbolos matemáticos. Ele oferece dois modo de escrita para compor as fórmulas matemáticas.

-  Em linha

```tex
$E=mc^2$
```

O ambiente matemático é iniciado e finalizado com o uso do *"$"*. Esse modo em linha é usado para quando queremos descrever matematicamente algo que faz parte do paragráfo.

-  Ambiente

```tex
\begin{equation}
	E=mc^2
\end{equation}
```

O modo de ambiente como vimos antes, inicia e termina com um begin e um end passando o parâmetro de equation. Ele é usado para equações que não fazem parte do texto e que são formatadas separadamente do texto e com uma qualidade superior.
##### ~={cyan}Pacotes=~

-  amsmath 

O pacote mais popular ele formata equações, alinha fórmulas, cria matrizes, sistemas de equações e entre outros.

-  amsfonts

É um pacote que contém uma grande variedade de fontes matemáticas, incluindo fontes especiais para conjuntos, letras gregas e símbolos.

-  amssymb

O pacote adiciona uma grande variedade de símbolos matemáticos adicionais, incluindo símbolos de conjuntos, operadores e setas.

- dsfont

O pacote que contém fontes especiais de conjuntos numéricos como conjunto de números reais, inteiros, racionais e entre outros.

-  mathtools

Pacote que oferece ferramentas adicionais para a criação de equações, incluindo recursos para definir novos operadores, criar equações com várias linhas, entre outros.

> Modo de uso

```latex
\usepackage{amsmath,amsthm,amsfonts,amssymb,dsfont,mathtools}
```

##### ~={cyan}Trabalhando com elementos matemáticos simples=~

```tex
Sinal de Soma: + ou $+$\\
Sinal de Subtração: - ou $-$\\
Sinal de Multiplicação: x.y ou $x.y$\\
% Usando a forma com Times que é o mesmo que Vezes (X) pra gente
Sinal de Multiplicação: $\times$\\
Sinal de Multiplicação: $\cdot$\\
Sinal de Divisão: / ou $\frac{x}{y}$\\ % Numeros com metade do tamanho da fonte original
Sinal de Divisão: $/$
Sinal de Divisão: $\dfrac{x}{y}$\\ % Numeros de mesmo tamanho que a fonte original
Sinal de Divisão: $x\div y$
```

##### ~={cyan}Trabalhando com Parenteses, Colchetes e Chaves=~

```tex
Parenteses 1: $\dfrac{x}{y}$\\
Parenteses 2: ($\dfrac{x}{y}$)\\
Parenteses 3: $\left(\dfrac{x}{y} \right)$\\
Parenteses 3: $\left(\dfrac{x+z \left( a\cdot b \right)}{y} \right)$\\

Colchetes 1: $\left[\dfrac{x+z \left( a\cdot b \right)}{y} \right]$\\

Chaves 1: $\left \{ \dfrac{x+z \left( a\cdot b \right)}{y} \right \}$\\
```

##### ~={cyan}Trabalhando com Potência e Radiciação=~

```tex
Potência 1: $a^n$\\
\\
Potência 2: $a^{b + (c \cdot d)}$\\
\\
Radiciação 1: $\sqrt{16}$\\
\\
Radiciação 2: $\sqrt[3]{8}$\\
\\
Radiciação 3: $\sqrt[n]{a +b+c+d}$\\
\\
% O 2 marca uma altura
Radiciação 4: $\sqrt{\vphantom{1}} x$
```

##### ~={cyan}Utilizando Letras Gregas=~

```tex
Alfa: $\alpha$\\
Beta: $\beta$\\
Delta: $\Delta$\\
Delta: $\delta$\\
Sigma: $\sigma$\\
Sigma: $\Sigma$\\
Sigma: $\varsigma$\\
Omega: $\omega$\\
Omega: $\Omega$\\
```

##### ~={cyan}Utilizando Funções Matemáticas Complexas=~

```tex
Se somente se 1: $ \leftrightarrow $\\
Se somente se 2: $ \Leftrightarrow $\\
Se somente se 3: $ \longleftrightarrow $\\
Negação Lógica: $ \neg p $\\
União: $ \cup $\\
União: $ \bigcup $\\
Integral Tripla: $\iiint f(x,y,z) dxdydz$\\
Integral Dupla: $ \iint $\\
Derivada: $\frac{d}{dx}f(x)$ ou $f'(x)$\\
Limite: $\lim_{x\to a} f(x)$
```

##### ~={cyan}Setas=~

```tex
Esquerda: $ \leftarrow $\\
Direita: $ \rightarrow $
```

##### ~={cyan}Matrizes=~

Matrizes em Latex são semelhantes a tabelas, entretanto o begin que seria da tabela é uma pmatrix para parenteses, ou bmatrix para colchetes. Além disso, devemos colocar o bloco de código da tabela/matriz dentro de um bloco de equation.

```tex
\begin{equation}
    \begin{pmatrix}
        \centering
        \begin{tabular}{cc}
            x & $x^b$\\
            $y+1$ & z
        \end{tabular}
        \label{Matriz Simples}
    \end{pmatrix}
\end{equation}

\begin{equation}
    \begin{bmatrix}
        \centering
        \begin{tabular}{cc}
            x & $x^b$\\
            $y+1$ & z\\
            0 & w+x
        \end{tabular}
        \label{Matriz Simples}
    \end{bmatrix}
\end{equation}
```

##### ~={cyan}Operações entre conjuntos, Somatórios e Produtórios=~

```tex
União: $A \cup B $\\
\\
Interseção: $ D \cap C $\\
\\
Somatório 1: $ \sum $\\
\\
Somatório 2: $ \sum_{x \in A} x$\\
\\
Somatório 3: $ \sum_{i=1}^n i = 1 + 2 + 3  +\ldots + n $\\
\\
Produtório 1: $ \prod $\\
\\
Produtório 2: $ \prod_{i=1}^n i=1 \cdot2\cdot3\ldots n$\\
\\
Produtório 3: $ \prod_{i=1}^5i = 1$\\
```

##### ~={cyan}Displaystyle=~

O comando *"\displaystyle"* é usado para mudar o estilo de exibição de uma expressão matemática, tonando-a maior e mais destacada.

A diferença desses código para os anteriores é que devemo adicionar o comando antes do que será escrito.

```tex
Somatório 3: $ \displaystyle \sum_{i=1}^n i = 1 + 2 + 3  +\ldots + n $\\
Produtório 2: $ \displaystyle \prod_{i=1}^n i=1 \cdot2\cdot3\ldots n$\\
```
##### ~={cyan}Limites, Derivadas e Integrais=~

```tex
Derivadas 1: $f(x) = x^2$ \\
\\
Derivadas 2: $\ \displaystyle \frac{df}{dx} = 2x$\\
\\
Integrais 1: $ \int_a^b f(x)dx$\\
\\
Integrais 2: $ \displaystyle \int_a^b f(x)dx $\\
\\
Integrais 3: $\displaystyle \oint_C \vec{F}\cdot d\vec{r}$\\
\\
Integrais 4: $ \displaystyle \int_{-\infty}^{+\infty} \log_x{F}$\\
\\
Integrais 5: $ \displaystyle \iint_{\sec{x}}^{cossec{x}} x$\\
\\
Limites 1: $ \displaystyle \lim_{x\to 3, y\to2} x+y $\\
\\
Limites 2: $ \displaystyle \lim_{\substack{x \to 0 \\ y \to 1}} f(x,y) $\\
```