# AppMonitor Pipeline

[![CI Pipeline](https://img.shields.io/github/actions/workflow/status/maitebelo/appmonitor-pipeline/ci.yml?branch=main)](https://github.com/maitebelo/appmonitor-pipeline/actions)

## Sobre o Git na Entrega Contínua

O Git é fundamental na entrega contínua pois:

- Permite controle de versão do código
- Facilita o trabalho em equipe através de branches
- Tags marcam versões estáveis do software
- Integração com ferramentas de CI/CD

## Pipeline de CI

O pipeline é executado automaticamente em push na branch main ou pull requests para main
1. **Validate**: Verifica a sintaxe do script
2. **Test**: Executa testes automatizados
3. **Package**: Gera e publica artefatos

### Logs e Depuração

- **Job Summary**: Resumo detalhado de cada job com:
  - Sistema operacional do runner
  - Branch atual
  - Status da execução
  - Links para artefatos gerados

- **Logs de Debug**: Ativados via `ACTIONS_STEP_DEBUG=true` para:
  - Detalhamento de cada step
  - Informações do ambiente
  - Rastreamento de variáveis

- **Mensagens Personalizadas**:
  - `::warning::` para alertas não críticos
  - `::error::` para falhas que interrompem o pipeline

## Variáveis no GitHub Actions

No GitHub Actions, existem três tipos principais de variáveis:

- **Variáveis de Ambiente (env)**: 
  - Acessíveis durante a execução do workflow
  - Podem ser definidas no nível do workflow ou job
  - Exemplo: `APP_ENV=dev`

- **Variáveis do Repositório (vars)**:
  - Configuradas nas configurações do repositório
  - Acessíveis em todos os workflows
  - Exemplo: `SUPPORT_EMAIL`

- **Segredos (secrets)**:
  - Armazenados de forma criptografada
  - Ideais para informações sensíveis
  - Exemplo: `API_KEY`

## Estrutura do Repositório

- `status-check.sh`: Script para verificação de status da aplicação
- `.github/workflows/ci.yml`: Configuração do pipeline de CI

## Instalação

```bash
git clone https://github.com/maitebelo/appmonitor-pipeline.git
```