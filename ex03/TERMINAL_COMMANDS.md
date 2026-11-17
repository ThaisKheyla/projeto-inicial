# ex03

gerar chave SSH:

```bash
ssh-keygen -t rsa -b 4096 -f id_rsa
```

vai criar:
- `id_rsa` (privada - nunca compartilha!)
- `id_rsa.pub` (pública - pode compartilhar)

copiar a pública pro arquivo solicitado:
```bash
cp id_rsa.pub id_rsa_pub
```

ve se tá lá:
```bash
cat id_rsa_pub
```

