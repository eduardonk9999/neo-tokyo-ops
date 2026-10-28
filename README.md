<div align="center">

# ⛩ NEO-TOKYO OPS

**ネオ東京・オプス**

*Dojo interativo de DevOps e resposta a incidentes — tema Akira (1988)*

[![Demo](https://img.shields.io/badge/▶_DEMO_AO_VIVO-ff2438?style=for-the-badge&labelColor=0b0507)](https://eduardonk9999.github.io/neo-tokyo-ops/)
[![HTML](https://img.shields.io/badge/HTML-puro-ff2438?style=flat-square&labelColor=0b0507)](#)
[![CSS](https://img.shields.io/badge/CSS-puro-35c8ff?style=flat-square&labelColor=0b0507)](#)
[![JS](https://img.shields.io/badge/JavaScript-vanilla-ffb13d?style=flat-square&labelColor=0b0507)](#)
[![Deps](https://img.shields.io/badge/dependências-zero-49ff9b?style=flat-square&labelColor=0b0507)](#)

*São 3 da manhã. A produção caiu. O que você digita primeiro?*

</div>

---

## 🏍 O que é

Um site de **página única** pra treinar DevOps do jeito que se aprende de verdade: **digitando comandos e resolvendo incidentes** — sem medo de derrubar nada, porque os terminais são 100% simulados.

A estética é Neo-Tokyo do filme **Akira**: vermelho neon sobre preto, katakana, glitch, scanlines e faixa de perigo. O poder do root é como o de Akira — use com responsabilidade.

```
root@neo-tokyo:~# df -h
/dev/vda2    50G   50G     0 100% /var    ← seu problema começa aqui
```

## 📟 Módulos

Cada módulo tem cartas de comandos essenciais. Clicou (ou digitou), o comando roda num **terminal sandbox** com saída realista de produção — `help` lista o catálogo, `↑` repete, `clear` limpa.

| # | Módulo | Foco |
|---|--------|------|
| 01 核 | **Linux** | Triagem de incidente: CPU, memória, disco, rede, logs |
| 02 箱 | **Docker** | A tríade `ps → logs → exec`, inspect, stats, prune |
| 03 譜 | **Docker Compose** | Subir, derrubar, reconstruir e debugar env |
| 04 群 | **Kubernetes** | `get → describe → logs`, rollout, rollback, scale |
| 05 図 | **Terraform** | Plan antes do apply, state, import, drift |
| 06 雲 | **AWS CLI** | `sts` antes de tudo, EC2, S3, CloudWatch, ECS, SSM |

**~65 comandos** no total, cada um com explicação de *quando usar*.

## 🚨 Sala de Incidentes

Seis cenários **SEV-1/SEV-2** com ambiente que reage aos seus comandos e muda de estado. Os objetivos marcam sozinhos quando você acerta — e o cenário te corrige quando você erra (reiniciar um container em crash loop de config não resolve; `rm` num log com file descriptor aberto não libera espaço…).

| Incidente | Stack | A lição |
|-----------|-------|---------|
| 💾 Disco cheio — API fora do ar | Linux | `df → du → truncate` (não `rm`!) |
| 🔥 CPU em 100% — site arrastando | Linux | `top → kill` no PID certo |
| 🔁 Container em crash loop | Docker | Logs revelam a env quebrada |
| 💀 CrashLoopBackOff por OOM | Kubernetes | `describe` não mente; rollback rápido |
| 🌀 Drift — recurso criado no console | Terraform | `BucketAlreadyExists → import` |
| ⚡ Instância de produção parada | AWS | `sts` primeiro, depois `start-instances` |

## 🎖 Progressão

- **+5 XP** por comando novo executado · **+60 XP** por incidente resolvido
- Patentes: `CIVIL → CAPSULE → PILOTO → ESPER → AKIRA`
- Progresso salvo em `localStorage` (só no seu navegador)

## 🚀 Rodando

Não tem build, não tem dependência, não tem servidor:

```bash
git clone https://github.com/eduardonk9999/neo-tokyo-ops.git
open neo-tokyo-ops/index.html
```

Ou só abra a **[demo ao vivo](https://eduardonk9999.github.io/neo-tokyo-ops/)**.

## 🛠 Stack

HTML + CSS + JavaScript vanilla num arquivo só. Fontes [Chakra Petch](https://fonts.google.com/specimen/Chakra+Petch) e [Share Tech Mono](https://fonts.google.com/specimen/Share+Tech+Mono) via Google Fonts. Nada roda de verdade: todo terminal é simulado por regex + máquinas de estado por missão.

---

<div align="center">

**健康優良不良少年**

*Feito por [Eduardo Silva](https://github.com/eduardonk9999) — aprender fazendo, não decorando.*

</div>
