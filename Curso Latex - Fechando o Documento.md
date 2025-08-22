##### ~={cyan}Com criar índices?=~

A inserção do índice pode ser feita em qualquer lugar do documento. Normalmente é feita no preâmbulo.

O comando abaixo cria os índices.

```tex
\tableofcontent
```

##### ~={cyan}Criando uma Capa para o Trabalho=~

Após o begin do documento e antes do maketitle, vamos construir a capa do trabalho. Para ajustar o tamanho, usaremos o comando "LARGE".

```tex
\begin{document}
\LARGE{Titulo do Trabalho}
...
\end{document}
```

Para limitar o tamanho do LARGE, isto é, fazer com que ele só altere o tamanho do título e não interfira em outras partes do texto, basta inserir todo o bloco em parenteses.

```tex
\begin{document}
{\LARGE{Titulo do Trabalho}}
...
\end{document}
```

```tex
\begin{titlepage}
\centering{\LARGE \textbf{{Titulo do Trabalho}}}
\end{titlepage}
```

O nome titlepage não é nenhuma palavra reservada, apenas uma palavra que serve de identificação para a página da capa.

> Código Completo

```tex
\begin{document}
	
	\begin{titlepage}
		\centering
		{\LARGE \textbf{{Titulo do Trabalho}}}\\
		
		\vspace{1cm}
		
		{\Large{Autor do Trabalho}}\\
		
		\vspace{1cm}
		
		{\Large{\textit{Instituição de Ensino}}}
		\vfill
		{\Large{ \textbf{Ano}}}
		
	\end{titlepage}
```

Revisando o código

-  \begin{document} - inicia o documento de texto
-  \begin{titlepage} - inicia a folha de texto e o titlepage é um nome qualquer
-  {\LARGE \textbf{{Titulo do Trabalho}}}\\\ - define apenas o titulo como negrito e em tamanho grande, além de pular uma linha
-  \vspace - cria um espaço de um centimetro entre uma linha e outra
-  {\Large{Autor do Trabalho}}\\\ - define o autor do trabalho, coloca em tamanho grande e pula uma linha
-  {\Large{\textit{Instituicao de Ensino}}} - define o nome da instituição, altera o tamanho e põe em itálico
-  \vfill - coloca o nome do ano no final da página

##### ~={cyan}Página de Dedicatória=~

As principais caracterísitcas de uma página de dedicatória são de que ela está em uma única página, alinhada à direita e em itálico.

```tex
\begin{document}
    \vspace*{\fill}
    \begin{flushright}
        \textit{
            Dedico este trabalho Aos meus familiares, que sempre me apoiaram com amor e compreensão em todos os momentos desta caminhada.
            Aos amigos, pela motivação e pela parceria nos dias mais difíceis.
            E a todos que, de alguma forma, contribuíram para que esta etapa da minha vida fosse concluída com sucesso.
        }
    \end{flushright}
    \vspace*{\fill}
```

-  Nesse código, o * no vspace faz ele se referir à margem superior ao invés do ponto em que o texto está. O parâmetro fill faz o preenchimento até o final da folha (rodapé). O mesmo deve ser feito para a parte inferior.
##### ~={cyan}Cabeçalhos e rodapés=~

A primeira coisa que se deve fazer quando está trabalhando com cabeçalhos é importar o pacote específico.

```tex
\usepackage{fancyhdr} % carrega pacote de Cabeçalho e rodapé
```

-  No preâmbulo do documento, montamos o cabeçalho e o rodapé.

```tex
% iniciar o cabeçalho personalizado
\pagestyle{fancy}
% limpa a formatação de cabeçalho e rodapé existente
\fancyhf{}
% cabeçalho
\fancyhead[L]{leftmark}
\fancyhead[R]{Trabalho}
% rodapé
\fancyfoot[L]{thepage}
```

-  Os parâmetros do fancyhead são, um obrigatório e outro opcional. O primeiro é o item, enquanto o segundo é a posição onde ele ficará.
-  Ao invés de usar uma palavra qualquer, eu posso usar uma palavra reservada *"\\leftmark"* que coloca o nome da seção em que estamos.
-  O rodapé é semelhante, porém o parâmetro obrigatório é o *"\thepage"* que é o número da página (Nesse caso, a linha não é colocada).
-  Para inserir a linha no rodapé deve-se adicionar outro comando no código.

```tex
\fancyfoot[C]{\hrulefill \thepage}
```

##### ~={cyan}Como usar várias formas de numerar página o mesmo documento?=~

-  Importar a biblioteca "*fancyhdr"* - biblioteca para cabeçalhos e rodapé
-  Cria um novo estilo

```tex
\usepackage{fancyhdr}
% Criando um novo estilo
% O valor passado nas chaves é o nome do estilo
\fancypagestyle{arabic}{
	\fancyhf{}                     % Cancela a formatação existente
	\fancyfoot[C]{\thepage}
}
```

-  Assim que o documento começa (no begin), devemos inserir o comando de numeração.

```tex
\begin{document}
	\pagenumbering{arabic}
	\pagestyle{arabic}
```

##### ~={cyan}Adicionando notas de rodapé=~

Para adicionar uma nota de rodapé é bem simples, basta escolher o ponto onde ela deve ser referenciada e colocar o código abaixo

```tex
...\footnote{nota que quer colocar}
```

##### ~={cyan}Formatação de Notas de Rodapé=~

-  setlength com headsep - é a separação do cabeçalho até o corpo do texto;
-  setlength com footnotesep - é a separação das notas de rodapé umas das outras;
-  setlength com footskip - é a separação da nota de rodapé do corpo do texto.

```tex
\usepackage[
lmargin=0cm,
tmargin=1.5cm,
rmargin=0cm,
bmargin=0.0cm
]{geometry} 

\setlength{\headsep}{4cm}
\setlength{\footnotesep}{0cm}
\setlength{\footskip}{0.1cm}
```

##### ~={cyan}Resumo=~

Criando um resumo de um trabalho utilizando a ABNTex2

























