# ex05 - Comandos do Terminal

## Objetivo
Criar um script Bash `git_commit.sh` que lista os últimos commits do git.

## Comandos Utilizados

### 1. Criar o arquivo git_commit.sh
```bash
echo 'git log --format="%H" -n 5' > git_commit.sh
```

### 2. Tornar o script executável
```bash
chmod +x git_commit.sh
```

### 3. Testar o script
```bash
./git_commit.sh
```

## Conteúdo do Script
O arquivo `git_commit.sh` contém:
```bash
#!/bin/bash
git log --format="%H" -n 5
```

## Significado do Comando Git
- `git log` - mostra o histórico de commits
- `--format="%H"` - exibe apenas o hash completo (SHA-1) dos commits
- `-n 5` - limita a 5 últimos commits

## Resultado
O script exibe os 5 últimos commits com seus hashes:
```
abc123def456...
def456ghi789...
...
```

## Alternativas
```bash
# Mostrar os últimos 10 commits
git log --format="%H" -n 10

# Mostrar commits com mensagem
git log --format="%H %s" -n 5

# Mostrar commits em formato oneline
git log --oneline -n 5
```
