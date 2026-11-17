# ex09 - Comandos do Terminal

## Objetivo
Criar um arquivo magic que define um tipo de arquivo personalizado.

## Comandos Utilizados

### 1. Criar o arquivo ft_magic
```bash
echo '41 string 42 42 file' > ft_magic
```

### 2. Verificar o conteúdo
```bash
cat ft_magic
```

### 3. Testar o arquivo magic com o comando file
```bash
# Com arquivo magic customizado
file -m ft_magic teste_42

# Ou usando diretamente
file -m ft_magic seu_arquivo
```

## Conteúdo do Arquivo Magic
O arquivo `ft_magic` contém:
```
41 string 42 42 file
```

## Significado da Definição Magic
- `41` - offset em bytes (posição 41 no arquivo)
- `string` - tipo de dado a verificar (string/texto)
- `42` - valor procurado (a string "42")
- `42 file` - descrição mostrada (pode ser customizada)

## Formato Geral do Magic File
```
offset  type    value       description
```

## Exemplos de Uso

### Teste com arquivo que contém "42" na posição 41
```bash
file -m ft_magic teste_42
# Resultado: teste_42: 42 file
```

### Criar um arquivo de teste
```bash
# Criar arquivo com "42" na posição 41
printf "%.0s#" {1..40}42 > teste_42
file -m ft_magic teste_42
```

## Alternativas de Magic File
```bash
# Verificar no começo do arquivo
0 string 42 42 file

# Verificar com expressão regular
0 regex ^42 "42 file"

# Múltiplos padrões
0 string ELF ELF executable
```

## Resultado
O arquivo magic permite identificar tipos de arquivo personalizados com base em padrões de conteúdo.

## Notas
- Magic files são usados pelo comando `file` para identificar tipos
- O arquivo magic padrão está em `/etc/magic`
- Arquivos magic customizados podem ser criados e usados com `file -m`
