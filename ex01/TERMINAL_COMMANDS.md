# ex01 - Comandos do Terminal

## Objetivo
Criar um arquivo com atributos/permissões específicas (testShell00).

## Comandos Utilizados

### 1. Criar o arquivo vazio
```bash
touch testShell00
```

### 2. Ajustar as permissões do arquivo
```bash
chmod 400 testShell00
```
O arquivo fica com permissão de leitura apenas para o proprietário.

### 3. Criar o arquivo tar
```bash
tar -cf testShell00.tar testShell00
```

### 4. Verificar as permissões
```bash
ls -l testShell00
```

## Resultado
O arquivo `testShell00` com permissões de leitura apenas (400) foi criado e empacotado em `testShell00.tar`.
