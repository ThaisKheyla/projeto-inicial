# ex04 - Comandos do Terminal

## Objetivo
Criar um comando personalizado `midLS` que executa um comando `ls` com opções específicas.

## Comandos Utilizados

### 1. Criar o arquivo midLS com o comando
```bash
echo 'ls -tmp' > midLS
```

### 2. Tornar o arquivo executável
```bash
chmod +x midLS
```

### 3. Testar o comando personalizado
```bash
./midLS
```

## Conteúdo do Arquivo
O arquivo `midLS` contém:
```bash
ls -tmp
```

## Significado das Opções
- `l` - formato longo (detalhado)
- `t` - ordena por tempo de modificação
- `m` - lista em uma única linha, separada por vírgulas
- `p` - adiciona `/` aos diretórios

### Alternativa: Formato detalhado por linha
```bash
ls -lt
```

## Resultado
Ao executar `./midLS`, o comando lista arquivos com as opções especificadas.
