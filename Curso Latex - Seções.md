##### ~={cyan}Divisão do Documento=~

Um documento pode ser dividido em diversas partes no latex, quando nós criamos um projeto em branco a primeira que vemos é a seção de introdução. Entretanto, além da seção temos as seguintes divisões (do maior para o menor).

-  Part

```tex
\part{Parte 1}
```

-  Capítulo

```tex
\chapter{Capítulo 1}
```

-  Seção

```tex
\section{Introducao}
```

-  Subseção

```Tex
\subsection{SubSeção}
```

-  Subsubseção

```tex
\subsubsection{SubSubSection}
```

-  Parágrafo

```tex
\paragraph{Parágrafo}
```

-  Subparágrafo

```tex
\subparagraph{Sub Paragrafo}
```

Uma observação importante é que ao usarmos um * depois do comando *section* e antes dos parâmetros, a enumeração é excluída.

```tex
\part{Parte 1}
    \chapter{Capitulo 1}
        \section*{Introdução} % ---------------------> AQUI !
            \subsection{SubSeção}
                \subsubsection{Sub sub seção}
                    \paragraph{Paragrafo}
                        \subparagraph{sub paragrafo}
        \section{Resumo}
        \section*{Metodos} % ---------------------> AQUI !
        \section{Resultados}
    \chapter{Capitulo 2}
```







