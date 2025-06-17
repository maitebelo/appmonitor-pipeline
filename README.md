# AppMonitor Pipeline

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

## Estrutura do Repositório

- `status-check.sh`: Script para verificação de status da aplicação
- `.github/workflows/ci.yml`: Configuração do pipeline de CI

## Instalação

```bash
git clone https://github.com/maitebelo/appmonitor-pipeline.git
``` 