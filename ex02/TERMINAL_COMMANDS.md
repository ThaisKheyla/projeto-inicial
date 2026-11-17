# ex02 - Comandos do Terminal

## Objetivo
Criar arquivos com permissões específicas (exo2).

## Comandos Utilizados

### 1. Criar o arquivo test1 com permissões executáveis
```bash
chmod 755 test1
# ou
chmod u=rwx,g=rx,o=rx test1
```

### 2. Criar o arquivo test3 com permissões de leitura/escrita
```bash
chmod 600 test3
# ou
chmod u=rw,g=,o= test3
```

### 3. Criar o arquivo test4 com permissões específicas
```bash
chmod 644 test4
# ou
chmod u=rw,g=r,o=r test4
```

### 4. Criar o arquivo test5 com permissões específicas
```bash
chmod 400 test5
# ou
chmod u=r,g=,o= test5
```

### 5. Criar o arquivo test6 (se necessário)
```bash
chmod 444 test6
# ou
chmod a=r test6
```

### 6. Empacotar os arquivos
```bash
tar -cf exo2.tar test1 test3 test4 test5 test6
```

### 7. Verificar as permissões
```bash
ls -l test*
```

## Resultado
Arquivos com permissões específicas foram criados e empacotados em `exo2.tar`.
