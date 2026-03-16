---
theme: seriph
highlighter: shiki
drawings:
  persist: false
transition: slide-left
comark: true
mdc: true
status: done
---

<div class="absolute inset-0 bg-black" />

---
title: "Copilots & Creators: Build with AI"
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
info: |
  Workshop: Copilots & Creators – Build with AI
  17 maart 2026 | Centric
status: done
---

# Copilots & Creators
## Build with AI

Bouw sneller, bedenk gedurfder

<div class="pt-12 text-gray-400">
  17 maart 2026 · Teams · 2 uur
</div>

<!--
Welkom iedereen!

Vragen policy: hand opsteken mag, maar tussendoor vragen mag ook gewoon.
Slides worden na de workshop gedeeld.
-->

---
status: done
---

# Wat gaan we doen vandaag?

- AI als **versneller** én **inspiratiebron**
- Hands-on met AI-codeassistenten en generatieve tools
- Van prompt naar praktijk

<br>

> Niet de tool bepaalt het idee - **jij wel**

<!--
Kort de agenda doornemen:
- Intro & context (0:00 – 0:15)
- Blok 1: Slimmer bouwen met AI (0:15 – 1:00)
- Pauze (1:00 – 1:15)
- Blok 2: Integratie & best practices (1:15 – 1:45)
- Wrap-up & showcase (1:45 – 2:00)
-->

---
layout: section
status: done
---

# Intro & Setting the Stage
## 0:00 – 0:15

<!--
Jezelf voorstellen.
Kort peilen: wie gebruikt al AI in hun dagelijkse werk?
Welke tools kennen ze (Copilot, ChatGPT, etc.)?
-->

---
status: done
---

# Wat kan moderne AI-tooling?

- **Github Copilot** – inline code suggesties in je editor
- **Code-assistenten** – refactoring, uitleg, tests via chat
- **CLI-tools** – GitHub Copilot CLI, Claude Code, en andere terminal-gebaseerde assistenten
- **Generatieve AI** – brainstorm, documentatie, ontwerp

<!--
Onderscheid tussen de categorieën toelichten:
- GitHub Copilot = inline suggesties in de IDE
- Code-assistent = het chat-venster in GitHub Copilot
- CLI-tools = vandaag de focus: GitHub Copilot CLI. Vermeld ook Claude Code en alternatieven.
- Generatieve AI = elke LLM chat interface (ChatGPT, Claude, etc.)
-->

---
layout: section
status: done
---

# Blok 1 – Slimmer Bouwen met AI
## 0:15 – 1:00

---
status: done
---

# Prompt-Basics & Patterns

Effectieve prompts schrijven voor:

- **Code generatie** – snel een basis neerzetten
- **Tests** – unit tests automatiseren
- **Refactoring** – bestaande code verbeteren
- **Documentatie** – uitleg en comments genereren

---
status: done
---

# Plan eerst, bouw daarna

Voordat je AI laat schrijven — laat het eerst **meedenken**

<br>

1. Beschrijf het probleem aan je CLI-agent
2. Laat AI een plan opstellen in een markdown-bestand
3. Itereer op het plan tot het klopt
4. Pas dan ga je naar implementatie

<br>

> De kwaliteit van je output begint bij de kwaliteit van je plan

<!--
Dit is een eigen workflow: werk eerst een plan uit met een CLI-agent (bijv. GitHub Copilot CLI of Claude Code).
Sla het op als markdown, itereer erop, werk details uit.
Pas daarna geef je het groene licht voor implementatie.
Dit voorkomt dat je halverwege bijstuurt en de output veel beter.
-->

---
status: done
---

# Hands-on: Codegeneratie

```
Taak: genereer een functie die...
Constraint: gebruik geen externe libraries
Output: voeg inline comments toe
```

<br>

> Bij CLI-tools en IDE-chat is je codebase al de context — die hoef je niet te herhalen

<br>

**Probeer het zelf:**
1. Kies een bestaande functie uit je eigen project
2. Vraag AI om het uit te breiden
3. Vraag AI om edge-cases te identificeren

<!--
Context weglaten is bewust: CLI-tools (GitHub Copilot CLI, Claude Code) en het chat-venster in VS Code/IDE
hebben al toegang tot de codebase. Context toevoegen is alleen nodig bij een externe chat (ChatGPT, Claude.ai)
zonder code-integratie. In deze workshop gaan we ervan uit dat iedereen CLI of IDE-chat gebruikt.
-->

---
status: in-progress
---

# Mini-challenge

> **"Maak een bestaande functie robuuster met AI"**

<br>

1. Kies een functie die je kent
2. Gebruik AI om het volgende te genereren:
   - Input validatie
   - Foutafhandeling
   - Unit tests
3. Bekijk wat AI mist — en waarom

⏱ 15 minuten

<!--
TODO: hoe faciliteer ik dit?
- Werken mensen alleen of in tweetallen?
- Loop ik rond, of is er een gedeeld scherm?
- Hoe deel ik de resultaten daarna plenair?
-->

