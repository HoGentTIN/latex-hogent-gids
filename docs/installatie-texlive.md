# TeX live

[TeX live](https://tug.org/texlive/) is tegenwoordig de standaard LaTeX-distributie voor de meeste Linux-distributies en kan ook op Windows geïnstalleerd worden.

## Installatie

=== "Windows"

    ```console
    choco install texlive --params="'/collections:xetex'"
    ```

=== "Debian/Ubuntu"

    ```console
    sudo apt install texlive-base texlive-latex-base texlive-latex-recommended texlive-bibtex-extra texlive-pictures texlive-fonts-recommended
    ```

=== "RedHat/Fedora/SuSE"

    ```console
    sudo dnf install 
    ```
