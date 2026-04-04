# 3D Blocks Editor

Um editor interativo de blocos em pseudo-3D para criar diagramas de arquitetura de forma visual e intuitiva.

## Sobre

O 3D Blocks Editor é uma aplicação single-page que permite criar, conectar e organizar blocos que representam componentes de arquitetura de software (como APIs, bancos de dados, caches, etc.) em uma perspectiva 3D simplificada.

Recursos principais:

- **Interface visual drag-and-drop**: Arraste blocos pela canvas para posicioná-los
- **Conexões entre blocos**: Conecte blocos com linhas para representar relacionamentos
- **Edição inline**: Clique duas vezes em um bloco para editar seu rótulo
- **Camadas (Z-axis)**: Use o scroll do mouse para ajustar a profundidade (zoom in/out)
- **Notas por bloco**: Cada bloco pode ter uma descrição rica acessível via botão ⓘ
- **Persistência automática**: Estado salvo automaticamente no localStorage
- **Controles de teclado**: Setas para mover, +/- para ajustar Z, Delete para remover

## Como usar

1. **Adicionar bloco**: Clique no botão "+ Bloco" e clique na canvas
2. **Mover bloco**: Arraste o bloco pela canvas
3. **Conectar blocos**:
   - Clique em um bloco (fica destacado)
   - Clique em outro bloco para criar a conexão
   - Clique novamente no mesmo bloco para cancelar
4. **Editar nome**: Duplo clique no bloco
5. **Ajustar profundidade**: Scroll do mouse sobre o bloco
6. **Adicionar descrição**: Clique no ícone ⓘ no bloco
7. **Deletar bloco**: Clique no botão "Deletar" e depois no bloco

## Atalhos de teclado

- `← ↑ → ↓`: Mover bloco selecionado
- `+` / `=`: Zoom in (aproximar)
- `-`: Zoom out (afastar)
- `Delete` / `Backspace`: Remover bloco selecionado
- `Escape`: Cancelar conexão pendente

## Estrutura do projeto

```
3d-blocks-editor/
└── docs/
    └── index.html  # Aplicação completa (HTML + CSS + JS)
```

A aplicação é um único arquivo HTML sem dependências externas - basta abrir no navegador.

## Tecnologias

- HTML5 Canvas
- CSS3 (Flexbox, positioning)
- JavaScript ES6+ (vanilla, sem frameworks)

## Características da renderização

- Projeção em pseudo-3D com perspectiva fixa
- Ordenação por profundidade (Z-axis) para renderização correta
- Blocos com faces frontal, laterais e traseiras
- Indicador visual de conexões (linhas tracejadas)
- Escala dos blocos varia com a profundidade

## Limitantes

- Máximo de 10 blocos por diagrama
- Nome do bloco: máximo 20 caracteres
- Descrição: máximo 300 caracteres

---

Desenvolvido com Claude Code