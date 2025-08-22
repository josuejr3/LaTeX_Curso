##### ~={cyan}Como criar uma tabela?=~

-  Criar ambiente de tabela

```tex
\begin{table}[]                 % Inicio da tabela
    \centering                  % centraliza a tabela
    \begin{tabular}{c|c}        % inicia a estrutura de linhas e colunas
         &  \\
         & 
    \end{tabular}               % finaliza a estrutura de linhas e colunas
    \caption{Caption}           % legenda da tabela
    \label{tab:placeholder}     % como se referir a tabela mais tarde
\end{table}                     % Final da tabela
```

-  O {c | c} indica que temos uma tabela de duas colunas, o c significa que o valor está centralizado
-  O & indica uma célula "&" outra célula

```tex
\begin{table}[]                 % Inicio da tabela
    \centering                  % centraliza a tabela
    \begin{tabular}{c|c|c}        % inicia a estrutura de linhas e colunas
        valor1 & valor2 & valor5 \\
        valor3 & valor4 & valor6
    \end{tabular}               % finaliza a estrutura de linhas e colunas
    \caption{Caption}           % legenda da tabela
    \label{tab:placeholder}     % como se referir a tabela mais tarde
\end{table}                     % Final da tabela
```

-  Para adicionar as bordas externas e internas horiziontais, basta usar o comando de *"hline"* no local em que se deseja a linha.

```tex
\begin{table}[]                 % Inicio da tabela
    \centering                  % centraliza a tabela
    \begin{tabular}{|c|c|c|}        % inicia a estrutura de linhas e colunas
        \hline
        valor1 & valor2 & valor5 \\
        \hline
        valor3 & valor4 & valor6 \\
        \hline
    \end{tabular}               % finaliza a estrutura de linhas e colunas
    \caption{Caption}           % legenda da tabela
    \label{tab:placeholder}     % como se referir a tabela mais tarde
\end{table}                     % Final da tabela
```

-  Para fazer bordas duplas, basta adicionar dois *"|"* ou dois "/hline"
##### ~={cyan}Como criar tabelas com bordas parciais?=~

-  O comando *"\cline{1-2}"* cria uma linha horizontal parcial entre as celulas 1 e 2.

```tex
\begin{table}[]                 % Inicio da tabela
    \centering                  % centraliza a tabela
    \begin{tabular}{c|c|c}        % inicia a estrutura de linhas e colunas
        valor1 & valor2 & valor5 \\
        \cline{1-2}
        valor3 & valor4 & valor6 \\
        \cline{3-3}
        valor8 & valor9 & valor7
    \end{tabular}               % finaliza a estrutura de linhas e colunas
    \caption{Caption}           % legenda da tabela
    \label{tab:placeholder}     % como se referir a tabela mais tarde
\end{table}                     % Final da tabela
```
##### ~={cyan}Como criar uma linha vertical?=~

Semlhante ao comando de criação de linha horizontal, o comando de linha vertical é usado entre uma coluna e outra.

```tex
valor1 \vline valor2
```
##### ~={cyan}Aplicando legendas, rótulos e referências à cada uma das tabelas=~

Quando estruturamos cada uma das tabelas, vimos que todas possuem em sua estrutura um label e um caption, o primeiro como sendo o nome ou referencia ao objeto no documento, enquanto que o segundo se refere a legenda.

```tex
...\ref{tab:nome_referencia_no_doc}
```
##### ~={cyan} Como aumentar a altura de uma linha?=~

A altura da linha pode ser definida em termos de ex ou cm, e é definida após a quebra de linha

```tex
\begin{table}[]
    \centering
    \begin{tabular}{c|c}
        1 & 2 \\
        \hline
        3 & 4 \\[0.8ex] % <<<<<<<<<<<<<<<<<<<<
        \hline
    \end{tabular}
    \caption{Caption}
    \label{tab:placeholder}
\end{table}
```

-  Para girar uma tabela, precisamos usar um pacote chamado *"/usepackages{rotating}"*
-  E no lugar do begin ter como parâmetro obrigatório uma table, deve ser uma *"sidewaystable"*.

<mark style="background: #BBFABBA6;">Obs</mark>

Apesar da tabela ficar rotacionada, ela ocupará uma página inteira.
##### ~={cyan}Tabela com Células Mescladas=~

Para mesclar tabelas usaremos o comando multicolumn. Esse comando possui três parâmetros, na ordem temos.

- Número das colunas que vão ser mescaladas;
- Formatação, como por exemplo centralizado;
- Conteúdo

```tex
\begin{table}[]
    \centering
    \begin{tabular}{c|c|c}
        \hline
        valor1 & valor2 & valor5  \\
        \hline
        valor3 & valor4 & valor6 \\
        \hline
        \multicolumn{3}{c}{Total}
    \end{tabular}
    \caption{Caption}
    \label{tab:placeholder}
\end{table}
```

##### ~={cyan}Listas de Tabelas=~

Para criar uma lista de tabelas, basta utilizar o comando de *"listoftables"*.

```tex
\section{Indice de Tabelas}
\listoftables
\cleardoublepage
```

Para remover-mos o "list of tables" usamos o seguinte código antes do \listoftables

```tex
\renewcommand{\listoftables}{}
```

##### ~={cyan}Table Generator=~

O Table Generator é uma ferramenta online que serve para criar códigos de tabelas para o Latex.

> Link

[[https://www.tablesgenerator.com |Table Generator]]


