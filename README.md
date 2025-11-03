
# 🎮 GUESS THE CHARACTER – AI Game  
*A machine learning–powered Akinator for Marvel & DC heroes*  




## 🧠 Overview  

**Guess the Character** is an interactive AI guessing game that tries to identify which **superhero or character** you’re thinking of — from **64 Marvel & DC heroes** — by asking a short series of yes/no questions.  

The project uses **Decision Tree models** trained on a structured dataset of hero traits (powers, gadgets, origins, etc.) to make logical guesses — just like **Akinator**, but custom-built and open-source.

---

## ⚙️ Features  

✅ Machine learning–based hero prediction  
✅ 7-question & 14-question model modes  
✅ Trait importance calculated via **Information Gain**  
✅ Trained with scikit-learn Decision Trees  
✅ Optional **Flask web interface**  
✅ Expandable dataset (add more heroes easily)

---

## 📊 Model Training Summary  

| Model | Questions | Train Accuracy | Test Accuracy | Cross-Validation |
|:------|:-----------:|:---------------:|:---------------:|:----------------:|
| **Decision Tree** | 7 | 34.09% | 34.09% | 34.09% ±3.21% |
| **Decision Tree** | 14 | **83.33%** | **83.33%** | **83.33% ±1.63%** |
| Random Forest | 14 | 83.33% | 83.33% | 81.82% ±0.46% |
| Gradient Boosting | 14 | 83.33% | 83.33% | 81.44% ±0.54% |
| AdaBoost | – | ❌ Poor performance | – | – |

📁 **Best Model:** Decision Tree (14 Questions)  
📂 **Saved Models:** `guess_game_models_enhanced/`

---

## 🧩 Dataset Features  

Each hero is represented by 20+ binary or categorical attributes, e.g.:  

- `superhero`, `uses_gadgets`, `flies`, `super_strength`  
- `team_member`, `detective`, `leader`, `scientist`, `immortal`  
- `genre_Marvel`, `genre_DC`, `alien_origin`, `tech_genius`  

### 🔝 Top Informative Features (Information Gain)
| Rank | Feature | IG |
|------|----------|----|
| 1 | uses_gadgets | 0.9993 |
| 2 | team_member | 0.9993 |
| 3 | enhanced_senses | 0.9985 |
| 4 | super_strength | 0.9973 |
| 5 | super_agility | 0.9973 |

---

## 🧮 How It Works  

1. The game starts by asking a set of yes/no questions.  
2. Each question corresponds to one feature from the dataset.  
3. The trained **Decision Tree model** uses your responses to narrow down possibilities.  
4. After 7 or 14 questions, it predicts which hero you’re thinking of.  

---

## 🕹️ Gameplay Example  

```bash
======================================================================
           🎮 GUESS THE CHARACTER GAME 🎮
              64 Marvel & DC Heroes
======================================================================

Q1: Does your character use gadgets? (yes/no): yes  
Q2: Is your character part of a team? (yes/no): yes  
Q3: Does your character have super strength? (yes/no): no  
...

🤖 AI Guess: Batman 🦇  
Confidence: 92%
````

---

## 📁 Project Structure

```
📦 guess_the_character/
 ┣ 📂 data/
 ┃ ┗ characters_dataset.csv
 ┣ 📂 guess_game_models_enhanced/
 ┃ ┣ decision_tree_7Q.pkl
 ┃ ┗ decision_tree_14Q.pkl
 ┣ 📂 static/
 ┃ ┗ assets/ (images, favicon, etc.)
 ┣ 📂 templates/
 ┃ ┗ index.html
 ┣ train_models.py
 ┣ game.py
 ┣ app.py
 ┗ README.md
```

---

## 🚀 Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/guess-the-character.git
cd guess-the-character
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the console version

```bash
python game.py
```

### 4️⃣ (Optional) Run the Flask web app

```bash
python app.py
```

Then open your browser at `http://127.0.0.1:5000/`

---

## 🧠 Tech Stack

* **Python 3.10+**
* **scikit-learn** – ML models (Decision Tree, Random Forest, etc.)
* **pandas / numpy** – data preprocessing
* **Flask** – web app interface
* **joblib** – model serialization

---

## 🧭 Future Improvements

* 🌐 Add online playable version
* 🧩 Expand dataset (MCU Phase 4, DCEU, anime, real-world celebs)
* 🧠 Adaptive question selection (entropy-based)
* 🖼️ Image UI with animations and hero cards
* 🔁 User feedback loop for retraining

---

## 👨‍💻 Author

**Developed by:** Dhruvil Patel
**Language:** Python
**Dataset:** Custom Marvel + DC dataset (64 heroes)
**Model Type:** Decision Tree Classifier

📫 *Feel free to fork, star ⭐, and contribute!*

---

## 📜 License

This project is released under the **MIT License** – free to use, modify, and share.

---



## 📈 Extended Model Results and Insights  

### 🧩 Top 40 Most Informative Features:
 1. uses_gadgets                   (IG: 0.9993)
 2. team_member                    (IG: 0.9993)
 3. enhanced_senses                (IG: 0.9985)
 4. super_strength                 (IG: 0.9973)
 5. super_agility                  (IG: 0.9973)
 6. genre_DC                       (IG: 0.9959)
 7. genre_Marvel                   (IG: 0.9959)
 8. energy_projection              (IG: 0.9919)
 9. tech_genius                    (IG: 0.9673)
