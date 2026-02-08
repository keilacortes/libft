<div align="center">
  <img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/a2544ce9-f5cf-40e2-afc6-40c796e968de"/>
</div>

# 📚 Libft - 42sp

> *Sua biblioteca C personalizada com funções essenciais*

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![42sp](https://img.shields.io/badge/42sp-000000?style=for-the-badge&logo=42&logoColor=white)
![Licença: MIT](https://img.shields.io/badge/Licença-MIT-9c42f5?style=for-the-badge)

Libft é o primeiro projeto principal da 42, onde criamos nossa própria biblioteca C do zero. Esta biblioteca reimplementa funções padrão do C e adiciona utilitários úteis que serão usados ao longo do currículo da 42.


## 🎯 Objetivo do Projeto

Este projeto consolida conhecimentos fundamentais em programação C, abordando:
- **Lógica de programação** com estruturas de controle e manipulação de dados
- **Ponteiros e memória** através de alocação dinâmica e conceitos de stack/heap
- **Organização de código** com protótipos de funções e bibliotecas estáticas
- **Automação** com criação de Makefiles
- **Testes e debug** identificando e prevenindo vazamentos de memória
- **(Bônus)** Estruturas de dados com listas encadeadas

## 📋 Funções Implementadas

### 🔤 Funções de Caracteres
| Função | Descrição | Categoria |
|--------|-----------|-----------|
| `ft_isalpha` | Verifica se é letra | Classificação |
| `ft_isdigit` | Verifica se é dígito | Classificação |
| `ft_isalnum` | Verifica se é alfanumérico | Classificação |
| `ft_isascii` | Verifica se é ASCII | Classificação |
| `ft_isprint` | Verifica se é imprimível | Classificação |
| `ft_toupper` | Converte para maiúsculo | Conversão |
| `ft_tolower` | Converte para minúsculo | Conversão |

### 📝 Funções de Strings
| Função | Descrição | Categoria |
|--------|-----------|-----------|
| `ft_strlen` | Tamanho da string | Medição |
| `ft_strchr` | Encontra primeira ocorrência | Busca |
| `ft_strrchr` | Encontra última ocorrência | Busca |
| `ft_strncmp` | Compara n caracteres | Comparação |
| `ft_strnstr` | Localiza substring | Busca |
| `ft_strdup` | Duplica string | Alocação |
| `ft_substr` | Extrai substring | Manipulação |
| `ft_strjoin` | Concatena strings | Manipulação |
| `ft_strtrim` | Remove caracteres das extremidades | Manipulação |
| `ft_split` | Divide string por delimitador | Manipulação |
| `ft_strmapi` | Aplica função a cada caractere | Transformação |
| `ft_striteri` | Aplica função a cada caractere (in-place) | Transformação |
| `ft_strlcpy` | Copia com limite de tamanho | Cópia |
| `ft_strlcat` | Concatena com limite de tamanho | Cópia |

### 🧠 Funções de Memória
| Função | Descrição | Categoria |
|--------|-----------|-----------|
| `ft_memset` | Preenche memória com valor | Manipulação |
| `ft_bzero` | Zera região de memória | Manipulação |
| `ft_memcpy` | Copia região de memória | Cópia |
| `ft_memmove` | Move região de memória (sobreposição segura) | Cópia |
| `ft_memchr` | Encontra caractere na memória | Busca |
| `ft_memcmp` | Compara regiões de memória | Comparação |
| `ft_calloc` | Aloca e zera memória | Alocação |

### 🔢 Funções de Conversão
| Função | Descrição | Categoria |
|--------|-----------|-----------|
| `ft_atoi` | Converte string para inteiro | String→Número |
| `ft_itoa` | Converte inteiro para string | Número→String |

### 📤 Funções de Output
| Função | Descrição | Categoria |
|--------|-----------|-----------|
| `ft_putchar_fd` | Escreve caractere no file descriptor | Escrita |
| `ft_putstr_fd` | Escreve string no file descriptor | Escrita |
| `ft_putendl_fd` | Escreve string + nova linha no fd | Escrita |
| `ft_putnbr_fd` | Escreve número no file descriptor | Escrita |

### 🔗 Listas Encadeadas (Bônus)
| Função | Descrição | Categoria |
|--------|-----------|-----------|
| `ft_lstnew` | Cria novo nó | Criação |
| `ft_lstadd_front` | Adiciona nó no início | Manipulação |
| `ft_lstadd_back` | Adiciona nó no final | Manipulação |
| `ft_lstsize` | Conta nós da lista | Informação |
| `ft_lstlast` | Retorna último nó | Busca |
| `ft_lstdelone` | Deleta um nó | Destruição |
| `ft_lstclear` | Deleta lista inteira | Destruição |
| `ft_lstiter` | Itera sobre lista | Iteração |
| `ft_lstmap` | Cria nova lista aplicando função | Transformação |

## 🧩 Funções Adicionais

Em projetos futuros, essas funcionalidades foram integradas:

### 🖨️ [ft_printf](https://github.com/keilacortes/ft_printf)
Implementação completa da função `printf` com suporte aos principais especificadores:
- `%c` - Caracteres
- `%s` - Strings
- `%p` - Ponteiros
- `%d` / `%i` - Decimais e Inteiros
- `%u` - Inteiros sem sinal
- `%x` / `%X` - Hexadecimal
- `%%` - Percentual literal

### 📖 [get_next_line](https://github.com/keilacortes/get_next_line)
Função que lê uma linha completa de qualquer file descriptor, ideal para:
- Processamento de arquivos linha por linha
- Leitura de entrada padrão
- Parsing de dados estruturados

## 🚀 Como Usar
Baixe este repositório e compile a `libft.a`, depois inclua o cabeçalho `libft.h` ao seu código fonte

```bash

$> git clone https://github.com/keilacortes/libft.git
$> cd libft
$> make
$> make bonus
```

### Exemplo (`test_libft.c`)
```c
#include "libft.h"

int main()
{
    char *original = "  42 São Paulo  ";
    char *limpo = ft_strtrim(original, " ");
    
    ft_printf("Original: '%s'\n", original);
    ft_printf("Limpo:    '%s'\n", limpo);
    
    free(limpo);
    return (0);
}
```

### Compile:
```bash
$> gcc test_libft.c -o test_libft -I inc libft.a
```
  
## 🏗️ Estrutura do Projeto
```
.
├── inc/                    # Headers
│   ├── libft.h             # Header principal
│   ├── ft_printf.h         # Header do ft_printf
│   └── get_next_line.h     # Header do GNL
├── src/                    # Código fonte
│   ├── *.c                 # Funções obrigatórias
│   ├── *_bonus.c           # Funções bônus
│   ├── ft_printf/          # Implementação ft_printf
│   └── get_next_line/      # Implementação GNL
├── libft.a                 # Biblioteca gerada
└── Makefile                # Sistema de build
```

## ⚙️ Comandos Disponíveis

| Comando | Descrição |
|---------|-----------|
| `make` | Compila a biblioteca padrão |
| `make bonus` | Compila incluindo listas encadeadas |
| `make clean` | Remove arquivos objeto (.o) |
| `make fclean` | Remove objetos e a biblioteca (.a) |
| `make re` | Recompila tudo do zero |

## 💬 Vamos Conversar?

Tem sugestões, encontrou um bug ou quer trocar uma ideia sobre programação? Chama aí!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/keilacortes)
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/users/1063035765224914974)

---

>*All 42 Badges — the astronomer Human Coder — were done by Larissa Cristina [@mewmewdevart](https://github.com/mewmewdevart)*
