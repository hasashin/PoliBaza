# __PoliBaza__ - style dla języka LaTeX ułatwiający pisanie sprawozdań i notatek

## Zawartość paczki:
- *poliBase* - styl bazowy, zawierający usprawnienia i nowe komendy ułatwiające pracę z dokumentami na studia
    wszystkie style zawierają styl bazowy.
- *poliNote* - styl do tworzenia notatek z zajęć, zmienia komendę ``\maketitle``, aby tworzyła mały nagłówek tytułowy
- *poliSpr* - styl do tworzenia sprawozdań, zmienia komendę ``\maketitle``, aby stworzyć oficjaną stronę tytułową

## Funkcje
1. Załącza paczki:
    - __adjustbox__ - [Strona paczki](https://ctan.org/pkg/adjustbox)
    - __amsmath__ - [Strona paczki](https://ctan.org/pkg/amsmath)
    - __array__ - [Strona paczki](https://ctan.org/pkg/array)
    - __bera__ - [Strona paczki](https://ctan.org/pkg/bera)
    - __booktabs__ - [Strona paczki](https://ctan.org/pkg/booktabs)
    - __datetime__ - [Strona paczki](https://ctan.org/pkg/datetime)
    - __enumerate__ - [Strona paczki](https://ctan.org/pkg/enumerate)
    - __eurosym__ - [Strona paczki](https://ctan.org/pkg/eurosym)
    - __fancyhdr__ - [Strona paczki](https://ctan.org/pkg/fancyhdr)
    - __fontenc__ - [Strona paczki](https://ctan.org/pkg/fontenc)
    - __geometry__ - [Strona paczki](https://ctan.org/pkg/geometry)
    - __graphicx__ - [Strona paczki](https://ctan.org/pkg/graphicx)
    - __hyperref__ - [Strona paczki](https://ctan.org/pkg/hyperref)
    - __indentfirst__ - [Strona paczki](https://ctan.org/pkg/identfirst)
    - __inputenc__ - [Strona paczki](https://ctan.org/pkg/inputenc)
    - __latexsym__ - [Strona paczki](https://ctan.org/pkg/latexsym)
    - __listings__ - [Strona paczki](https://ctan.org/pkg/listings)
    - __lmodern__ - [Strona paczki](https://ctan.org/pkg/lmodern)
    - __multirow__ - [Strona paczki](https://ctan.org/pkg/multirow)
    - __polski__ - [Strona paczki](https://ctan.org/pkg/polski)
    - __sectsty__ - [Strona paczki](https://ctan.org/pkg/sectsty)
    - __tikz__ - [Strona paczki](https://ctan.org/pkg/tikz)
    - __xcolor__ - [Strona paczki](https://ctan.org/pkg/xcolor)
2. Zmienia:
    - rozmiar komórek tabeli dodając im cięcej odstępu wewnątrz
    - wielkość linii oddzielającej nagłówek i stopkę z paczki __fancyhdr__ na 0pt
    - kolory linków z paczki __hyperref__:
        - link ogólny - czarny
        - link do pliku - czarny
        - link url - niebieski
        - link do cytatu - czarny
    - separator daty z paczki __datetime__ na ``.``
3. Dodaje komendy:
    - ``\centerimage[label]{path/to/image}{caption}``
    
       Komenda wstawia wycentrowany obraz z podpisem. Ta komenda jest zalecana dla zdjęć kwadratowych i pionowych, ponieważ dopasowuje zdjęcie, aby zajmowało około 30% wysokości kartki.
       
       Argumenty
        - _label_ - jest argumentem opcjonalnym. Jeśli jest podany, to zdjęcie będzie posiadało etykietę **zdj:_label_**,
        - _caption_ - jest argumentem wymaganym. Zawarty w nim tekst znajdzie się w podpisie pod zdjęciem. 
        W przypadku podania pustego argumentu podpis nie pojawi się,
        - _path_ - jest argumentem wymaganym. Określa ścieżkę do dodawanego pliku graficznego.

    - ``\centerimagewide[label]{path/to/image}{caption}``
    
       Zaleca się użycie tej komendy, jeśli zdjęcie dodane przez ``\centerimage`` jest zbyt małe lub zbyt szerokie.
       Komenda wstawia wycentrowany obraz z podpisem. Ta komenda dopasowuje zdjęcie, aby zajmowało 70% szerokości kartki.
       
       Argumenty
        - _label_ - jest argumentem opcjonalnym. Jeśli jest podany, to zdjęcie będzie posiadało etykietę **zdj:_label_**,
        - _caption_ - jest argumentem wymaganym. Zawarty w nim tekst znajdzie się w podpisie pod zdjęciem. 
        W przypadku podania pustego argumentu podpis nie pojawi się,
        - _path_ - jest argumentem wymaganym. Określa ścieżkę do dodawanego pliku graficznego.
    - ``\i{tekst}``

       Komenda wyświetla tekst jako pochylony. Alias komendy ``\textit{}``.

       Argumenty
        - _tekst_ - tekst, który będzie pochylony

    - ``\b{tekst}``

       Komenda wyświetla tekst jako pogrubiony. Alias komendy ``\textbf{}``.

       Argumenty
        - _tekst_ - tekst, który będzie pogrubiony
        
    - ``\red{tekst}``

       Komenda koloruje tekst na czerwono. Alias zestawu komend: ``\color{red} tekst \color{black}``.

       Argumenty
        - _tekst_ - tekst, który będzie pokolorowany

    - ``\green{tekst}``

       Komenda koloruje tekst na zielono. Alias zestawu komend: ``\color{green} tekst \color{black}``.

       Argumenty
        - _tekst_ - tekst, który będzie pokolorowany

    - ``\blue{tekst}``

       Komenda koloruje tekst na niebiesko. Alias zestawu komend: ``\color{blue} tekst \color{black}``.

       Argumenty
        - _tekst_ - tekst, który będzie pokolorowany

    - ``\makecopyright{tekst}``

       Komenda tworzy nową stronę z informacją o prawach autorskich na dole strony.

       Argumenty
        - _tekst_ - tekst, który będzie pokazany za znakiem ©
    - ``\makelogotitle``
        
       Komenda tworzy stronę tytułową podobną w oficjalnej formie z logo uczelni

       Argumanty
	    brak
4. Tworzy strony tytułowe komendą ``\maketitle``:
    - __dla notatki__  - strona tytułowa ma formę nagłówka pierwszej strony oddzielonego linią od tekstu. 
    Zawiera tytuł, autora i datę,
    - __dla sprawozdania__ - strona tytułowa ma oficjalną formę z nazwą uczelni, wydziału, instytutu oraz danymi
    autora, tytułem i datą,
    - __dla sprawozdania z logo uczelni__ - strona tytułowa ma oficjalną formę z logo uczelni na górze strony, nazwą uczelni, wydziału
    oraz danymi autora, tytułem i datą. Obrazek logo jest umieszczony w folderze __resources__.

## Instalacja

Sciągnij to repozytorium do katalogu 
```
$(texmfroot)/tex/latex/
```
gdzie ``texmfroot`` to ścieżka do folderu TDS (TeX Directory Structure), która może wyglądać:
- MacOS: ``~/Library/texmf/``
- UNIX/Linux: ``~/texmf``
- Windows: wybrany folder dodany jako TDS

## Użycie

W preambule dokumentu należy dodać odpowiednią paczkę komendą:
```latex
\usepackage{NazwaPaczki}
```
Można opcjonalnie dołączyć paczkę __minted__, za pomocą odpowiedniej opcji _withminded_ w komendzie:
```latex
\usepackage[withminted]{NazwaPaczki}
```
Paczka _minted_ wymaga zainstalowanego interpretera __Python__ wraz z paczką __pygment__ oraz użycia argumentu ```-shell-escape``` 
podczas budowania projektu.