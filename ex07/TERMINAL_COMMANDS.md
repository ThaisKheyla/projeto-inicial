# ex07 - Comandos do Terminal

## Objetivo
Trabalhar com diffs e patches no Git.

## Comandos Utilizados

### 1. Criar um arquivo base (a)
```bash
echo "conteúdo original" > a
```

### 2. Criar um arquivo modificado (b)
```bash
echo "conteúdo modificado" > b
```

### 3. Gerar um patch/diff
```bash
diff -u a b > sw.diff
# ou
diff -Naur a b > sw.diff
```

### 4. Visualizar o conteúdo do diff
```bash
cat sw.diff
```

### 5. Aplicar um patch
```bash
patch < sw.diff
```

### 6. Reverter o patch
```bash
patch -R < sw.diff
```

## Conteúdo do Arquivo b (resultado esperado)
O arquivo `b` contém as mudanças em relação ao arquivo `a`.

## Formato do Diff
O arquivo `sw.diff` segue o formato unificado:
```
--- a	2024-01-01 12:00:00.000000000 +0000
+++ b	2024-01-01 12:00:01.000000000 +0000
@@ -1 +1 @@
-conteúdo original
+conteúdo modificado
```

## Alternativas
```bash
# Diff recursivo para diretórios
diff -Naur dir1/ dir2/ > output.diff

# Aplicar patch com verbosidade
patch -p0 -v < sw.diff

# Verificar se patch pode ser aplicado
patch --dry-run < sw.diff
```

## Resultado
O arquivo `sw.diff` contém as diferenças entre os arquivos `a` e `b`.
