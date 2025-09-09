# About
Based off https://www.latextemplates.com/template/friggeri-resume-cv

## Requirements

### Packages
texlive-scheme-basic
texlive-xetex-bin
texlive-euenc
texlive-parskip
texlive-textpos
texlive-lm-math
texlive-tex-gyre

### OSX
Download the full version of MacTex, should have everything you need: http://www.tug.org/mactex/

Ensure `/Library/TeX/texbin` is added to Path.

### Linux

Download and install TeX Live from: https://www.tug.org/texlive/acquire-netinstall.html

```
# this will speed up downloads significantly
sudo dnf install -y perl-libwww-perl perl-LWP-Protocol-https

wget https://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz
tar -xvf install-tl-unx.tar.gz 
sudo ./install-tl-*/install-tl --persistent-downloads --no-interaction --profile $RESUME_REPO_DIR/texlive-install.profile 

tlmgr search --global --file textpos.sty

sudo /usr/local/bin/tlmgr install textpos collection-fontsrecommended

sudo dnf install texlive texlive-xetex texinfo-tex texlive-scheme-basic texlive-euenc texlive-parskip texlive-textpos texlive-lm-math texlive-tex-gyre
```

## Generating pdf
xelatex resume.tex
