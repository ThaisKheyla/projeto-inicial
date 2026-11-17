# Avaliação Shell 00

## ex00
```bash
cat z
# deve exibir: Z
```

## ex01
```bash
ls -l testShell00
# deve ter permissão: -r-------- (400)
tar -tf testShell00.tar
# deve conter: testShell00
```

## ex02
```bash
ls -l test*
# test1: -rwxr-xr-x (755)
# test3: -rw------- (600)
# test4: -rw-r--r-- (644)
# test5: -r-------- (400)
# test6: -r--r--r-- (444)
tar -tf exo2.tar
# deve conter todos os test files
```

## ex03
```bash
cat id_rsa_pub
# deve começar com: ssh-rsa AAAA...
file id_rsa_pub
# deve reconhecer como OpenSSH public key (ou similar)
```

## ex04
```bash
./midLS
# deve executar sem erro
cat midLS
# deve conter: ls -tmp
```

## ex05
```bash
./git_commit.sh
# deve exibir hashes dos commits (SHA-1)
head -c 40 git_commit.sh
# deve conter: git log --format="%H" -n 5
```

## ex06
```bash
./git_ignore.sh
# deve exibir arquivos ignorados
grep -q "git ls-files" git_ignore.sh
# deve ter o comando git ls-files
```

## ex07
```bash
cat sw.diff
# deve ter formato unificado (--- a +++ b)
test -f a && test -f b
# deve ter os dois arquivos
```

## ex08
```bash
./clean
# executar (vai deletar temporários se houver)
head -c 60 clean
# deve conter: find . -type f
```

## ex09
```bash
cat ft_magic
# deve conter: 41 string 42
file -m ft_magic teste_42
# deve reconhecer o arquivo
```
