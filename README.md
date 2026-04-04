# 3D Blocks Editor

Um editor visual de lembretes em pseudo-3D onde você pode organizar suas ideias e notas em um espaço tridimensional.

## Sobre

O 3D Blocks Editor é uma aplicação single-page que permite criar e organizar blocos de texto em um ambiente 3D interativo. Cada bloco representa um lembrete, nota ou ideia que pode ser posicionado livremente no espaço, criando uma visualização panorâmica de todas as suas anotações.

Recursos principais:

- **Visualização 3D total**: Navegue pelos seus lembretes em um espaço com profundidade
- **Posicionamento livre**: Arraste blocos pela canvas e ajuste sua profundidade com o scroll
- **Edição inline**: Duplo clique para editar o texto de qualquer bloco
- **Descrições detalhadas**: Cada bloco tem uma área de descrição expandida
- **Conexões visuais**: Conecte blocos relacionados com linhas para criar relacionamentos
- **Persistência automática**: Seu trabalho é salvo automaticamente no navegador
- **Interface minimalista**: Foco total no conteúdo, sem distrações

## Como usar

1. **Adicionar lembrete**: Clique no botão "+ Bloco" e clique na canvas
2. **Mover lembrete**: Arraste o bloco pela canvas
3. **Conectar lembretes**:
   - Clique em um bloco (fica destacado)
   - Clique em outro bloco para criar a conexão
   - Clique novamente no mesmo bloco para cancelar
4. **Editar texto**: Duplo clique no bloco para editar o título
5. **Ajustar profundidade**: Use o scroll do mouse sobre o bloco para afastar ou aproximar
6. **Adicionar descrição**: Clique no ícone ⓘ no bloco para abrir o painel de notas
7. **Deletar lembrete**: Clique no botão "Deletar" e depois no bloco

## Atalhos de teclado

- `← ↑ → ↓`: Mover bloco selecionado
- `+` / `=`: Aproximar (zoom in)
- `-`: Afastar (zoom out)
- `Delete` / `Backspace`: Remover bloco selecionado
- `Escape`: Cancelar conexão pendente

## Conceito

Ao invés de listas planas ou arquivos de texto, o 3D Blocks Editor permite que você **veja todas as suas ideias em um único espaço**. Ao posicionar lembretes em diferentes profundidades (Z), você pode:

- Organizar por prioridade (mais perto = mais importante)
- Agrupar por temas (posicionar próximos visualmente)
- Criar fluxos de trabalho (conectando blocos relacionados)
- Manter uma visão geral de todos os seus lembretes simultaneamente

A renderização 3D proporciona uma sensação de amplitude, permitindo que você "viaje" pelo seu espaço de notas e descubra conexões que seriam perdidas em uma lista linear.

## Estrutura do projeto

```
3d-blocks-editor/
└── docs/
    └── index.html  # Aplicação completa (HTML + CSS + JS)
```

A aplicação é um único arquivo HTML sem dependências externas - basta abrir no navegador.

## Tecnologias

- HTML5 Canvas para renderização
- CSS3 (Flexbox, positioning absoluto)
- JavaScript ES6+ (vanilla, sem frameworks)

## Características técnicas

- Projeção em pseudo-3D com perspectiva fixa (f=600px)
- Ordenação automática por profundidade para correto occlusion
- Blocos com faces frontal, laterais e traseiras renderizadas
- Indicadores visuais: conexões tracejadas, glow em selecionados
- Escala dos blocos varia com a profundidade (quanto mais perto, maior)

## Limitantes

- Máximo de 10 blocos por cenário (design decision para manter performance e simplicidade)
- Título do bloco: máximo 20 caracteres
- Descrição: máximo 300 caracteres
- As coordenadas X/Y são limitadas ao tamanho da canvas
- Profundidade (Z) entre 0 e 360 unidades

---

Desenvolvido como ferramenta de organização visual pessoal.