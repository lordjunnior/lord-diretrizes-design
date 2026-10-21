> **Nota:** Este repositório contém a implementação de habilidades da Anthropic para a Claude. Para informações sobre o padrão Agent Skills, consulte [agentskills.io](http://agentskills.io)[cite: 6].

[![skills.sh](https://skills.sh/b/anthropics/skills)](https://skills.sh/anthropics/skills)

# Lord Diretrizes de Design (Skills)

Habilidades (skills) são pastas contendo instruções, scripts e recursos que a Claude carrega dinamicamente para aumentar o desempenho em tarefas especializadas. As habilidades ensinam a Claude a executar tarefas específicas de forma padronizada e repetível, seja criando documentos com as diretrizes visuais da sua organização, analisando dados por meio de fluxos operacionais específicos ou automatizando tarefas cotidianas.

Para mais informações, consulte:
- [O que são habilidades?](https://support.claude.com/en/articles/12512176-what-are-skills)[cite: 6]
- [Como usar habilidades na Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)[cite: 6]
- [Como criar habilidades personalizadas](https://support.claude.com/en/articles/12512198-creating-custom-skills)[cite: 6]
- [Preparando agentes para o mundo real com Agent Skills](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)[cite: 6]

---

# Sobre Este Repositório

Este repositório reúne habilidades que demonstram o potencial prático do ecossistema de habilidades da Claude. Elas abrangem desde aplicações criativas (arte, música, design de interface) até tarefas estritamente técnicas (testes de aplicações web, geração de servidores MCP) e rotinas corporativas (comunicação institucional, diretrizes de marca e redação).

Cada habilidade é autocontida em sua própria pasta e possui um arquivo `SKILL.md` com as instruções e metadados lidos pela Claude. Você pode navegar por essas pastas para buscar referências para suas próprias implementações ou para estudar padrões arquiteturais.

A maioria das habilidades deste repositório é de código aberto sob a licença Apache 2.0[cite: 6]. Também disponibilizamos as habilidades de criação e edição de documentos que operam nos bastidores dos recursos de arquivos da Claude, localizadas nas subpastas [`skills/docx`](./skills/docx), [`skills/pdf`](./skills/pdf), [`skills/pptx`](./skills/pptx) e [`skills/xlsx`](./skills/xlsx)[cite: 6]. Estes módulos possuem código disponível para consulta (source-available), servindo como base técnica para habilidades avançadas operando em ambientes reais de produção.

## Aviso Legal

**Estas habilidades são disponibilizadas exclusivamente para demonstração e finalidades educacionais.** Embora parte dessas capacidades esteja acessível nativamente na Claude, os comportamentos e resultados gerados podem variar em relação aos modelos demonstrados. As habilidades aqui reunidas servem para exemplificar fluxos e possibilidades operacionais. Teste sempre as instruções no seu próprio ambiente de execução antes de adotá-las em fluxos críticos de produção.

---

# Estrutura de Habilidades

- [./skills](./skills): Exemplos práticos divididos em Design e Criação, Engenharia e Desenvolvimento Técnico, Comunicação Corporativa e Manipulação de Documentos.
- [./spec](./spec): Especificação formal da arquitetura Agent Skills.
- [./template](./template): Estrutura base para inicialização de novas habilidades.

---

# Execução no Claude Code, Claude.ai e via API

## Claude Code

Você pode registrar este repositório como um catálogo (marketplace) de extensões no Claude Code executando o comando:

```bash
/plugin marketplace add anthropics/skills
Para instalar um conjunto específico de módulos:   Selecione Browse and install plugins.   Escolha anthropic-agent-skills.   Marque document-skills ou example-skills.   Confirme em Install now.   Se preferir a instalação direta via linha de comando, execute:   Bash/plugin install document-skills@anthropic-agent-skills
/plugin install example-skills@anthropic-agent-skills
Com o plugin ativo, basta acionar a habilidade em linguagem natural. Por exemplo, ao instalar o pacote document-skills, você pode solicitar:   "Use a habilidade de PDF para extrair os campos de formulário do arquivo caminho/do/documento.pdf"   Claude.aiEstes modelos de habilidades já estão integrados nas contas com planos pagos no Claude.ai. Para utilizar habilidades deste repositório ou carregar implementações próprias, siga o guia oficial em Usando habilidades na Claude[cite: 6].   API da ClaudeAs habilidades mantidas pela Anthropic e módulos personalizados também podem ser acionados via API[cite: 6]. Consulte o manual de integração em Skills API Quickstart[cite: 6].Como Criar uma Habilidade BásicaA criação de uma habilidade requer apenas uma pasta contendo um arquivo SKILL.md estruturado com cabeçalho YAML e instruções detalhadas[cite: 6]. Você pode utilizar o modelo template-skill deste repositório como ponto de partida[cite: 6]:Markdown---
name: nome-da-minha-habilidade
description: Uma descricao clara do que a habilidade executa e em quais cenarios deve ser ativada
---

# Nome da Minha Habilidade

[Insira aqui as instrucoes detalhadas que a Claude devera seguir quando esta habilidade estiver em execucao]

## Exemplos
- Exemplo de uso 1
- Exemplo de uso 2

## Diretrizes
- Diretriz operacional 1
- Diretriz operacional 2
O cabeçalho YAML requer obrigatoriamente dois campos[cite: 6]:name: Identificador único da habilidade (escrito em letras minúsculas, usando hífens para separar palavras)[cite: 6].description: Descrição objetiva da funcionalidade e dos gatilhos de acionamento[cite: 6].O corpo do documento em Markdown contém as regras de comportamento, referências e orientações de execução[cite: 6]. Detalhes adicionais estão disponíveis em Como criar habilidades personalizadas[cite: 6].Habilidades Desenvolvidas por ParceirosO ecossistema permite conectar a Claude a ferramentas externas de terceiros[cite: 6]. Casos de integração desenvolvidos por parceiros[cite: 6]:Notion: Habilidades do Notion para Claude[cite: 6]Licença e AtribuiçãoEste projeto é disponibilizado sob os termos da Licença Apache, Versão 2.0[cite: 6].Projeto Base e Conceito Original: Anthropic (anthropics/skills)[cite: 6]Curadoria, Tradução Técnica e Adaptação: Lord JunniorRepositório Oficial: lordjunnior/lord-diretrizes-designPortal de Aplicações: lordjunnior.com.br/ferramentas