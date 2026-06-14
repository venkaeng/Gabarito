# 🧠 Gabarito

**Gabarito** é um aplicativo pessoal de diário comportamental, criado para registrar a jornada diária de forma rápida, humana e sem burocracia. Ele foi construído para funcionar na rua, no carro, entre compromissos — em qualquer momento em que você precise desabafar ou registrar o que está acontecendo na sua vida.


> *"Gabarito: a peça de referência que define o padrão perfeito. Não porque a perfeição seja alcançável — mas porque ter um norte claro é o que permite o aperfeiçoamento contínuo."*
---

## Por que ele foi criado?

A vida moderna acumula múltiplos papéis simultâneos: profissional, pai, esposo, filho, devoto. Cada um com suas demandas, imprevistos e cobranças. O problema não é falta de planejamento — é que o **planejamento ideal raramente sobrevive ao contato com a realidade**.

O Gabarito nasceu para mapear essa realidade com honestidade:

- O que está consumindo sua energia de verdade?
- Quando você foge de uma tarefa, é cansaço biológico ou bloqueio mental?
- Quais projetos cabem genuinamente na sua rotina atual?

Sem cobranças robóticas. Sem perfeição. Apenas um espelho claro da realidade para reajustes cirúrgicos de rota.

---

## Como utilizar

### Acesso
Abra o link abaixo no **Chrome para Android** (recomendado):

```
https://venkaeng.github.io/Gabarito/gabarito.html
```

Para instalar como app: toque nos **três pontinhos** do Chrome → **Adicionar à tela inicial**.

---

### As três métricas (registre antes de cada relato)

| Métrica | O que mede | Escala |
|---|---|---|
| 🔋 **Energia** | Seu estado biológico no momento | Baixo (Esgotado) $\rightarrow$ Alto (Pleno) | 1, 3, 5 |
| 🎯 **Foco** | Sua capacidade de concentração agora | Baixo (Disperso) $\rightarrow$ Alto (Focado) | 1, 3, 5 |
| 🧱 **Resistência** | O quanto você está evitando a tarefa | Baixo (Fluindo) $\rightarrow$ Alto (Bloqueio Total) | 1, 3, 5 |

A **Resistência** é especialmente importante: ela permite à IA distinguir se você deixou de fazer algo por **esgotamento real** ou por **fricção cognitiva** com a tarefa em si. São causas diferentes que exigem soluções diferentes.

---

### As quatro abas do app

**📝 Registrar**
Toque no botão gigante de microfone e fale. O app transcreve em tempo real. Ajuste as métricas antes ou depois. Toque em **Salvar registro**.

**📋 Histórico**
Todos os seus registros em ordem cronológica, com as métricas em destaque visual.

**📈 Evolução**
Gráfico dos últimos 14 dias mostrando a curva de Energia, Foco e Resistência. Aqui também ficam os botões de exportação.

**⚙️ Config**
Configure os lembretes automáticos via Telegram e gerencie seus backups.

---

### Backup dos dados

Os dados ficam salvos no navegador do seu celular. Para não perder nada:

1. Vá em **⚙️ Config** → **Backup e Restauração**
2. Toque em **Baixar shec_backup.json**
3. Guarde o arquivo no Google Drive ou envie para si mesmo no WhatsApp/Telegram

Para restaurar ou sincronizar com outro dispositivo, use **Importar backup** — o app faz fusão inteligente, sem duplicar registros.

---

### Lembretes via Telegram

Para receber notificações nos horários que escolher:

1. No Telegram, pesquise **@BotFather** → digite `/newbot` → siga as instruções → copie o **Token**
2. Abra seu novo bot e aperte **Iniciar**. Acesse `https://api.telegram.org/bot[TOKEN]/getUpdates` e copie o número em `"id"` dentro de `"chat"`
3. Em **⚙️ Config**, cole o Token e o Chat ID → escolha os horários → **Salvar**
4. Toque em **Enviar mensagem de teste** para confirmar

---

## Como usar os dados com Inteligência Artificial

