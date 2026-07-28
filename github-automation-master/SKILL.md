---
name: github-automation-master
description: >
  Skill completa de automação do GitHub para o Antigravity e Hermes.
  Cobre criação de repositórios, Pull Requests (PRs), stacked PRs, revisão de código por IA,
  gestão de branches, issue tracking, GitHub Actions (CI/CD), releases e automação via gh CLI e REST API.
  Gatilhos: "github", "pull request", "pr", "git clone", "push", "issue", "release", "gh cli", "ci/cd".
---

# SKILL: GitHub Automation & Operations Master

## 📌 Visão Geral
Esta skill transforma a IA em um operador avançado do GitHub utilizando a CLI oficial (`gh`) e a API REST/GraphQL. Ela permite automação completa do ciclo de vida de desenvolvimento de software sem necessidade de intervenção manual no navegador.

---

## 🛠️ Capacidades Principais & Operações Automáticas

### 1. Gestão de Repositórios & Clonagem
- **Criar Repositórios**: `gh repo create <nome> --private --source=. --remote=origin`
- **Clonar / Fork**: `gh repo clone <owner>/<repo>`
- **Sincronização de Remotos**: Manter repositórios locais e remotos 100% atualizados.

### 2. Ciclo de Vida de Pull Requests (PRs)
- **Criar PR**: `gh pr create --title "<titulo>" --body "<descricao_detalhada>"`
- **Revisar PR**: Analisar diffs, apontar code smells e comentar direto nas linhas via `gh pr review`.
- **Merge Automático**: `gh pr merge <pr_number> --squash --delete-branch` após passar nos testes.
- **Stacked PRs**: Organizar grandes alterações em PRs encadeados e menores para facilidade de revisão.

### 3. Gestão de Issues & Kanban
- **Criar & Triar Issues**: `gh issue create --title "<titulo>" --label "bug,prioridade-alta"`
- **Vincular PRs a Issues**: Fechar issues automaticamente usando `Closes #123` no body do PR.

### 4. CI/CD com GitHub Actions
- **Monitorar Builds**: `gh run list` e `gh run watch` para acompanhar workflows de integração contínua.
- **Logs de Erros de Build**: Extrair logs de falha via `gh run view --log-failed` para diagnóstico imediato.

### 5. Releases & Tagging
- **Gerar Releases**: `gh release create v1.0.0 --title "Versão 1.0.0" --notes-file CHANGELOG.md`
- **Anexar Artefatos**: Upload automático de binários ou pacotes gerados no release.

---

## 🎯 Regras de Execução Segura
1. **Nunca commitar credenciais**: Verificar com o `git diff` antes de dar commit se há arquivos `.env` ou secrets.
2. **Mensagens de Commit Semânticas**: Usar o padrão Conventional Commits (`feat:`, `fix:`, `docs:`, `refactor:`).
3. **Branches Limpas**: Sempre criar feature branches (`feature/nome`, `fix/nome`) em vez de commitar direto na `main`/`master`.
