# AI Engineer in 90 Days — execution roadmap

## CO
Za 90 dní postavit přenositelný portfolio AI engineer artefakty, ne jen nasbírat repo bookmarks.

## PROČ
Firmu ani klienta nezajímá, že jsi prošel 10 GitHub rep. Zajímá je, jestli umíš:
- navrhnout use case
- postavit funkční prototyp
- vyřešit retrieval/evals/runtime
- udělat API
- popsat limity, cost, bezpečnost a trade-offs

## JAK
Roadmapa je rozdělená do 6 bloků.
Každej blok končí konkrétním artefaktem.

---

## Block 0 — setup a operating baseline (Days 1–5)

### Cíl
Připravit si prostředí tak, aby ses neuvařil na tooling bordelu.

### Udělej
- nainstaluj a ověř:
  - Python 3.11+
  - uv nebo pip + venv
  - git
  - Docker
  - Ollama
  - VS Code / Cursor / editor co používáš
- založ GitHub repo pro portfolio index, třeba:
  - `ai-engineer-90-days`
- vytvoř si pracovní strukturu:
  - `projects/`
  - `notes/`
  - `experiments/`
  - `artifacts/`

### Artefakt
- repo `ai-engineer-90-days`
- README s tím, co budeš 90 dní dělat

### Definition of done
- umíš rozjet Python projekt, commitnout ho a pushnout
- umíš lokálně spustit model přes Ollama

---

## Block 1 — Python + API + local LLM basics (Days 6–20)

### Cíl
Přestat bejt závislej na copy-paste kouzlech a mít backend základ.

### Nauč se
- Python základy pro produkční použití:
  - functions
  - classes jen kde dávaj smysl
  - typing
  - dataclasses / pydantic
  - async basics
- FastAPI:
  - GET/POST endpointy
  - request/response modely
  - error handling
- Ollama:
  - lokální inference
  - model selection
  - prompt in / output out

### Mini projekt 1
**Local LLM API wrapper**

Postav malou FastAPI appku, která:
- vezme prompt
- pošle ho do Ollama
- vrátí odpověď přes REST API
- loguje request/response metadata

### Repo requirements
- README
- jednoduchý diagram flow
- `.env.example`
- curl examples
- aspoň 3 testy

### Artefakt
- repo 1: `local-llm-api`

### Definition of done
- app běží lokálně
- má testy
- jde ji pustit podle README bez telepatie

---

## Block 2 — RAG fundamentals (Days 21–40)

### Cíl
Naučit se ingestion, chunking, retrieval a vector DB bez pohádek kolem.

### Repo focus
- `run-llama/llama_index`
- `qdrant/qdrant`
- optionally reference `awesome-llm-apps`

### Nauč se
- document ingestion
- chunking trade-offs
- embeddings basics
- retrieval pipeline
- vector DB operations

### Mini projekt 2
**Docs Q&A assistant**

Postav aplikaci, která:
- vezme složku dokumentů nebo markdownů
- naindexuje je do Qdrantu
- umí položit dotaz
- vrátí odpověď + cited source chunks

### Repo requirements
- README s architecture section
- sample documents
- ingestion script
- query script nebo API
- source citation output
- note o limitech a failure modes

### Artefakt
- repo 2: `docs-rag-assistant`

### Definition of done
- dokážeš ukázat, odkud odpověď vzala data
- umíš vysvětlit, proč retrieval funguje nebo selhává

---

## Block 3 — Evaluation layer (Days 41–50)

### Cíl
Přestat říkat "funguje to podle pocitu".

### Repo focus
- `vibrantlabsai/ragas`

### Nauč se
- faithfulness
- answer relevancy
- context precision/recall
- eval dataset basics

### Upgrade projektu 2
Přidej eval harness:
- malé test questions dataset
- Ragas evaluation run
- markdown nebo json report

### Artefakt
- eval report v repo `docs-rag-assistant`
- sekce README: "How we evaluate quality"

### Definition of done
- máš měřitelný baseline
- umíš říct, co zhoršuje / zlepšuje výsledky

---

## Block 4 — Agent workflows (Days 51–70)

### Cíl
Naučit se orchestrace bez toho, abys sklouzl do agent circus.

