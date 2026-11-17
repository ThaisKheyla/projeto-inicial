# ex08

script que limpa arquivos temporários (terminados em ~ e #...#):

```bash
echo 'find . -type f \( -name "*~" -o -name "#*#" \) -print -delete' > clean
```

deixar executável:
```bash
chmod +x clean
```

testar:
```bash
./clean
```

vai procurar e deletar arquivos temporários

nota: 
- `-type f` = apenas arquivos
- `*~` = backups de editor (arquivo.txt~)
- `#*#` = backups do Emacs (#arquivo.txt#)
- `-delete` = deleta os encontrados
