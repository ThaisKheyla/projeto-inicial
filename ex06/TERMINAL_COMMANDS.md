# ex06

script que mostra os arquivos ignorados pelo git:

```bash
echo 'git ls-files --others --ignored --exclude-standard' > git_ignore.sh
```

deixar executável:
```bash
chmod +x git_ignore.sh
```

testar:
```bash
./git_ignore.sh
```

vai listar todos os arquivos que git ignora (definidos no .gitignore)

nota: `--others` = arquivos não rastreados, `--ignored` = só ignorados, `--exclude-standard` = usa regras do .gitignore
