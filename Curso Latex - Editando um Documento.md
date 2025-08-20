##### ~={cyan}Como funciona o Geometry?=~

O pacote geometry serve para defnirmos o tipo de folha e layout em que o trabalho será criado (margens).

> Exemplo

```tex
\documentclass{article}
% Configurando o pacote
\usepackage[a4paper, top=2cm, bottom=2cm,left=3cm, right=3cm ]{geometry}
```

```tex
\documentclass{article}
\usepackage{graphicx} % Required for inserting images

% Pacote de geometria para layout
% Pacote lipsum para geração de texto
\usepackage[a4paper, top=3cm, left=3cm, bottom=2cm, right=2cm]{geometry}
\usepackage{lipsum}

\title{Parte 3}
\author{Josué Júnior}
\date{August 2025}
```

##### ~={cyan}Tipos de fontes=~

-  Definindo o tamanho da fonte principal

```tex
\documentclass[10pt]{article}
```

-  Definindo o tamanho da fonte temporariamente 

O primeiro número define o tamanho da fonte em pontos tipográficos (pt), o segundo é a altura da linha, ou seja, o "espaçamento entre linhas do paragráfo", normalmente é um pouco maior que o primeiro valor. O comando "\selectfont" é obrigatório para aplicar as mudanças.

```tex
\fontsize{20}{20}\selectfont
```

-  Outros tamanhos de fontes do menor para o maior.

<div style="width: 70%; margin: auto; font-family: Arial, sans-serif;">
  <h5 style="text-align:center;">Tamanhos de Fonte no LaTeX</h5>
  <table border="1" cellspacing="0" cellpadding="8" style="width:100%; border-collapse:collapse; text-align:center;">
    <thead style="background:#000080;">
      <tr>
        <th>Comando</th>
        <th>Tamanho aproximado (base 10pt)</th>
        <th>Uso comum</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>\tiny</td>
        <td>≈ 5pt</td>
        <td>Texto mínimo, raramente usado</td>
      </tr>
      <tr>
        <td>\scriptsize</td>
        <td>≈ 7pt</td>
        <td>Índices, legendas pequenas</td>
      </tr>
      <tr>
        <td>\footnotesize</td>
        <td>≈ 8pt</td>
        <td>Notas de rodapé</td>
      </tr>
      <tr>
        <td>\small</td>
        <td>≈ 9pt</td>
        <td>Texto menor que o normal</td>
      </tr>
      <tr style="background:#2F4F4F;">
        <td>\normalsize</td>
        <td>≈ 10pt</td>
        <td>Tamanho padrão do documento</td>
      </tr>
      <tr>
        <td>\large</td>
        <td>≈ 12pt</td>
        <td>Títulos menores, destaques</td>
      </tr>
      <tr>
        <td>\Large</td>
        <td>≈ 14pt</td>
        <td>Seções e subtítulos</td>
      </tr>
      <tr>
        <td>\LARGE</td>
        <td>≈ 17pt</td>
        <td>Títulos principais</td>
      </tr>
      <tr>
        <td>\huge</td>
        <td>≈ 20pt</td>
        <td>Capítulos, destaque forte</td>
      </tr>
      <tr>
        <td>\Huge</td>
        <td>≈ 25pt</td>
        <td>Destaques muito grandes</td>
      </tr>
    </tbody>
  </table>
</div>

----

<mark style="background: #BBFABBA6;">Ok, mas e como fazer quando um documento tem que ter um layout diferente dos definidos?</mark>

Para resolver esse processo é simples, basta utilizar o código abaixo que cria uma nova geometria e em seguida restaura para a principal.

```tex
\newgeometry{top=1cm, bottom=5cm, right=2.5cm, left=3.5cm}
\section{Desenvolvimento}
\lipsum{25-30}
\restoregeometry{}
```

---
##### ~={cyan}Quebras de linha no documento=~

A quebra de linha basicamente é quando queremos pula uma linha/ir direto para linha seguinte, para fazer isso, podemos usar o seguinte comando.

-  New Line

Esse comando quebra a linha dentro de um parágrafo. (Não quebra o parágrafo), ou seja, o parágrafo continua o mesmo.

```tex
\section{introducao}
 Sed ante tellus, tristique ut, iaculis eu, malesuada ac, dui. Mauris nibh leo, facilisis non, adipiscing quis, ultrices a, dui.
Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Donec odio elit, dictum in, \newline hendrerit sit amet, egestas
sed, leo. Praesent feugiat sapien aliquet odio. Integer vitae justo. Aliquam vestibulum fringilla lorem. Sed neque lectus, consectetuer at, consectetuer
sed, eleife
...
```

-  Line break

Esse comando é usado para forçar uma quebra de linha sem criar uma nova seção. Ele será usado para evitar que uma palavra quebre no final da linha.

```tex
\section{introducao}
 Sed ante tellus, tristique ut, iaculis eu, malesuada ac, dui. Mauris nibh leo, facilisis non, adipiscing quis, ultrices a, dui.
Pellentesque \linebreak habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Donec odio elit, dictum in, hendrerit sit amet, egestas
sed, leo. Praesent feugiat sapien aliquet odio. Integer vitae justo. Aliquam vestibulum fringilla lorem. Sed neque lectus, consectetuer at, consectetuer
sed, eleife
```

Um fato importante é que o linebreak quebra a linha e justifica o que restou, não deixando espaços. Já o anterior, newline, deixa espaços.

-  Par

O comando par força o ínicio de um novo parágrafo e com isso também faz a quebra de linha.

```tex
\section{introducao}
Donec odio elit, dictum in, hendrerit sit amet, egestas
sed, leo. Praesent feugiat sapien aliquet odio. Integer vitae justo. \par Aliquam vestibulum fringilla lorem. Sed neque lectus, consectetuer at, consectetuer
sed, eleife
```

-  Vspace

O vspace é o valor de espaçamento que é um comando usado para inserir um espaço vertical de alguns centímetros que é usado para quebrar linhas.

```tex
\section{introducao}
Donec odio elit, dictum in, hendrerit sit amet, egestas
sed, leo. Praesent feugiat sapien aliquet odio. Integer vitae justo. \vspace{2cm} Aliquam vestibulum fringilla lorem. Sed neque lectus, consectetuer at, consectetuer
sed, eleife
```

-  Hfill e Hbreak (combinados)

Esses comandos são usados para criar uma linha e preencher a linha com um espaço em branco

```tex
\section{introducao}
Donec odio elit, dictum in, hendrerit sit amet, egestas
sed, leo. Praesent feugiat sapien aliquet odio. Integer vitae justo. \fill \break Aliquam vestibulum fringilla lorem. Sed neque lectus, consectetuer at, consectetuer
sed, eleife
```

##### ~={cyan}Invertendo margens de páginas pares e ímpares=~

Para inverter as margens em páginas pares e ímpares basta utilizar o código abaixo.

```LaTex
\geometry{
	twoside % inverte as margens (esquerda e direita) nas páginas pares e ímpares 
}
```

Eu posso definir a inversão de margens apenas em uma única seção, basta fazer o seguinte.

```tex
\newgeometry{top=1cm, bottom=1cm, left=1cm, right=1cm}
\section{Desenvolvimento}
\lipsum[25-18]
\restoregeometry
```

