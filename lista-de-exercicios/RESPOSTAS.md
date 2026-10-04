# Lista de Exercícios — 22 Questões Dissertativas

**Aluno:** Júlio Florencio
**Disciplina:** Programação Orientada a Objetos
**Linguagem de referência:** Python

---

## Parte I — Fundamentos de POO

### 1. Classe e objeto

A classe é um modelo que define atributos e comportamentos. O objeto é uma
instância concreta criada a partir dessa classe.

### 2. Encapsulamento

É a proteção dos dados internos de um objeto, controlando como eles são
acessados ou alterados. Em Python, usa-se a convenção `_atributo` para indicar
uso interno e `__atributo` para aplicar *name mangling*, dificultando o acesso
direto.

### 3. Herança

Uma subclasse herda atributos e métodos de uma superclasse. Ela pode adicionar
novos métodos, sobrescrever métodos existentes ou utilizar `super()` para
aproveitar o comportamento da classe base.

### 4. Polimorfismo

Permite usar objetos de subclasses diferentes como se fossem objetos da
superclasse. Cada subclasse pode implementar o mesmo método de uma maneira
diferente.

### 5. Função do `self`

O `self` representa a instância atual do objeto. Ele permite acessar os
atributos e métodos específicos daquele objeto.

### 6. Tipos de métodos

| Tipo | Decorador | Primeiro parâmetro | Finalidade |
|---|---|---|---|
| Método de instância | — | `self` | Trabalha com dados do objeto |
| Método de classe | `@classmethod` | `cls` | Trabalha com a classe ou seus atributos |
| Método estático | `@staticmethod` | — | Função auxiliar relacionada à classe |

### 7. Atributos de classe

São definidos diretamente na classe e compartilhados entre todas as instâncias.
Os atributos de instância normalmente são definidos com `self` e pertencem
individualmente a cada objeto.

### 8. Métodos *hook* no Template Method

São métodos opcionais ou pontos de extensão que uma subclasse pode sobrescrever.
Eles permitem manter o processamento geral na superclasse e colocar regras
específicas nas subclasses.

---

## Parte II — Clean Code

### 9. Objetivo do Clean Code

Produzir código claro, simples, legível, fácil de testar e fácil de manter por
outros desenvolvedores.

### 10. Visão de Bjarne Stroustrup

Um código limpo deve ser eficiente, claro e direto. Cada rotina deve executar
uma tarefa bem definida, sem acumular responsabilidades desnecessárias.

### 11. Três perguntas que um nome deve responder

Um nome deve informar:

1. Por que esse elemento existe?
2. O que ele faz?
3. Como ele deve ser usado?

### 12. Nomes grandes

Nomes maiores são aceitáveis quando deixam o propósito claro. É melhor um nome
longo e explicativo do que uma abreviação curta e confusa.

### 13. Convenção para classes e métodos

Classes representam conceitos ou entidades e geralmente recebem nomes com
substantivos, como `Cliente`. Métodos representam ações e normalmente usam
verbos, como `calcular_total()`.

### 14. Métodos com muitos níveis de aninhamento

Um método com muitas estruturas internas provavelmente faz várias coisas.
Dividi-lo em métodos menores, cada um com uma única tarefa, melhora a leitura e
reduz responsabilidades.

### 15. *Code Smell*

É um sinal de que o código pode ter problemas de estrutura ou manutenção. Código
ruim aumenta erros, retrabalho e dificuldade para incluir novas funcionalidades,
prejudicando o projeto e a evolução profissional do desenvolvedor.

### 16. Princípio DRY

Significa *"Don't Repeat Yourself"* — não se repita. A ideia é evitar copiar e
colar a mesma lógica em várias partes do sistema, colocando o comportamento
comum em um único local reutilizável.

### 17. Uso excessivo de comentários

Muitos comentários podem indicar que o código não está claro. A alternativa
recomendada é utilizar nomes significativos, métodos pequenos e uma estrutura
que explique por si mesma o que está sendo feito.

### 18. Regras FIRST para testes

| Regra | Significado |
|---|---|
| **F**ast | Rápidos |
| **I**ndependent | Independentes |
| **R**epeatable | Repetíveis |
| **S**elf-validating | Capazes de indicar automaticamente se passaram ou falharam |
| **T**imely | Escritos no momento adequado, preferencialmente junto ou antes do código |

---

## Parte III — SOLID e Arquitetura Limpa

### 19. Princípio da Responsabilidade Única (SRP)

Uma classe deve ter apenas um motivo para mudar, ou seja, uma responsabilidade
principal. Quando uma classe possui responsabilidades demais, sua coesão diminui
e sua manutenção fica mais difícil.

### 20. Princípio Aberto/Fechado (OCP)

O código deve permitir a criação de novos comportamentos sem alterar o que já
funciona. A herança e o polimorfismo permitem criar subclasses com novas
implementações, reduzindo mudanças na classe original.

### 21. Princípio de Substituição de Liskov (LSP)

Uma subclasse deve poder substituir sua superclasse sem quebrar o sistema. Se a
classe derivada exige recursos extras, como "baterias" que não estavam
previstas na classe base, isso indica que a abstração ou a relação de herança
foi mal definida.

### 22. Relação entre SOLID e Arquitetura Limpa

O Clean Code melhora variáveis, métodos e classes. O SOLID ajuda a organizar
responsabilidades e dependências. Por exemplo, o SRP separa as responsabilidades
dos módulos, enquanto o DIP faz as regras de negócio dependerem de abstrações, e
não diretamente de banco de dados, frameworks ou serviços externos. Isso
facilita testes, manutenção e substituição de tecnologias.
