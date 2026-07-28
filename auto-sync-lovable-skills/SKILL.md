---
name: auto-sync-lovable-skills
description: >
  Regra rígida de sincronização automática.
  Garante que sempre que uma nova skill for criada, alterada ou adicionada ao Antigravity ou Hermes,
  ela seja imediatamente adicionada e espelhada no pacote master do Lovable (lovable_skills_master_pack.json),
  no Obsidian Vault e nos arquivos individuais .md para manter 100% de paridade.
  Gatilhos: "nova skill", "criar skill", "adicionar skill", "sync lovable", "atualizar skills".
---

# SKILL: Auto-Sync Skills to Lovable

## 📌 Regra Rígida de Execução
Toda e qualquer criação, modificação ou remoção de skill no Antigravity ou no Hermes Master DEVE acionar automaticamente o script:
`python C:\Users\marcu\AppData\Local\hermes\scripts\injetar_todas_skills_lovable.py`

Isso garante que o Lovable NUNCA fique desatualizado e sempre tenha acesso a 100% da biblioteca de skills.
