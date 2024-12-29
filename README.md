# edu-book :: A Simple and Obvious Latex Textbook Maker

## Description:
The edu-book LaTeX Style Package was designed to simplify the creation of textbooks 
for educational and academic purposes. The package includes pre-defined commands 
and layouts to streamline common tasks such as importing content from external files, 
creating chapters with labeled headers, and embedding visual elements like figures, 
diagrams, and tables.

It provides specialized tools for generating title pages, shaded text areas for 
emphasis, and integrates seamlessly with common file types (e.g., CSV for tables, 
TikZ for diagrams, and PNG for images). The framework relies on global parameters 
to standardize configurations for file types, extensions, and locations, ensuring 
a consistent and efficient workflow for authors.

The focus is on simplicity and obviousness ensuring that users—whether manually editing 
or leveraging AI outputs—can maintain a polished, professional appearance with minimal effort. 

## Getting Started:

```
\documentclass{book}
\usepackage{edu-book}
\usepackage{natbib}

\pgfkeys{
    /params/.is family,
    /params/.cd,
    %
        % Book
        book/title/.initial     = Book Title,
        book/subtitle/.initial  = Book running title,
    %
        % Author
        author/.initial             = Author's Name, 
        author/title/.initial       = Author's Title,
        author/affiliation/.initial = Author's Institution,
        author/email/.initial       = ,
}


\begin{document}
\sloppy

\TitlePage
\Chapter[title=Hello World]{ch01}

\bibliographystyle{plain}
\bibliography{references}
\end{document}

```

## Example:

This is the resulting document from [main.tex](./main.tex) ([PDF](./main.pdf) attached)

![Animated GIF of main.pdf](images/main.gif)


