# Exemplos de código Magik para Smallworld

[![Gerado pelo GitHub Copilot](https://img.shields.io/badge/Gerado%20por-GitHub%20Copilot-blue)](https://github.com/features/copilot)

Este repositório demonstra como o **GitHub Copilot** pode desenvolver exemplos abrangentes de código Magik para Smallworld. Magik é uma linguagem de programação orientada a objetos usada no GE Smallworld GIS (Sistema de Informação Geográfica).

## 📚 Sumário

- [Sobre Magik](#sobre-magik)
- [Arquivos de demonstração](#arquivos-de-demonstração)
- [Primeiros passos](#primeiros-passos)
- [Recursos demonstrados](#recursos-demonstrados)
- [Exemplos de uso](#exemplos-de-uso)
- [Estrutura de arquivos](#estrutura-de-arquivos)

## Sobre Magik

**Magik** é a linguagem de programação usada na plataforma Smallworld GIS. Suas principais características incluem:

- Orientação a objetos com herança baseada em protótipos
- Tipagem dinâmica
- Gerenciamento de memória com coleta de lixo
- Estilo de programação baseado em métodos
- Suporte integrado a operações de GIS

## Arquivos de demonstração

| Arquivo | Descrição |
|------|-------------|
| `01_hello_world.magik` | Exemplo básico de Hello World e métodos de saída |
| `02_variables_and_types.magik` | Variáveis, tipos de dados e operações aritméticas |
| `03_control_flow.magik` | Condicionais, laços e blocos |
| `04_procedures.magik` | Funções, expressões lambda e recursão |
| `05_classes_and_oop.magik` | Padrões de programação orientada a objetos |
| `06_collections.magik` | Vetores, tabelas hash, conjuntos e outros |
| `07_exception_handling.magik` | Tratamento de erros e blocos de proteção |
| `08_practical_examples.magik` | Geometria, utilitários de texto e matemática |
| `09_main_demo.magik` | Ponto de entrada principal para executar as demonstrações |

## Primeiros passos

Para executar as demonstrações em um ambiente Smallworld Magik:

```magik
# Carregue todos os arquivos de demonstração
# Em seguida, execute a demonstração completa:
object.run_all_demos()

# Ou execute uma demonstração rápida:
object.quick_demo()

# Ou consulte a ajuda:
object.magik_help()
```

## Recursos demonstrados

### 1. Sintaxe básica
- Saída de Hello World
- Comentários e documentação
- Declaração de pacote

### 2. Variáveis e tipos de dados
```magik
_local my_integer << 42
_local my_float << 3.14159
_local my_string << "Olá, Magik"
_local my_symbol << :my_symbol
_local my_boolean << _true
```

### 3. Controle de fluxo
```magik
# Condicionais
_if score >= 60
_then
    write("Aprovado!")
_else
    write("Reprovado")
_endif

# Laços
_over i _over range(1, 10)
_loop
    write(i)
_endloop
```

### 4. Procedimentos (métodos)
```magik
_method object.add_numbers(a, b)
    ## Soma dois números.
    _return a + b
_endmethod
```

### 5. Programação orientada a objetos
```magik
# Define uma classe (exemplar)
def_slotted_exemplar(:demo_point,
    {
        {:x, 0},
        {:y, 0}
    },
    {:object})

# Construtor
_method demo_point.new(x, y)
    _local new_point << _clone
    new_point.x << x
    new_point.y << y
    _return new_point
_endmethod
```

### 6. Coleções
```magik
# Vetor simples
_local numbers << {1, 2, 3, 4, 5}

# Tabela hash
_local person << hash_table.new()
person[:name] << "João"
person[:age] << 30

# Rope (vetor dinâmico)
_local my_rope << rope.new()
my_rope.add("elemento")
```

### 7. Tratamento de exceções
```magik
_protect
    # Código protegido
    write("Executando...")
_protection
    # Sempre executa (como finally)
    write("Limpeza")
_endprotect
```

### 8. Operações de GIS e geometria
```magik
# Cálculo de distância
_local distance << geometry_utils.distance(x1, y1, x2, y2)

# Área de um polígono
_local area << geometry_utils.polygon_area(vertices)

# Verifica se um ponto está dentro de um polígono
_local inside << geometry_utils.point_in_polygon?(x, y, polygon)
```

## Exemplos de uso

### Executar todas as demonstrações
```magik
object.run_all_demos()
```

### Demonstrações individuais
```magik
# Demonstração de Hello World
object.demo_output()

# Variáveis e tipos
object.demo_variables()
object.demo_data_types()

# Controle de fluxo
object.demo_conditionals()
object.demo_loops()

# Procedimentos
object.demo_procedures()
object.demo_iterators()

# Programação orientada a objetos
object.demo_oop()

# Coleções
object.demo_collections()

# Tratamento de exceções
object.demo_exceptions()

# Exemplos práticos
object.demo_geometry()
object.demo_string_utils()
object.demo_validation()
object.demo_math()
```

### Demonstração específica de GIS
```magik
object.gis_concepts_demo()
```

## Estrutura de arquivos

```
test-assisted-magik/
├── README.md                         # Esta documentação
└── examples/
    ├── 01_hello_world.magik          # Saída básica
    ├── 02_variables_and_types.magik  # Tipos de dados
    ├── 03_control_flow.magik         # Condicionais e laços
    ├── 04_procedures.magik           # Funções e expressões lambda
    ├── 05_classes_and_oop.magik      # Padrões de POO
    ├── 06_collections.magik          # Coleções
    ├── 07_exception_handling.magik   # Tratamento de erros
    ├── 08_practical_examples.magik   # Utilitários
    └── 09_main_demo.magik            # Ponto de entrada principal
```

## Demonstração das capacidades do Copilot

Este repositório foi gerado pelo **GitHub Copilot**, demonstrando sua capacidade de:

✅ Compreender a sintaxe e a semântica da linguagem Magik  
✅ Gerar código Magik devidamente formatado  
✅ Criar exemplos abrangentes que cobrem os principais recursos da linguagem  
✅ Escrever comentários de documentação adequados  
✅ Implementar padrões de orientação a objetos  
✅ Criar funções utilitárias práticas  
✅ Trabalhar com conceitos específicos de GIS  
✅ Seguir as convenções de código Magik  

## Licença

Este código de demonstração é fornecido "no estado em que se encontra" para fins educacionais.

---

*Gerado pelo assistente de IA do GitHub Copilot*