# Neo-Tokyo Ops

Site interativo de estudo de DevOps e resposta a incidentes, com tema do filme **Akira** (Neo-Tokyo, cyberpunk).

Página única em HTML/CSS/JS puro, sem build e sem dependências — basta abrir o `index.html` no navegador.

## O que tem

- **6 módulos** — Linux (triagem de incidente), Docker, Docker Compose, Kubernetes, Terraform e AWS CLI
- **~65 comandos essenciais** em cartas clicáveis, cada um executável num terminal simulado com saída realista de produção
- **6 missões de incidente** com ambiente que reage aos comandos:
  1. Disco cheio derrubando a API (`df` → `du` → `truncate`)
  2. CPU em 100% por job esquecido (`top` → `kill`)
  3. Container Docker em crash loop (logs → corrigir `.env` → `compose up`)
  4. Pod em CrashLoopBackOff por OOM (`describe` → `rollout undo`)
  5. Drift no Terraform com BucketAlreadyExists (`plan` → `import`)
  6. Instância EC2 de produção desligada (`sts` → `describe` → `start`)
- **Progressão** — XP por comando novo (+5) e por incidente resolvido (+60), patentes de CIVIL até AKIRA, progresso salvo em `localStorage`

Os terminais são 100% simulados: nada roda de verdade, é seguro errar à vontade.