---
layout: statement
status: done
---

# Pauze
## 1:00 – 1:15

---
layout: section
status: done
---

# Blok 2 – Integratie & Best Practices
## 1:15 – 1:45

---
status: in-progress
---

# AI in je dagelijkse workflow

| Fase | AI-toepassing |
|------|--------------|
| Code review | Eigen changes vóór push · PR review via `git diff` + CLI agent |
| CI/CD | Test generatie, changelog |
| Documentatie | Automatisch bijwerken |
| Onboarding | Codebase uitleg · `agents.md` genereren als persistent context |

<!--
TODO: slide nog verder uitwerken

Code review - twee scenario's:
1. Eigen changes: staged diff reviewen met CLI agent voor je pusht — eenvoudig
2. PR van collega: platform-onafhankelijk via git:
   - git fetch origin
   - git diff main...origin/<branch>
   - Feed diff aan CLI agent (werkt op GitHub, Azure DevOps, GitLab, etc.)
   - gh CLI is alleen een shortcut voor GitHub gebruikers
   - Kwaliteit van de review staat of valt met een goede agents.md/CLAUDE.md in de repo

Onboarding:
- CLI agent uitleg laten geven over de codebase
- agents.md laten genereren door de AI zelf → dient daarna ook als persistente context voor de agent
- TODO: agents.md concept verder uitleggen — misschien eigen slide?

CI/CD en Documentatie: nog verder uitwerken
-->


---
status: done
---

# Valkuilen

- **Bias** – AI reproduceert patronen uit trainingsdata
- **Security** – nooit blindeling credentials of secrets meegeven
- **Privacy** – geen klantdata in publieke AI-tools
- **Kwaliteit** – AI heeft altijd menselijke review nodig

<br>

> AI is een **co-pilot**, geen autopilot

<!--
Bias: geef een concreet voorbeeld voor developers — AI stelt soms verouderde patronen voor
of onveilige code, simpelweg omdat dat veel voorkomt in de trainingsdata.

Security & Privacy zijn verwant maar onderscheiden:
- Security: nooit API keys, wachtwoorden of secrets in je prompt plakken
- Privacy: geen klantdata, persoonsgegevens of bedrijfsgevoelige info in publieke tools
- Vermeld: sommige tools hebben enterprise-varianten (bijv. GitHub Copilot for Business)
  waarbij data de organisatie niet verlaat — dat verandert de afweging.

Kwaliteit: benadruk dat AI zelfverzekerd foute code kan genereren. Review is geen optie, het is verplicht.
-->

---
status: done
---

# AI-ready Developer Mindset

<v-clicks>

- Formuleer **context** voor je prompt, niet alleen het verzoek
- Gebruik AI voor **verkenning**, jij neemt de beslissing
- Controleer output altijd op correctheid en veiligheid
- Bouw **herbruikbare prompt-patterns** op
- Ken de **grenzen** van je tool

</v-clicks>

<!--
"Formuleer context" geldt vooral voor externe chat-interfaces zonder codebase-toegang.
Bij CLI-tools en IDE-chat is de context al aanwezig — benadruk dit onderscheid expliciet,
want anders klinkt dit punt tegenstrijdig met wat eerder gezegd is over het weglaten van context.

"Herbruikbare prompt-patterns" sluit mooi aan op de planning-slide: een goed plan is zelf ook een prompt-patroon.
-->

---
layout: section
status: done
---

# Wrap-up & Showcase
## 1:45 – 2:00

---
status: in-progress
---

# Demo's

Laat zien wat je hebt gemaakt tijdens de mini-challenge

- Wat was de input?
- Wat genereerde AI?
- Wat paste je aan?

<!--
TODO: zelfde open vragen als bij de mini-challenge:
- Wie presenteert? Iedereen, vrijwilligers, of random?
- Hoeveel tijd per persoon?
- Is er een gedeeld scherm of loopt iedereen naar voren?
- Hoe sluit ik dit blok af naar de takeaways?
-->

---
status: done
---

# Takeaways

- Prompts zijn **ontwerpartefacten** — schrijf ze bewust
- AI versnelt het **routinewerk**, jij doet het denkwerk
- Integreer stap voor stap: één workflow tegelijk
- Blijf kritisch: **review alles** wat AI genereert

---
status: in-progress
---

# Resources

- [Slidev](https://sli.dev) – deze presentatie
- [GitHub Copilot docs](https://docs.github.com/copilot)
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [OWASP AI Security](https://owaspai.org/)

<br>

**Vragen?**

<!--
TODO: een gedeelde link naar deze slide aanmaken en communiceren naar de deelnemers.
Bijv. via Netlify, Vercel, of een interne SharePoint/Teams-post.
-->

---
layout: end
status: done
background: https://cover.sli.dev
---

# Bedankt!

Copilots & Creators · 17 maart 2026

<br>

> "AI won't replace humans — but humans with AI will replace humans without AI."
> <span class="text-sm text-gray-400">— Karim Lakhani, Harvard Business School</span>
