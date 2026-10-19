# 🧠 Segundo Cérebro Multi-IA (Multi-Agent Knowledge OS)

> Um guia prático, arquitetura de engenharia e template local-first para construir um **Segundo Cérebro com Múltiplos Agentes de IA** (Claude Code, Antigravity, Gemini CLI, Cursor) no Obsidian.

---

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Obsidian](https://img.shields.io/badge/Obsidian-Local--First-purple.svg)
![AI: Multi-Agent](https://img.shields.io/badge/AI-Multi--Agent%20Ready-success.svg)
![Standard: AGENTS.md](https://img.shields.io/badge/Standard-AGENTS.md-orange.svg)

---

## 🌟 O que é e por que este guia existe?

A maioria dos tutoriais de *"Segundo Cérebro com IA"* encontrados na internet ensina uma receita muito básica: instalar o Obsidian, plugar um assistente e usá-lo para resumir páginas ou bater papo sobre notas soltas.

Quando o volume de notas cresce ou quando você tenta aplicar isso a **projetos complexos, estudos profundos ou decisões profissionais**, esse modelo simples desmorona:
1. **A IA perde o contexto ou alucina:** Sem delimitação de escopo, a IA lê o cofre inteiro, mistura assuntos e queima limites de contexto desnecessariamente.
2. **Cofres viram lixões de anotações:** Ideias brutas e rascunhos disputam espaço com decisões estruturais e metas.
3. **Ficam reféns de uma única ferramenta (Vendor Lock-in):** Se você configura tudo para um único assistente (ex: só Claude ou só OpenAI), perde a liberdade de usar os modelos mais rápidos e inteligentes conforme o mercado evolui.

Este projeto propõe uma **arquitetura de nível sênior de produto e engenharia** para transformar o seu Obsidian em um **Sistema Operacional de Conhecimento e Execução**.

---

## 🏛️ Os 4 Pilares da Arquitetura

```
┌────────────────────────────────────────────────────────────────────────┐
│                        CAMADA 1: ESTRATÉGIA                            │
│  - AGENTS.md / CLAUDE.md (Diretrizes Universais & Contrato da IA)      │
│  - 01 - Contexto/PERFIL.md (Identidade, Valores, Forças & Gargalos)    │
│  - 01 - Contexto/Objetivos e Progresso.md (Bússola de Metas)           │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │
        ┌───────────────────────────┴───────────────────────────┐
        ▼                                                       ▼
┌──────────────────────────────────────┐  ┌──────────────────────────────────────┐
│     CAMADA 2: EXECUÇÃO (Projeto A)   │  │     CAMADA 2: EXECUÇÃO (Projeto B)   │
│  - Pasta Dedicada do Projeto         │  │  - Pasta Dedicada do Projeto         │
│  - AGENTS.md Local (Escopo Estrito)  │  │  - AGENTS.md Local (Escopo Estrito)  │
│  - Visão Geral & DoD                 │  │  - Visão Geral & DoD                 │
│  - Checklist & Diário de Bordo       │  │  - Checklist & Diário de Bordo       │
└──────────────────────────────────────┘  └──────────────────────────────────────┘
```

### 1. Padrão Multi-IA com `AGENTS.md`
Em vez de ficar amarrado a um formato proprietário, usamos o **`AGENTS.md`** como a fonte única da verdade para todas as IAs:
* **Antigravity / Gemini CLI:** Lêem `AGENTS.md` nativamente.
* **Claude Code & Claudian:** Lêem `CLAUDE.md`, que aponta diretamente para o `@AGENTS.md`.
* **Cursor / Windsurf / Copilot:** Compartilham as mesmas diretrizes contextuais.

### 2. Arquitetura de Duas Camadas
* **Camada 1 (Estratégia & Vida — Raiz do Cofre):** Onde a IA atua como **parceira de pensamento e mentora**. Ela te ajuda a priorizar, desafia suas suposições e conecta pontos entre trabalho, estudos e rotina.
* **Camada 2 (Execução Focada — Pastas de Projetos):** Cada projeto possui seu próprio arquivo de contexto local. A IA só trabalha no escopo daquele projeto, com critérios de conclusão claros (*Definition of Done*), sem gastar tokens com o resto do cofre.

### 3. O Desacoplamento da Workbench (`99 - Workbench/`)
A maior falha dos segundos cérebros é exigir organização imediata de quem está no meio de um turbilhão de ideias:
* **Workbench (Bancada do Usuário):** Zona livre de regras. Você joga pensamentos soltos, braindumps e anotações de reunião sem precisar formatar.
* **Pastas Curadas (A Verdade Oficial):** Só entram notas revisadas, estruturadas e com links consistentes. A IA atua na "promoção" do que amadureceu na Workbench para as pastas oficiais.

### 4. Disciplina de Engenharia & Governança
Inspirado nas diretrizes de **Andrej Karpathy** e nas melhores práticas de engenharia de software:
* **Pense antes de codar/escrever:** Declare suposições e investigue a causa raiz.
* **Simplicidade primeiro:** O mínimo necessário que resolve o problema, sem superengenharia.
* **Mudanças cirúrgicas:** A IA altera apenas o estritamente necessário e limpa sua própria sujeira.
* **Critérios de sucesso claros:** Toda tarefa tem um critério verificável de sucesso.

---

## 📁 Estrutura de Pastas do Template

```text
meu-segundo-cerebro/
├── .agents/skills/            # Habilidades automatizadas (executáveis pela IA)
│   ├── configurar-cerebro/    # Entrevista de calibração de perfil e metas
│   └── novo-projeto/          # Scaffold automático de novas frentes
├── .claude/skills/            # Espelho de compatibilidade para Claude Code
├── 00 - Entrada/              # Captura rápida e notas temporárias da Inbox
├── 01 - Contexto/             # Quem você é, pontos fortes e metas (Camada 1)
├── 02 - Áreas/                # Áreas contínuas de responsabilidade e vida
├── 03 - Projetos/             # Frentes com início, meio e fim (Camada 2)
│   └── _Modelo de Projeto/    # Template base com Visão Geral e AGENTS.md local
├── 04 - Decisões/             # Registros Formais de Decisão (ADRs)
├── 99 - Workbench/            # Bancada de trabalho bruto e notas rápidas
├── AGENTS.md                  # Manual universal de comportamento das IAs
├── CLAUDE.md                  # Ponte de compatibilidade para ferramentas Claude
└── README.md                  # Mapa central do cofre (00 - Início)
```

---

## ⚡ Guia Rápido: Como Começar do Zero

### Passo 1: Baixar e Abrir no Obsidian
1. Clone ou baixe este repositório.
2. Copie a pasta `template-vault/` para o seu computador.
3. No [Obsidian](https://obsidian.md/), clique em **"Abrir pasta como cofre"** e selecione a pasta.

### Passo 2: Calibrar a IA com a sua Identidade
Abra seu terminal ou assistente de IA no cofre e digite:
```bash
/configurar-cerebro
```
A IA fará 4 perguntas conversacionais para entender:
1. Seu momento atual e principais prioridades.
2. Suas metas para os próximos 6 a 12 meses.
3. Seus maiores pontos fortes e onde costuma se sabotar.
4. Como você quer ser desafiado e respondido (estilo de feedback).

Ao final, ela sintetiza e grava automaticamente seus arquivos de contexto (`PERFIL.md` e `Objetivos e Progresso.md`).

### Passo 3: Iniciar seu Primeiro Projeto Automatizado
Para criar uma nova frente de trabalho com escopo delimitado:
```bash
/novo-projeto
```
A IA solicitará o nome, a área e o critério de conclusão, gerando a pasta com a nota de **Visão Geral** e o **`AGENTS.md` local de Camada 2** em segundos.

---

## 🗺️ Roadmap de Evolução

- [x] Repositório estruturado com licença aberta e sanitizado.
- [x] Padrão `AGENTS.md` universal documentado.
- [x] Skills automatizadas (`/configurar-cerebro` e `/novo-projeto`).
- [ ] Guia interativo em formato de página Web moderna (UI com Astro Starlight / VitePress).
- [ ] Catálogo de skills extras (TDD, Systematic Debugging, ADR Generators).
- [ ] Exemplos de integração com MCPs locais.

---

## 📄 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.
