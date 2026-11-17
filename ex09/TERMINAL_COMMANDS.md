# ex09

criar um arquivo magic que identifica tipo de arquivo personalizado:

```bash
echo '41 string 42 42 file' > ft_magic
```

ve se tá lá:
```bash
cat ft_magic
```

testar com o comando file:
```bash
file -m ft_magic teste_42
```

vai procurar pela string "42" na posição 41 do arquivo

nota:
- `41` = posição/offset no arquivo
- `string` = tipo de dado (procura por texto)
- `42` = o valor que procura
- `42 file` = descrição que mostra (pode customizar)
