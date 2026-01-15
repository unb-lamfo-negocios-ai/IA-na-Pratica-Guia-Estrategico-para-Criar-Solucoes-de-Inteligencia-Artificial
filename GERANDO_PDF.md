# Como Gerar o PDF do E-book

## Pré-requisitos

1. **Node.js** instalado
2. **Typst** instalado (ferramenta de geração de PDF)

## Instalando o Typst (apenas na primeira vez)

**Opção 1 - Download direto:**
1. Acesse https://github.com/typst/typst/releases
2. Baixe `typst-x86_64-pc-windows-msvc.zip`
3. Extraia o `typst.exe` para uma pasta no PATH (ex: `C:\Users\SeuUsuario\AppData\Local\Programs\typst\`)

**Opção 2 - Via winget:**
```bash
winget install Typst.Typst
```

## Gerando o PDF

1. Abra o terminal na pasta do projeto

2. Execute o comando:
```bash
jupyter-book build --typst
```

3. O PDF será gerado em:
```
exports/book-typst.pdf
```

## Observações

- O processo leva cerca de 30 segundos
- Alguns warnings sobre "Unknown admonition kind" e "grid" são esperados e não afetam o resultado final
- Se aparecer erro sobre um GIF não convertido, instale o [ImageMagick](https://imagemagick.org/script/download.php#windows) (opcional)

## Comando rápido (resumo)

```bash
jupyter-book build --typst
# PDF gerado em: exports/book-typst.pdf
```