10. wears_mask                     (IG: 0.9624)
11. uses_weapon                    (IG: 0.9624)
12. solo_hero                      (IG: 0.9624)
13. regeneration                   (IG: 0.9516)
14. superhero                      (IG: 0.9457)
15. flies                          (IG: 0.9257)
16. martial_artist                 (IG: 0.9183)
17. stealth_expert                 (IG: 0.9024)
18. leader                         (IG: 0.8454)
19. ranged_fighter                 (IG: 0.8454)
20. scientist                      (IG: 0.7990)
21. wears_armor                    (IG: 0.7864)
22. immortal                       (IG: 0.7864)
23. experiment_origin              (IG: 0.7864)
24. male                           (IG: 0.7732)
25. avenger                        (IG: 0.7732)
26. uses_magic                     (IG: 0.7596)
27. alien_origin                   (IG: 0.7596)
28. from_earth                     (IG: 0.7455)
29. anti_hero                      (IG: 0.7309)
30. justice_league                 (IG: 0.7002)
31. mystic_power_source            (IG: 0.6840)
32. tech_enhanced                  (IG: 0.6673)
33. dual_identity                  (IG: 0.6500)
34. mutant                         (IG: 0.5945)
35. telepathy                      (IG: 0.5746)
36. reformed_villain               (IG: 0.5541)
37. detective                      (IG: 0.5328)
38. trained_assassin               (IG: 0.5328)
39. military_background            (IG: 0.5108)
40. shapeshifter                   (IG: 0.4642)
Selected 7 questions for model training
Selected 15 questions for model training
Selected 20 questions for model training
Selected 25 questions for model training
Selected 30 questions for model training
Selected 35 questions for model training
Selected 40 questions for model training

======================================================================
COMPARING DIFFERENT MODELS
======================================================================


| Questions | Model             | Train (%) | Test (%) | CV Mean (%) | CV Std (±%) |
| --------- | ----------------- | --------- | -------- | ----------- | ----------- |
| **7**     | Random Forest     | 34.091    | 34.091   | 28.598      | 1.417       |
|           | Gradient Boosting | 34.091    | 34.091   | 28.409      | 1.673       |
|           | AdaBoost          | 3.788     | 3.788    | 2.462       | 0.268       |
|           | Decision Tree     | 34.091    | 34.091   | 34.091      | 3.214       |
|           | KNN               | 34.091    | 34.091   | 31.250      | 2.126       |
| **15**    | Random Forest     | 84.848    | 84.848   | 83.333      | 1.168       |
|           | Gradient Boosting | 84.848    | 84.848   | 83.144      | 0.966       |
|           | AdaBoost          | 1.515     | 1.515    | 2.083       | 0.268       |
|           | Decision Tree     | 84.848    | 84.848   | 84.848      | 1.417       |
|           | KNN               | 84.848    | 84.848   | 83.333      | 1.071       |
| **20**    | Random Forest     | 93.939    | 93.939   | 93.750      | 0.000       |
|           | Gradient Boosting | 93.939    | 93.939   | 93.750      | 0.000       |
|           | AdaBoost          | 3.030     | 3.030    | 2.462       | 1.168       |
|           | Decision Tree     | 93.939    | 93.939   | 93.939      | 0.268       |
|           | KNN               | 93.939    | 93.939   | 93.750      | 0.000       |
| **25**    | Random Forest     | 97.727    | 97.727   | 97.538      | 0.268       |
|           | Gradient Boosting | 97.727    | 97.727   | 97.538      | 0.268       |
|           | AdaBoost          | 4.545     | 4.545    | 2.652       | 0.966       |
|           | Decision Tree     | 97.727    | 97.727   | 97.727      | 0.464       |
|           | KNN               | 97.727    | 97.727   | 97.538      | 0.268       |
| **30**    | Random Forest     | 98.485    | 98.485   | 98.295      | 0.464       |
|           | Gradient Boosting | 98.485    | 98.485   | 98.295      | 0.464       |
|           | AdaBoost          | 3.030     | 3.030    | 2.273       | 0.928       |
|           | Decision Tree     | 98.485    | 98.485   | 98.485      | 0.536       |
|           | KNN               | 98.485    | 98.485   | 98.295      | 0.464       |
| **35**    | Random Forest     | 99.242    | 99.242   | 99.242      | 0.268       |
|           | Gradient Boosting | 99.242    | 99.242   | 99.242      | 0.268       |
|           | AdaBoost          | 2.273     | 2.273    | 2.273       | 0.000       |
|           | Decision Tree     | 99.242    | 99.242   | 99.242      | 0.268       |
|           | KNN               | 99.242    | 99.242   | 99.242      | 0.268       |
| **40**    | Random Forest     | 100.000   | 100.000  | 100.000     | 0.000       |
|           | Gradient Boosting | 100.000   | 100.000  | 100.000     | 0.000       |
|           | AdaBoost          | 2.273     | 2.273    | 2.652       | 1.071       |
|           | Decision Tree     | 100.000   | 100.000  | 100.000     | 0.000       |
|           | KNN               | 100.000   | 100.000  | 100.000     | 0.000       |


======================================================================
BEST MODEL FOR 7 QUESTIONS: Decision Tree
  Test Accuracy: 34.091%

======================================================================
BEST MODEL FOR 15 QUESTIONS: Decision Tree
  Test Accuracy: 84.848%

======================================================================
BEST MODEL FOR 20 QUESTIONS: Decision Tree
  Test Accuracy: 93.939%

======================================================================
BEST MODEL FOR 25 QUESTIONS: Decision Tree
  Test Accuracy: 97.727%

======================================================================
BEST MODEL FOR 30 QUESTIONS: Decision Tree
  Test Accuracy: 98.485%

======================================================================
BEST MODEL FOR 35 QUESTIONS: Random Forest
  Test Accuracy: 99.242%

======================================================================
BEST MODEL FOR 40 QUESTIONS: Random Forest
  Test Accuracy: 100.000%
======================================================================

Models and data saved to 'guess_game_models_enhanced_v2/'

✅ Training complete!
