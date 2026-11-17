# ex08 - Comandos do Terminal

## Objetivo
Criar um script que limpa arquivos temporários usando o comando `find`.

## Comandos Utilizados

### 1. Criar o arquivo clean (script de limpeza)
```bash
echo 'find . -type f \( -name "*~" -o -name "#*#" \) -print -delete' > clean
```

### 2. Tornar o script executável
```bash
chmod +x clean
```

### 3. Testar o script
```bash
./clean
```

## Conteúdo do Script
O arquivo `clean` contém:
```bash
find . -type f \( -name "*~" -o -name "#*#" \) -print -delete
```

## Significado do Comando Find
- `find .` - busca no diretório atual e subdiretórios
- `-type f` - encontra apenas arquivos (não diretórios)
- `-name "*~"` - encontra arquivos terminados em `~` (backups do editor)
- `-o` - operador OR (ou)
- `-name "#*#"` - encontra arquivos que começam e terminam com `#` (backups do Emacs)
- `-print` - exibe os arquivos encontrados
- `-delete` - deleta os arquivos encontrados

## Resultado
O script encontra e deleta todos os arquivos temporários:
- Backups de editor (ex: arquivo.txt~)
- Backups do Emacs (ex: #arquivo.txt#)

## Precauções
```bash
# Teste sem deletar antes (removendo -delete)
find . -type f \( -name "*~" -o -name "#*#" \) -print

# Ou use -delete com confirmação
find . -type f \( -name "*~" -o -name "#*#" \) -print -ok rm {} \;
```

## Alternativas
```bash
# Apenas arquivos terminados em ~
find . -type f -name "*~" -delete

# Com diretórios específicos
find /tmp -type f -name "*~" -delete
```