O verdadeiro poder do Gabarito está na análise semanal. Ao final de cada semana, exporte o arquivo **`diario_semanal.md`** (aba 📈 Evolução) e alimente uma IA com os três prompts abaixo em **chats separados** — isso evita que os contextos se misturem e garante análises mais precisas.

---

### 📁 Arquivo de histórico pessoal: `perfil_comportamental.md`

Crie e mantenha atualizado um arquivo pessoal com duas seções:

```
## Arsenal de Sucesso
Estratégias e hábitos que funcionaram e estão ativos.

## Laboratório de Hibernação
Táticas testadas por 14-21 dias sem adesão. 
A IA não deve sugerir estas enquanto seu contexto de vida for o mesmo.
```

---

### 🔍 Lente 1 — O Engenheiro de Processos (Chat A)

Cole este prompt + o conteúdo do `diario_semanal.md`:

```
Você é um Engenheiro de Processos especialista em gestão de tempo. 
Analise cronologicamente o diário fornecido. Ignore julgamentos de culpa 
ou desabafos emocionais. Monte de forma puramente estatística:

1) O mapa da Rotina Real: quantas horas/blocos são consumidos por 
   imprevistos e obrigações fixas (família, logística, saúde).
2) Os horários e dias da semana onde os desvios ocorrem com maior frequência.
3) O bloco real de tempo útil restante para trabalho focado.
```

---

### 🧠 Lente 2 — O Mentor Comportamental (Chat B)

Cole este prompt + o `diario_semanal.md` + o resultado da Lente 1 + o `perfil_comportamental.md`:

```
Você é um psicólogo cognitivo-comportamental e mentor de produtividade humanizada.

1) Cruze os desvios de rota com as métricas de Energia, Foco e Resistência. 
   Identifique se o usuário foge das tarefas por exaustão biológica real 
   ou por fricção cognitiva (bloqueio com a complexidade da tarefa).

2) Aplique o Princípio de Pareto (80/20): identifique a única mudança 
   comportamental que trará o maior impacto positivo.

3) Consulte a seção "Laboratório de Hibernação" do perfil histórico e 
   não sugira táticas congeladas lá, a menos que o contexto de vida 
   do usuário tenha mudado visivelmente.

4) Gere um "Card de Conquista" em HTML/Markdown destacando uma vitória 
   ou ajuste de rota consciente feito pelo usuário nesta semana.
```

---

### 🗺️ Lente 3 — O Alinhador de Expectativas (Chat C)

Cole este prompt + o `diario_semanal.md` + o resultado da Lente 1:

```
Você é um estrategista de vida e analista de expectativas.

Filtre todas as menções a desejos, ambições, novos projetos ou cobranças 
de longo prazo (pessoais, profissionais, familiares, espirituais).

Cruze esses desejos com a Rotina Real mapeada pela Lente 1.

Faça o alinhamento de expectativas: alerte se o usuário está sofrendo 
por tentar abraçar o mundo. Indique quais projetos paralelos devem ser 
colocados "na geladeira" para o próximo semestre e quais realmente 
cabem no cenário atual de energia.
```

---

## Filosofia do projeto

- **Custo zero** — 100% gratuito, sem assinaturas, sem dependências pagas
- **Fricção mínima** — registrar deve ser tão fácil quanto apertar um botão no semáforo
- **Humanizado** — foco em energia e psicologia cognitiva, não em produtividade robótica
- **Princípio de Pareto** — identificar os 20% de causas que geram 80% dos desvios
- **Privacidade total** — seus dados ficam no seu celular, nunca em servidores de terceiros

---

## Tecnologia

- HTML + CSS + JavaScript puro (zero dependências, zero frameworks)
- Web Speech API nativa do Chrome (transcrição de voz gratuita e ilimitada)
- localStorage para persistência de dados
- Telegram Bot API para lembretes
- GitHub Pages para hospedagem gratuita

---

*Projeto pessoal. Dados privados armazenados localmente no dispositivo do usuário.*
