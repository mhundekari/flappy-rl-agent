# Flappy Bird mit Reinforcement Learning (DQN)

Dieses Projekt implementiert einen RL-Agenten auf Basis von Deep Q-Learning (DQN), der das Spiel Flappy Bird erlernen soll. Ziel war es, zentrale Konzepte der Vorlesung praktisch anzuwenden und kritisch auf eine eigenständig gewählte Umgebung zu übertragen.

---

## 📂 Projektstruktur

- `notebook/flappy_agent.ipynb` – Haupt-Notebook mit Training, Visualisierung & Evaluation
- `notebook/trained_dqn.pt` – gespeichertes Modell nach Training
- `requirements.txt` – benötigte Python-Pakete
- `PyGame-Learning-Environment/` – eingebundene Spielumgebung (PLE)

---

## 🚀 Setup & Ausführung

1. Virtuelle Umgebung erstellen:

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

```

2. Notebook starten:

```bash
jupyter notebook notebook/flappy_agent.ipynb
```

---

## 🧠 RL-Architektur

- **Deep Q-Network (DQN)** mit:
  - Feedforward-Netz (256-128)
  - Replay Buffer
  - ε-greedy Exploration
  - Reward Shaping
  - Target Network
  - (optional getestet: Double DQN)

---

## 📊 Ergebnisse

- Der Agent wurde über 500 Episoden trainiert und zeigte in einzelnen Durchläufen deutliche Fortschritte.
- In einem Lauf wurde ein Total Reward von über 15 erreicht, in anderen deutlich geringere Werte.
- Zur Bewertung der Reproduzierbarkeit wurden mehrere Trainings mit unterschiedlichen Seeds durchgeführt.
- Eine anschließende Testepisode ohne Exploration (greedy Policy) zeigte punktuell gelerntes Verhalten, jedoch keine robuste Steuerungsstrategie.

---

## 🎬 Demo (Modell Flappy Bird spielen lassen)

Das Notebook enthält eine Testfunktion, in der der geladene Agent deterministisch spielt. Die beobachtete Performance variiert stark zwischen einzelnen Läufen, was auf die hohe Varianz der Lernumgebung hinweist.

---

## 📚 Verwendete Quellen

- Mnih et al. (2013): Playing Atari with Deep Reinforcement Learning
- Van Hasselt et al. (2016): Deep Reinforcement Learning with Double Q-learning
- PyGame Learning Environment (PLE): https://github.com/ntasfi/PyGame-Learning-Environment
