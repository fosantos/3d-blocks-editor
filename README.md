# Floatmind

Editor interativo de blocos em perspectiva 3D para organizar ideias, tarefas e metas — inspirado no "Second Brain".

## Como usar

O layout usa "ilhas" flutuantes estilo Excalidraw: menu/realinhar/undo/redo no topo esquerdo, ferramentas de bloco na lateral esquerda, painel contextual no topo quando um bloco está selecionado, e contador + ajuda no canto inferior esquerdo.

- **Adicionar bloco:** Clique no botão "＋" na ilha lateral e clique no canvas para posicionar
- **Conectar blocos:** Clique num bloco (fica selecionado), depois clique noutro — ou use o dropdown "conectar a…" no painel contextual
- **Editar nome:** Duplo clique no bloco (ou botão ✎ no painel contextual)
- **Mover:** Arraste os blocos ou arraste o fundo para mover todo o gráfico
- **Profundidade (Z):** Use a roda do mouse sobre um bloco selecionado, o slider no painel contextual, ou as teclas `+` e `-`
- **Mover com teclado:** Setas direcionais (← ↑ → ↓)
- **Remover bloco:** Tecla `Delete`/`Backspace` ou o botão no painel contextual
- **Desfazer conexão/remoção:** `Esc` ou Ctrl+Z
- **Realinhar blocos:** Clique no botão de realinhar na ilha superior esquerda para centralizar todos os blocos na tela

**Nota:** O número máximo de blocos é 15.

## Importar / Exportar

- **Exportar:** Abra o menu (☰) na ilha superior esquerda e clique em "Exportar" para gerar um JSON com todos os blocos e conexões. Copie o texto ou descarregue o ficheiro.
- **Importar:** Abra o menu (☰) e clique em "Importar"; cole um JSON válido ou abra um ficheiro previamente exportado. O estado atual será substituído.

O formato exportado inclui:
- Lista de blocos (posição, rótulo, descrição)
- Conexões entre blocos
- Metadados (versão, data de exportação)

## Funcionalidades

- Blocos em perspectiva 3D com profundidade ajustável
- Conexões visuais entre blocos
- Painel de descrição por bloco
- Botão de realinhamento para centralizar todos os blocos
- Layout responsivo que ocupa a tela inteira
- Zero dependências — HTML/CSS/JS puro
- Estado persistente no localStorage

## Arquivo

Tudo está em um único arquivo: `docs/index.html`

Abra diretamente no browser — não precisa de servidor.

## Breve descrição

Este editor foi criado como ferramenta visual para organizar pensamentos (Ideias), compromissos (Tarefas) e objetivos (Metas) de forma espacial e conectada, usando uma metáfora de blocos tridimensionais flutuando num espaço virtual.
