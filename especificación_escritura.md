Guía de Estilo de Escritura para LaTeX

Este documento define el estilo de escritura y las convenciones de formato para su implementación en LaTeX, con el fin de mantener la consistencia, claridad y profesionalismo académico.

1. Tono y Voz
1.1. Tono Formal y Objetivo

El lenguaje debe ser siempre formal, preciso y objetivo. Evite el uso de expresiones coloquiales, opiniones personales o lenguaje vago.

1.2. Voz Impersonal y Tercera Persona

La redacción debe realizarse en tercera persona o utilizando la voz pasiva para mantener un tono impersonal. Se debe evitar estrictamente el uso de la primera persona del singular (yo) o del plural (nosotros).

Incorrecto: Implementamos un prototipo para validar los conceptos...

Correcto: Se realizó la implementación de un prototipo para validar los conceptos...

Incorrecto: En nuestro trabajo, decidimos realizar una revisión sistemática...

Correcto: En este trabajo se presenta una investigación exhaustiva...

2. Formato de Texto y Énfasis (Comandos LaTeX)
2.1. Negrita

Utilice el comando \textbf{texto} para los siguientes casos:

Resaltar términos clave en el momento de su definición o introducción principal.

Ejemplo: El concepto de \textbf{Cloud Manufacturing (CMfg)} es un paradigma que surge...

Identificar etiquetas o títulos dentro de elementos como listas descriptivas.

Ejemplo: \item[\textbf{Título:}] Estado del arte de Cloud Manufacturing.

2.2. Cursiva y Énfasis

Términos en idioma extranjero: Utilice el comando \textit{texto} para palabras que no tienen una traducción estandarizada.

Ejemplo: ...para validar el \textit{framework} de Eclipse BaSyx.

Énfasis en el texto: Para dar un énfasis semántico, es preferible usar \emph{texto}. Este comando es más flexible, ya que anida correctamente (cursiva dentro de cursiva se vuelve texto normal).

Ejemplo: ...actuar, \emph{virtualmente}, como si fuesen empresas grandes.

2.3. Acrónimos

Para una gestión profesional de los acrónimos, se recomienda el paquete acronym.

En el preámbulo: Añadir \usepackage{acronym}.

Definir los acrónimos: Antes de \begin{document}, defina todos los acrónimos que usará.

Generated latex
\acro{CMfg}{Cloud Manufacturing}
\acro{AAS}{Asset Administration Shell}


Uso en el texto: Utilice el comando \ac{<etiqueta>}. LaTeX gestionará automáticamente la primera aparición (escribiendo el nombre completo y el acrónimo) y las siguientes (solo el acrónimo).

Ejemplo: ...el concepto de \ac{CMfg} es un paradigma... El objetivo de \ac{CMfg} es...

3. Convenciones Académicas en LaTeX
3.1. Citas y Bibliografía

Utilice BibTeX o BibLaTeX para gestionar la bibliografía. En el texto, las citas se insertan con el comando \cite{<clave_bib>}.

Cita única: ...comienza a surgir el concepto de “lote de tamaño 1” \cite{shafiq2014implementing}.

Citas múltiples: ...no existe una definición precisa de \ac{CMfg} \cite{adamson2017,henzel2018,ren2015}.

3.2. Notas al Pie

Utilice el comando \footnote{<texto de la nota>} para añadir información complementaria.

Ejemplo: ...validar el \textit{framework}\footnote{Llamamos \textit{framework} a una estructura base que simplifica el desarrollo de un proyecto...} de Eclipse BaSyx.

3.3. Figuras y Tablas

Utilice los entornos flotantes figure y table para que LaTeX maneje su posicionamiento. Para las referencias cruzadas, se recomienda el paquete cleveref (\usepackage{cleveref}).

Epígrafe (Caption): Se genera con el comando \caption{<descripción>}.

Etiqueta y Referencia: Se define con \label{<tipo>:<etiqueta>} y se referencia con \cref{<tipo>:<etiqueta>}.

Ejemplo de código para una figura:

Generated latex
\begin{figure}[ht!] % Posicionamiento sugerido: here, top, definitely!
    \centering
    \includegraphics[width=0.8\textwidth]{figures/modelo_operacion.png}
    \caption{Modelo de operación de fabricación en la nube \cite{liu2019scheduling}.}
    \label{fig:modelo_operacion}
\end{figure}

Como se puede observar en la \cref{fig:modelo_operacion}, el sistema...
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Latex
IGNORE_WHEN_COPYING_END
3.4. Listas

Listas numeradas (enumerate): Para secuencias, pasos de un algoritmo o elementos ordenados.

Generated latex
\begin{enumerate}
    \item Registro de recursos (Resource registration).
    \item Virtualización de recursos (Resource virtualization).
    \item Presentación de requisitos (Requirement submission).
\end{enumerate}
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Latex
IGNORE_WHEN_COPYING_END

Listas con viñetas (itemize): Para elementos sin un orden específico. LaTeX gestiona automáticamente el estilo de las viñetas en listas anidadas.

Generated latex
\begin{itemize}
    \item Congreso XXXIII ENDIO - XXXI EPIO RED-M IX, 2020
    \begin{itemize}
        \item \textbf{Título:} Estado del arte de Cloud Manufacturing.
        \item \textbf{Autores:} Santiago Chiappa, Emiliano Videla...
    \end{itemize}
    \item Digitalización de extremo a extremo.
\end{itemize}