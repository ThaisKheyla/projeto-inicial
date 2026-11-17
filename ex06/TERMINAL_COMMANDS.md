# ex06 - Comandos do Terminal

## Objetivo
Criar um script Bash `git_ignore.sh` que lista arquivos ignorados pelo Git.

## Comandos Utilizados

### 1. Criar o arquivo git_ignore.sh
```bash
echo 'git ls-files --others --ignored --exclude-standard' > git_ignore.sh
```

### 2. Tornar o script executável
```bash
chmod +x git_ignore.sh
```

### 3. Testar o script
```bash
./git_ignore.sh
```

## Conteúdo do Script
O arquivo `git_ignore.sh` contém:
```bash
#!/bin/bash
git ls-files --others --ignored --exclude-standard
```

## Significado do Comando Git
- `git ls-files` - lista arquivos rastreados pelo Git
- `--others` - inclui arquivos não rastreados
- `--ignored` - inclui apenas arquivos ignorados
- `--exclude-standard` - usa as regras do `.gitignore` padrão

## Resultado
O script lista todos os arquivos que são ignorados pelo Git de acordo com o `.gitignore`:
```
mywork.c~
.DS_Store
*~
#*#
```

## Alternativas
```bash
# Listar apenas arquivos não rastreados
git ls-files --others --exclude-standard

# Mostrar status com arquivos ignorados
git status --ignored
```

## Notas
- Os arquivos listados não serão commitados no Git
- Padrões de ignore são definidos no arquivo `.gitignore`