### Repo focus
- `langchain-ai/langchain`
- `langchain-ai/langgraph`
- `crewAIInc/crewAI` pouze jako optional srovnání
- `microsoft/ai-agents-for-beginners` jako orientační mapa

### Nauč se
- tools
- tool calling
- stateful workflow
- branching
- retry / failure handling
- human-in-the-loop

### Mini projekt 3
**Support / research workflow agent**

Postav workflow, kterej:
- přijme task
- rozhodne, co je potřeba dohledat
- zavolá retrieval nebo tool
- vrátí structured output
- loguje intermediate steps

### Repo requirements
- README s workflow diagramem
- jasně popsaný input/output contract
- ukázka failure modes
- note proč jsi zvolil LangGraph nebo jiný orchestrátor

### Artefakt
- repo 3: `agentic-workflow-demo`

### Definition of done
- workflow je opakovatelnej
- umíš ukázat stav, ne jen finální text

---

## Block 5 — MCP + packaging + brag mode (Days 71–85)

### Cíl
Přidat moderní integraci a udělat z toho něco, co se dá ukázat bez studu.

### Repo focus
- `punkpeye/awesome-mcp-servers`
- `Shubhamsaboo/awesome-llm-apps`

### Udělej
- připoj 1–2 MCP servery do jednoho z projektů
- nepřeháněj to, jeden practical use case stačí
- doplň:
  - Dockerfile
  - run instructions
  - screenshots / GIF / terminal capture
  - architecture image

### Artefakt
- jeden polished capstone repo
- jeden lightweight demo video nebo GIF

### Definition of done
- někdo cizí pochopí do 2 minut, co to dělá
- není to jen repo plný TODO a magie

---

## Block 6 — polish + interview readiness (Days 86–90)

### Cíl
Převést technickej bordel na portfolio, který se dá ukázat lidem.

### Udělej
- vyčisti README všech projektů
- přidej tags / topics na GitHub
- doplň root portfolio README:
  - co jsi stavěl
  - co ses naučil
  - co jsou limity
- vyplň `SHOWCASE_TEMPLATE.md`
- připrav si 5min a 15min verzi vysvětlení každýho projektu

### Artefakty
- portfolio index repo
- showcase doc
- 3 polished pinned repos

### Definition of done
- umíš se pochlubit bez toho, aby sis připadal jak podvodník
- každý projekt umíš obhájit technicky i prakticky

---

## Doporučenej order rep

### Core
1. `microsoft/ai-agents-for-beginners`
2. `ollama/ollama`
3. `langchain-ai/langchain`
4. `run-llama/llama_index`
5. `qdrant/qdrant`
6. `langchain-ai/langgraph`
7. `vibrantlabsai/ragas`

### Secondary
8. `Shubhamsaboo/awesome-llm-apps`
9. `punkpeye/awesome-mcp-servers`
10. `crewAIInc/crewAI`

## Weekly rhythm
- **Po–Út:** learn + prototype
- **St:** refactor + tests
- **Čt:** docs + README + cleanup
- **Pá:** ship něco malýho
- **So:** review co fungovalo a co bylo PNJ
- **Ne:** lehkej rest nebo jen notes

## Hard rules
- Každej 14denní blok musí skončit něčím na GitHubu
- Bez README se projekt nepočítá
- Bez testů nebo evals je to demo, ne portfolio
- Když něco nefunguje, napiš proč, ne že to "nějak blblo"
- Nehonit 12 frameworků naráz

## Red flags
- jen notebooky bez appky
- jen prompt engineering bez backendu
- jen agent hype bez evals
- repo bez run instrukcí
- všechno lokálně, nic nedokumentovaný

## Portfolio scoring rubric
Ohodnoť si každý projekt 0–2 body za:
- problém je srozumitelnej
- jde to spustit
- má to README
- má to testy nebo evals
- má to architekturu
- umíš vysvětlit trade-offs
- je tam nějaká práce s datama nebo retrieval
- je tam production-ish myšlení

**14–16 bodů** = dobrý, tohle už ukážeš bez křeče

## ROLLBACK
Když nestíháš, nesnižuj kvalitu všude, ale scope.

Osekej to takhle:
- CrewAI úplně pryč
- MCP jen lehce
- místo 3 velkejch projektů udělej 2 pořádný
- evals aspoň na 1 capstone
- radši jeden fakt dobrej repo než tři polomrtvý zombíky
