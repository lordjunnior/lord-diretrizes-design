<div align="center">

# Lord Diretrizes de Design

![Padrao](https://img.shields.io/badge/Padrao-Agent%20Skills-black?style=for-the-badge&logo=anthropic)
![Ambiente](https://img.shields.io/badge/Ambiente-Claude%20%7C%20Cursor%20%7C%20Codex-8A2BE2?style=for-the-badge)
![Licenca](https://img.shields.io/badge/Licenca-Apache%202.0-blue?style=for-the-badge&logo=apache)
![Status](https://img.shields.io/badge/Status-Estavel-brightgreen?style=for-the-badge)

**Estrutura avançada de competências modulares, diretrizes visuais e automação para agentes inteligentes.**

Conjunto de diretrizes, scripts e instruções empacotadas para o ecossistema Claude e ferramentas de programação orientadas por IA, com base na especificação aberta Agent Skills.

</div>

---

## Demonstração Visual

<div align="center">
  <img src="assets/demonstracao.gif" alt="Demonstração do Lord Diretrizes de Design" width="850">
</div>

---

## Visão Geral e Arquitetura

As habilidades (*skills*) são diretórios compostos por ficheiros `SKILL.md`, scripts operacionais e recursos auxiliares carregados dinamicamente para orientar agentes em tarefas especializadas. O sistema padroniza a execução em múltiplos contextos, desde a conceção de interfaces técnicas sem vícios genéricos até à manipulação rigorosa de documentos e análise de dados.

### Pilares de Engenharia

* **Execução Repetível:** Eliminação de respostas improvisadas através de instruções e regras contratuais bem definidas.
* **Isolamento de Escopo:** Cada competência reside na sua própria pasta, encapsulando metadados, dependências e parâmetros de validação.
* **Compatibilidade Multiferramenta:** Conformidade total com a especificação formal Agent Skills, suportando Claude Code, Claude.ai, Cursor e clientes MCP.
* **Código Limpo e Documentado:** Diretrizes estritas para evitar excesso de elementos visuais genéricos e manter semântica sustentável.

---

## Módulos e Competências Disponíveis

| Domínio | Caminho | Finalidade Técnica |
| :--- | :--- | :--- |
| `Documentos DOCX` | `skills/docx` | Criação, leitura e edição programática de documentos Word |
| `Documentos PDF` | `skills/pdf` | Extração de tabelas, formulários e processamento visual de ficheiros PDF |
| `Apresentações PPTX`| `skills/pptx` | Estruturação automatizada de diapositivos e diagramas técnicos |
| `Folhas de Cálculo` | `skills/xlsx` | Tratamento, consolidação e geração de tabelas e métricas Excel |
| `Design de Frontend`| `skills/frontend-design` | Diretrizes estéticas, padrões de layout escuro e identidade visual |
| `Exemplos e Testes` | `skills/example-skills` | Modelos práticos de servidores MCP e fluxos de automação técnica |

---

## Integração no Claude Code

Para registar o repositório como catálogo de extensões no terminal do Claude Code:

```bash
/plugin marketplace add anthropics/skills
Para proceder à instalação direta de conjuntos específicos via linha de comandos:

Bash
/plugin install document-skills@anthropic-agent-skills
/plugin install example-skills@anthropic-agent-skills
Após a instalação, as competências são acionadas através de instruções diretas:

Plaintext
Utilize a habilidade de PDF para extrair todos os campos do formulário em ./documento.pdf
Especificação de uma Nova Habilidade
Cada módulo requer apenas uma pasta dedicada e um ficheiro SKILL.md estruturado com cabeçalho YAML e orientações objetivas:

Markdown
---
name: nome-da-habilidade
description: Descrição objetiva da funcionalidade técnica e condições de ativação
---

# Nome da Habilidade

[Instruções detalhadas para execução pelo modelo]

## Diretrizes de Execução
- Regra de validação estrutural 1
- Regra de formatação e semântica 2
Licença e Atribuição
Este projeto é disponibilizado sob os termos da Licença Apache, Versão 2.0.

Projeto Base e Especificações Originais: Anthropic (anthropics/skills)

Curadoria, Tradução Técnica e Padronização: Lord Junnior

Repositório Oficial: lordjunnior/lord-diretrizes-design

Portal de Aplicações: lordjunnior.com.br/ferramentas
