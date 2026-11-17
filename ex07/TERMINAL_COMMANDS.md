# ex07

trabalhar com diffs/patches:

criar arquivo base:
```bash
echo "conteúdo original" > a
```

criar arquivo modificado:
```bash
echo "conteúdo modificado" > b
```

gerar o patch:
```bash
diff -u a b > sw.diff
```

ve o diff:
```bash
cat sw.diff
```

aplicar o patch:
```bash
patch < sw.diff
```

reverter:
```bash
patch -R < sw.diff
```

