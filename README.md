# 🔥 App INPE — Focos de Calor e Áreas Queimadas

> Projeto desenvolvido na **Fatec-Jacareí** · Curso de Desenvolvimento de Software Multiplataforma (DSM) · 3º Semestre

---

## 📋 Sobre o Projeto

Aplicativo mobile desenvolvido com dados abertos do **INPE (Instituto Nacional de Pesquisas Espaciais)** para monitoramento de focos de calor e áreas queimadas no Brasil. O objetivo é tornar essas informações **acessíveis e compreensíveis** para diferentes perfis de usuários — do produtor rural ao analista ambiental.

---

## 👥 Personas do Projeto

> As personas foram construídas com base em dados secundários do **Programa Queimadas/INPE**, documentação do sistema **TerraMA2Q** e pesquisas sobre perfis de usuários de sistemas de monitoramento ambiental no Brasil.

---

### 👨‍🌾 Persona 3 — Raimundo Silva, 58 anos

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   👨‍🌾  RAIMUNDO SILVA                          PERSONA #03      │
│       58 anos · Produtor Rural · Pecuarista                     │
│       📍 Altamira, Sudoeste do Pará                             │
│                                                                 │
│   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━    │
│                                                                 │
│   🏡  Propriedade: 40 hectares (gado, mandioca, milho)          │
│   📱  Dispositivo: Samsung Android básico (Android 10)          │
│   📶  Conexão: 3G instável (piora em dias de chuva)             │
│   🎓  Escolaridade: Ensino Fundamental                          │
│   💬  App mais usado: WhatsApp (diariamente)                    │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

#### 🧍 Quem é ele

Raimundo tem uma propriedade de **40 hectares** no sudoeste do Pará, onde cria gado e cultiva mandioca e milho. Nunca estudou além do ensino fundamental e **aprendeu a usar o celular com o filho mais novo**, de 22 anos, que mora na cidade.

Acessa o WhatsApp todos os dias, mas **raramente instala apps novos** — só o faz quando alguém de confiança indica e mostra como usar. Trabalha ao ar livre com o celular no bolso e a **tela no brilho máximo** por causa do sol forte.

---

#### 🎯 Objetivos

| # | Objetivo | Por quê é importante |
|---|----------|----------------------|
| 1 | Saber com antecedência se há fogo chegando perto da propriedade | Para tirar o gado do pasto a tempo |
| 2 | Acionar vizinhos e a defesa civil com antecedência | Tempo de resposta é crítico em incêndios rurais |
| 3 | Receber informação clara, sem precisar interpretar nada | Não tem familiaridade com linguagem técnica ou mapas digitais |
| 4 | Saber a distância do foco em **quilômetros**, não em mapa | Um ponto no mapa não significa nada para ele |

---

#### 😤 Frustrações e Barreiras

> ⚠️ **Barreira Digital**
> Já tentou usar o portal do INPE uma vez, mas desistiu porque o mapa carregou lento e apareceram *"um monte de pontinhos vermelhos espalhados"* sem ele entender se algum era perto de casa.

> ⚠️ **Linguagem Técnica**
> Não sabe o que significa **"foco ativo"**, **"risco alto"** ou **"bioma Amazônia"**. Sem contexto, esses termos não comunicam nada para ele.

> ⚠️ **Falta de Confiança no App**
> Quando recebe um alerta genérico sem localização clara, **ignora**. Já aprendeu que *"coisa de app costuma ser exagero"*.

> ⚠️ **Conectividade Instável**
> Sinal 3G fraco, especialmente de manhã cedo e em dias de chuva. Apps pesados travam antes de carregar a informação.

---

#### 📱 Tecnologias Usadas

```
📱 Smartphone    →  Samsung básico · Android 10 · tela no brilho máximo
📶 Internet      →  3G instável (zona rural) · piora em dias de chuva
💬 App favorito  →  WhatsApp (grupos de agricultores da região)
🗺️ Mapas/GPS    →  Nunca usou · não tem referência espacial digital
```

---

#### 🗣️ Citação Realista

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  "Eu não preciso de mapa não. Me manda uma mensagem falando:     ║
║   'Raimundo, tem fogo a 5 km de você, cuidado' — isso eu        ║
║   entendo. Esse negócio de pontinho vermelho no mapa             ║
║   não me diz nada."                                              ║
║                                                                  ║
║                          — Raimundo Silva, 58 anos               ║
║                            Produtor Rural · Altamira, PA         ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

---

#### 💡 O que essa persona exige do App

| Dor identificada | Decisão de design |
|------------------|-------------------|
| ⚠️ Não lê mapas técnicos | Alerta em **linguagem natural**, sem depender do mapa |
| ⚠️ Internet instável | App **leve**, carregamento rápido, funcionar parcialmente offline |
| ⚠️ Não estima distância no mapa | Mostrar **distância em km** do foco até a localização do usuário |
| ⚠️ Só confia em quem conhece | Onboarding simples + identificação clara que os dados são do **INPE** |
| ⚠️ Usa WhatsApp | Notificação push simples + botão **"Compartilhar no WhatsApp"** |
| ⚠️ Tela ao sol | Garantir **contraste alto** e fonte legível em ambientes externos |

---

#### 🗺️ Jornada Resumida

```
📲 Recebe          🔍 Abre           🗺️ Vê             ❓ Tenta           ✅ Age
   notificação  →     o app      →     o mapa      →     entender     →     
                                                                         
   😟 Ansioso       😤 Impaciente    😰 Assustado      😖 Frustrado      😌 Aliviado
   "O que é isso?"  "Por que         "Onde fica        "O que é          (só com
                     demora tanto?"   minha fazenda?"   'foco ativo'?)    ajuda do filho)
```

> 🔴 **Pico de frustração:** Etapa 4 — Raimundo não consegue interpretar os termos técnicos e precisa ligar para o filho para entender se está em perigo.

---

## 🔗 Recursos do Projeto

- 📄 [Mapa de Jornada Completo](./jornada-raimundo.html)
- 📊 [Todas as Personas](./personas/)
- 🎨 [Protótipo de Telas](./prototipo/)

---

## 📚 Referências das Personas

As personas foram baseadas em fontes reais:

- **INPE** — Programa Queimadas: documentação do público-alvo do sistema
- **TerraMA2Q** — Adotado por secretarias estaduais do Acre, Tocantins e Piauí; identifica gestores municipais, fiscais do IBAMA e Corpo de Bombeiros como usuários principais
- **Governo de SP** — Operação Corta Fogo: uso dos dados do INPE desde 2011 pela Polícia Militar Ambiental
- **Pesquisa UFV (2005)** — Perfil de produtores rurais e uso irregular do fogo na agricultura

---

## 🛠️ Tecnologias do Projeto

![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![INPE](https://img.shields.io/badge/Dados-INPE-orange?style=for-the-badge)

---

## 👨‍💻 Desenvolvedor

**Felipe Ribeiro**
Engenheiro de Produção (UNIVESP) · DSM — Fatec-Jacareí · 3º Semestre

[![GitHub](https://img.shields.io/badge/GitHub-feliperib286-181717?style=flat&logo=github)](https://github.com/feliperib286)
[![Portfólio](https://img.shields.io/badge/Portf%C3%B3lio-feliperib286.github.io-orange?style=flat)](https://feliperib286.github.io/Portifolio-DSM/)

---

> *Projeto acadêmico desenvolvido na Fatec-Jacareí como parte do curso de Desenvolvimento de Software Multiplataforma (DSM) — 3º Semestre, 2025.*
