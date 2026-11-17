# ex05

script que mostra os últimos 5 commits do git:

```bash
echo 'git log --format="%H" -n 5' > git_commit.sh
```

deixar executável:
```bash
chmod +x git_commit.sh
```

testar:
```bash
./git_commit.sh
```

vai exibir os 5 últimos commits com seus hashes (SHA-1)

nota: `%H` = hash completo do commit, `-n 5` = últimos 5
