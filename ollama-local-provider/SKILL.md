---
name: ollama-local-provider
description: >
  Skill para integrar o Ollama (servidor local de LLMs) ao Antigravity e Hermes Master.
  Permite executar modelos como DeepSeek-R1, Qwen2.5-Coder, Llama3.3 e Mistral 100% offline,
  com custo zero de API, sem limites de tokens e com privacidade total.
  Gatilhos: "ollama", "llm local", "offline", "deepseek local", "qwen local", "sem api", "custo zero".
---

# SKILL: Ollama Local LLM Provider

## 📌 Visão Geral
O Ollama é um servidor local de modelos de linguagem de código aberto (100% gratuito).
Esta skill habilita o Antigravity e o Hermes Master a rotearem chamadas de IA diretamente para a máquina local (`http://localhost:11434`) ou para a VPS da Oracle Cloud (`http://137.131.177.17:11434`).

---

## 🛠️ Modelos Recomendados para o Nosso Ecossistema

1. **`qwen2.5-coder`** (Codificação & Programação):
   - Modelo focado em gerar código limpo em TypeScript, Python e SQL.
   - Comando para baixar: `ollama run qwen2.5-coder`

2. **`deepseek-r1`** (Raciocínio Lógico Avançado & Diagnóstico):
   - Excelente para resolver problemas complexos e planejar arquiteturas.
   - Comando para baixar: `ollama run deepseek-r1:8b`

3. **`llama3.3`** (Copywriting & Atendimento):
   - Ideal para geração de textos para o `araujo-make` e automação de suporte.
   - Comando para baixar: `ollama run llama3.3`

---

## 🔗 Integração com Antigravity & Hermes

### API OpenAI-Compatible (Porta 11434)
O Ollama expõe um endpoint idêntico ao da OpenAI em `http://localhost:11434/v1`.
Qualquer ferramenta ou agente do Hermes pode consumi-lo enviando a chave de API fictícia `ollama`:

```python
import openai

client = openai.OpenAI(
    base_url="http://localhost:11434/v1",
    api_key="ollama" # Não é necessário pagamento
)

response = client.chat.completions.create(
    model="qwen2.5-coder",
    messages=[{"role": "user", "content": "Escreva uma função de retry em Python."}]
)
print(response.choices[0].message.content)
```

---

## 💡 Vantagens Estratégicas para o Projeto
- **Custo R$ 0,00**: Sem cobrança por token de entrada ou saída.
- **Privacidade Máxima**: Os dados do TV Araújo e UTM.ai permanecem no seu hardware.
- **Operação Offline**: Funciona mesmo se a internet cair.
