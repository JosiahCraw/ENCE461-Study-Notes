FROM blang/latex:ctanfull

RUN tlmgr option repository ftp://tug.org/historic/systems/texlive/2017/tlnet-final
RUN tlmgr update --self
RUN tlmgr install beamer

CMD latexmk -pdf *.tex

