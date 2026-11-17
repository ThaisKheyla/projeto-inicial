# ex04

criar um comando personalizado `midLS` que executa `ls -tmp`

```bash
echo 'ls -tmp' > midLS
```

deixar executável:
```bash
chmod +x midLS
```

testar:
```bash
./midLS
```

pronto! comando criado

nota: `ls -tmp` lista arquivos em uma linha separados por vírgula, ordenados por tempo
