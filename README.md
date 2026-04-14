# Floatmind

Editor interativo de blocos em perspectiva 3D para organizar ideias, tarefas e metas — inspirado no "Second Brain".

## Como usar

- **Adicionar bloco:** Clique no botão "Novo bloco" e clique no canvas para posicionar
- **Conectar blocos:** Clique num bloco (fica selecionado), depois clique noutro para conectar
- **Editar nome:** Duplo clique no bloco
- **Mover:** Arraste os blocos ou arraste o fundo para mover todo o gráfico
- **Profundidade (Z):** Use a roda do mouse sobre um bloco selecionado
- **Mover com teclado:** Setas direcionais (← ↑ → ↓)
- **Ajustar Z:** Teclas `+` e `-`
- **Desfazer conexão/remoção:** `Esc`
- **Remover bloco:** Tecla `Delete` ou `Backspace`
- **Realinhar blocos:** Clique no botão "Realinhar" na toolbar para centralizar todos os blocos na tela

**Nota:** O número máximo de blocos é 15.

## Importar / Exportar

- **Exportar:** Clique em "Exportar" no painel lateral para gerar um JSON com todos os blocos e conexões. Copie o texto ou descarregue o ficheiro.
- **Importar:** Clique em "Importar" e cole um JSON válido ou abra um ficheiro previamente exportado. O estado atual será substituído.

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
