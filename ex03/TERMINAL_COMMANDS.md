# ex03 - Comandos do Terminal

## Objetivo
Gerar uma chave pública SSH e salvá-la no arquivo `id_rsa_pub`.

## Comandos Utilizados

### 1. Gerar um par de chaves SSH (se necessário)
```bash
ssh-keygen -t rsa -b 4096 -f id_rsa
```
Este comando gera:
- `id_rsa` - chave privada (mantida secreta)
- `id_rsa.pub` - chave pública

### 2. Visualizar a chave pública
```bash
cat id_rsa.pub
```

### 3. Copiar a chave pública para o arquivo solicitado
```bash
cp id_rsa.pub id_rsa_pub
```

### 4. Verificar o conteúdo
```bash
cat id_rsa_pub
```

## Resultado
A chave pública SSH foi salva no arquivo `id_rsa_pub` com formato:
```
ssh-rsa AAAA...
```

## Notas de Segurança
- Nunca compartilhe a chave privada (`id_rsa`)
- A chave pública (`id_rsa_pub`) pode ser compartilhada com servidores SSH
- As chaves são geradas apenas uma vez durante o setup
