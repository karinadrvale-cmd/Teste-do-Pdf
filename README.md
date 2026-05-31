# Episódio Emocional

> Uma ferramenta interativa de autoconhecimento para mapear, compreender e ressignificar episódios emocionais.

**Criado por [Karina Drvale](https://github.com/karinadrvale-cmd)**

---

## O que é

O **Episódio Emocional** é um guia reflexivo em formato de jornada — um formulário em 6 etapas que conduz a pessoa pelo processo de análise de uma situação emocional vivida. Ao final, gera automaticamente um **mapa visual** das conexões entre o gatilho, o padrão emocional e o comportamento.

A ferramenta é inteiramente **client-side**: roda no navegador, sem servidor, sem banco de dados, sem login. Tudo fica local.

---

## Como usar

1. Abra o arquivo `index.html` no navegador — ou acesse via GitHub Pages
2. Clique em **"Começar minha jornada"**
3. Preencha as 6 etapas com calma e honestidade
4. Clique em **"Concluir jornada"** para ver o resumo completo e o mapa
5. Use os botões de download para salvar o mapa

---

## As 6 etapas

| Etapa | Nome | O que é registrado |
|-------|------|--------------------|
| 1 | **Situação** | Condição anterior, Evento objetivo e Gatilho interno |
| 2 | **Padrão Automático** | Base de dados emocional-comportamental |
| 3 | **Emoções & Reações** | Emoção primária, nuances, intensidade, mudanças físicas e psicológicas |
| 4 | **Ações** | Como você reagiu e se foi construtiva ou destrutiva |
| 5 | **Reestruturação** | Nova perspectiva + condição posterior |
| 6 | **Insight** | O que você leva dessa experiência |

---

## Sobre o Gatilho

> **Evento** → o fato externo, objetivo, observável.
> **Gatilho** → o que aquele evento *tocou* internamente: o significado imediato, o medo ativado, a memória despertada ou a crença confirmada.

O mesmo evento pode não disparar nada em outra pessoa. O gatilho é pessoal — ele existe na interseção entre o evento e a sua história emocional.

---

## Funcionalidades

- Jornada guiada em 6 etapas com transições e barra de progresso
- Chips de emoção primária com ramificações de nuances
- Slider de intensidade emocional (0–10)
- Padrões automáticos selecionáveis + campo livre
- **Mapa mental SVG** gerado dinamicamente com 5 colunas de análise
- Nós do mapa clicáveis com popup de texto completo
- Cards de resumo com modal expansível
- **Download do mapa como PNG** (3× resolução, ~crisp em qualquer tamanho)
- **Imprimir / Salvar como PDF** via diálogo do navegador
- Totalmente responsivo (mobile e desktop)
- Zero dependências externas — apenas Google Fonts

---

## Download do mapa

Ao final da jornada, dois botões aparecem abaixo do mapa:

### 🖼 Baixar mapa (PNG)
Gera uma imagem PNG em **3× de resolução** (triplicando a resolução do SVG original).
Perfeito para salvar no computador, compartilhar ou guardar como arquivo.

- Clique no botão → aguarde a geração (indicador de carregamento)
- O arquivo `mapa-episodio-emocional.png` será baixado automaticamente
- Inclui rodapé discreto com assinatura do projeto

> **Nota sobre fontes:** A conversão SVG→Canvas pode renderizar as fontes com equivalentes do sistema (serif / sans-serif) em vez das fontes Google Fonts originais. A estrutura visual e todos os dados permanecem intactos.

### 🖨 Imprimir / Salvar PDF
Abre o diálogo de impressão do navegador, com layout configurado para:
- Mostrar **apenas o mapa** (oculta formulário, cards e cabeçalhos)
- Orientação **paisagem**
- Margens mínimas

Para salvar como PDF: no diálogo de impressão, selecione **"Salvar como PDF"** (disponível em Chrome, Safari, Edge e Firefox) como impressora.

---

## Estrutura do projeto

```
episodio-emocional/
├── index.html      ← aplicação completa (HTML + CSS + JS em um único arquivo)
└── README.md
```

Toda a lógica está em `index.html`. Sem dependências de build, npm ou frameworks.

---

## Tecnologias

- **HTML5** semântico
- **CSS3** — variáveis, animações, backdrop-filter, line-clamp, `@media print`
- **JavaScript** vanilla — sem frameworks
- **SVG** gerado dinamicamente via JS
- **Canvas API** para exportação PNG
- **Google Fonts** — Fraunces + DM Sans

---

## Deploy via GitHub Pages

1. Vá em **Settings → Pages** no repositório
2. Em *Source*, selecione `main` e `/ (root)`
3. Salve — disponível em:

```
https://<seu-usuario>.github.io/<nome-do-repositorio>/
```

---

## Changelog

### v3.0
- Adicionado campo **Gatilho** separado do Evento na Etapa 1
- Nó Gatilho no mapa agora exibe o gatilho interno real (não o evento)
- Blocos expansíveis: todos os nós do mapa são clicáveis com popup de texto completo
- Cards de resumo com prévia truncada e modal de leitura completa

### v2.0
- Modal expansível nos cards de resumo
- `clipPath` SVG em todos os nós (texto nunca ultrapassa a borda)
- Mapa responsivo sem scroll horizontal

### v1.0
- Lançamento inicial com jornada de 6 etapas e mapa SVG dinâmico

---

*Criado com cuidado por Karina Drvale · 2025*
