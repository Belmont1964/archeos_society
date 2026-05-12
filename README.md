# Archeos Society – Edição Digital 🏛️🃏

**Archeos Society – Digital Edition** é a versão online do famoso jogo de tabuleiro criado por **Paolo Mori**, recriando a experiência de expedições arqueológicas em um ambiente digital interativo. Desenvolvido como projeto acadêmico de **Sistemas de Informação na Universidade Federal Fluminense (UFF)**, o sistema permite que **2 a 6 jogadores** competam estrategicamente para explorar sítios arqueológicos, recrutar especialistas e administrar recursos limitados, com o objetivo de **acumular o maior prestígio científico e social ao longo de várias temporadas**.

A versão digital mantém fielmente as mecânicas do tabuleiro, incluindo:

* **Gestão de cartas e especialistas:** planejamento tático de arqueólogos, botânicos, médicos e guias.
* **Eventos estratégicos:** cada sítio arqueológico apresenta desafios únicos; a terceira carta de macaco encerra a temporada e reorganiza o mercado de cartas.
* **Pontuação e progresso:** evolução de veículos e habilidades dos especialistas, com pontuação transparente.
* **Interatividade digital:** decisões em tempo real, preservando a complexidade estratégica do jogo físico.

---

## 🚀 Stack Tecnológica

* **Frontend:** React + Vite (TypeScript, Tailwind CSS v4)
* **Backend:** FastAPI (Python 3.11, Pydantic)
* **Persistência:** SQLAlchemy + SQLite (estado completo do jogo serializado em JSON)
* **Infraestrutura:** Docker & Docker Compose (multi-stage builds)
* **Comunicação:** API RESTful modular (macrogestão de partidas e microgestão de turnos)

---

## 🛠️ Arquitetura e Decisões de Projeto

* **Core Engine (Backend):** valida todas as regras do manual (limite de 10 cartas na mão, bloqueio de ações fora de turno, gatilho da 3ª carta de macaco).
* **Interface (Frontend):** React + Vite com tipagem TypeScript que espelha os contratos da API, garantindo consistência de estado durante a partida.

---

## 📋 Regras Implementadas (MVP)

* **Gestão de Mão:** limite estrito de 10 cartas por jogador.
* **Mecânica de Macacos:** a terceira carta encerra a temporada, limpando mercado e mesa.
* **Expedições:** líderes e especialistas (Guia, Botânico, Médico, Professor, etc.) com habilidades diferenciadas.
* **Sítios Arqueológicos:** progressão de veículos, pontuação ajustável (Lado A básico / Lado B avançado).

---

## 💻 Como Executar

O projeto pode ser rodado **localmente** ou via **Docker**.

### 1️⃣ Backend (FastAPI)

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
pip install .
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```

* API disponível: [http://localhost:8000](http://localhost:8000)
* Swagger: [http://localhost:8000/docs](http://localhost:8000/docs)

---

### 2️⃣ Frontend (React + Vite)

```bash
cd frontend
npm install
cp .env.example .env
npm run dev
```

* Frontend disponível: [http://localhost:5173](http://localhost:5173)

---

### 3️⃣ Docker (opcional)

```bash
docker-compose up --build
```

* Inicia backend e frontend juntos sem necessidade de configuração local.

---

## 👥 Equipe de Desenvolvimento

* Sandro Luis Flausino Junior
* Yuri Moura
* Caio Brasil
* José Augusto
* Alysson Rocha
* Rafael Fernandes

