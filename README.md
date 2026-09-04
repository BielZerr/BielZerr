<div align="center">

# Gabriel Souza

**Software Engineer @ Nubank** · Clojure · Event-driven · Platform

<p>
  <img src="https://img.shields.io/badge/Nubank-8A05BE?style=for-the-badge&logo=nubank&logoColor=white" alt="Nubank">
  <img src="https://img.shields.io/badge/Clojure-5881D8?style=for-the-badge&logo=clojure&logoColor=white" alt="Clojure">
  <img src="https://komarev.com/ghpvc/?username=BielZerr&style=for-the-badge&color=8A05BE&label=VISITAS" alt="views">
</p>

</div>

---

## 👋 Oi, eu sou o Gabriel, mais conhecido como Biel!

Sou **Software Engineer no Nubank**, trabalhando com **backend em Clojure** e arquitetura de **microsserviços orientados a eventos**.

Meu dia a dia é construir serviços que conversam entre si por **Kafka**, expõem **APIs HTTP** com contratos bem definidos, persistem em **Datomic**, rodam na **AWS** e são observados no **Datadog**. Gosto do tipo de problema em que o sistema precisa ser **idempotente**, sobreviver a reentrega de mensagens e continuar correto quando uma integração externa cai no meio do caminho — porque é exatamente isso que acontece na prática.

Antes de escrever código, eu gasto tempo desenhando o fluxo. Depois disso, a implementação é quase consequência.

```clojure
(ns gabriel.core
  (:require [nubank.engineering :as eng]
            [schema.core :as s]))

(def gabriel
  {:role       "Software Engineer @ Nubank"
   :focus      [:backend :event-driven :platform :automation]
   :languages  ["Clojure" "Python"]
   :daily      #{:kafka :datomic :aws :datadog :rest-apis :okta}
   :arch       "diplomat → controller → logic (I/O na borda, lógica pura no centro)"
   :philosophy "Fluxo desenhado antes de código escrito."
   :location   "Brasil 🇧🇷"})

(s/defn open-to-work? :- s/Bool
  "Sempre aberto a trocar ideia sobre sistemas distribuídos."
  [_] true)
```

---

## 🛠️ No que eu trabalho

**Automação de ciclo de vida e plataforma interna** — serviços que substituem processos manuais e workflows low-code por código versionado, testado e observável.

- 🐝 **Microsserviços event-driven em Clojure** — produtores e consumidores Kafka, contratos com *schema*, idempotência sob reentrega, e adaptadores `wire ↔ model` na fronteira.
- 🔌 **Integrações com sistemas de terceiros** — HCM/RH, identity providers, MDM, assinatura eletrônica, ticketing. Muita API alheia, muita borda instável, muito *guard-rail*.
- ⚡ **Automação de processos ponta a ponta** — rotinas diárias que leem uma fonte de verdade, resolvem regras de negócio e disparam ações reais em vez de gerar tarefa pra alguém fazer na mão.
- 🌎 **Rollout multi-país** — parametrização por país, *feature flags*, i18n e janelas de compatibilidade pra migrar sem quebrar o que já está em produção.
- 📊 **Observabilidade** — contadores de falha de integração, alertas de latência e error rate, e dashboards que apontam *qual* foi o motivo dominante da falha, não só que falhou.
- 🔐 **Hardening** — segredo fora do código (Secrets Manager), sanitização de saída, e revisão de superfície de permissão junto com Security.
- 🧹 **Migração e decommission** — a parte menos glamourosa e mais importante: desligar o legado depois que o novo já está de pé.

> Detalhes de sistemas internos ficam de fora daqui de propósito. Se quiser trocar ideia sobre a arquitetura por trás disso, é só chamar.

---

## 🧰 Stack

**Linguagens**

![Clojure](https://img.shields.io/badge/Clojure-5881D8?style=for-the-badge&logo=clojure&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)

**Dados & Mensageria**

![Apache Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![Datomic](https://img.shields.io/badge/Datomic-2E3E4E?style=for-the-badge&logo=clojure&logoColor=5881D8)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

**Cloud & Infra**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=FF9900)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white)

**Observabilidade**

![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=for-the-badge&logo=datadog&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![PagerDuty](https://img.shields.io/badge/PagerDuty-06AC38?style=for-the-badge&logo=pagerduty&logoColor=white)

**Web & Ferramentas**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

---

## 🧠 Como eu penso sobre software

```
┌─────────────────────────────────────────────────────────────┐
│                                                              │
│   1.  I/O na borda. Lógica pura no centro.                   │
│       Se a regra de negócio precisa de mock pra ser           │
│       testada, ela está no lugar errado.                      │
│                                                              │
│   2.  Todo consumidor vai receber a mesma mensagem duas       │
│       vezes. Idempotência não é otimização, é requisito.      │
│                                                              │
│   3.  Migração só termina quando o legado é desligado.        │
│       Rodar os dois em paralelo pra sempre é dívida, não      │
│       segurança.                                              │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

---

## 📈 Sobre o gráfico aqui do lado

A maior parte do que eu escrevo vive em repositórios privados de trabalho. Então a lista de repos públicos aqui é curta de propósito — o gráfico de contribuições conta mais história do que ela.

---

## 📫 Fala comigo

Se você trabalha com **Clojure**, **sistemas orientados a eventos** ou **automação de plataforma interna** — ou só quer discutir por que o `reduce` resolve mais coisa do que parece — manda mensagem.

<div align="center">

<a href="https://github.com/BielZerr"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>

<br><br>

<sub><code>(println "Obrigado por passar por aqui. 🟣")</code></sub>

</div>
