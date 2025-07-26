# ⚽ Detecção de Jogadores, Bola e Árbitro com YOLOv5

Este projeto utiliza **YOLOv5 (versões small e medium)** e um dataset do **Roboflow** para treinar um modelo capaz de detectar:
- Jogadores (player)
- Goleiros (goalkeeper)
- Bola (ball)
- Árbitros (referee)

O objetivo é aplicar visão computacional para análise automatizada de partidas de futebol.

---

## 📁 Dataset

O dataset foi importado diretamente da plataforma **Roboflow**, contendo imagens rotuladas com 4 classes:

- `ball`
- `goalkeeper`
- `player`
- `referee`

Formato: **YOLOv5**

---

## 🔧 Estrutura do Projeto

| Etapa | Descrição |
|------|-----------|
| 1️⃣ | Instalação de dependências e importação do dataset via Roboflow |
| 2️⃣ | Clone do repositório oficial YOLOv5 |
| 3️⃣ | Ajuste do arquivo `data.yaml` com os caminhos corretos |
| 4️⃣ | Treinamento inicial com YOLOv5‑S (modelo pequeno) |
| 5️⃣ | Treinamento com YOLOv5‑M (modelo médio) |

---

## 📈 Resultados Obtidos


### 🔹 YOLOv5s (Modelo Pequeno)
| Classe       | Precision (P) | Recall (R) | mAP@0.5 | mAP@0.5:0.95 |
|--------------|----------------|------------|---------|---------------|
| Ball         | 0.827          | 0.280      | 0.359   | 0.137         |
| Goalkeeper   | 0.766          | 0.649      | 0.800   | 0.543         |
| Player       | 0.912          | 0.959      | 0.977   | 0.771         |
| Referee      | 0.646          | 0.667      | 0.727   | 0.514         |
| **Média (All)** | **0.788**    | **0.639**  | **0.716** | **0.491**     |

---

### 🔸 YOLOv5m (Modelo Médio)
| Classe       | Precision (P) | Recall (R) | mAP@0.5 | mAP@0.5:0.95 |
|--------------|----------------|------------|---------|---------------|
| Ball         | 0.947          | 0.561      | 0.629   | 0.310         |
| Goalkeeper   | 0.922          | 0.976      | 0.982   | 0.791         |
| Player       | 0.965          | 0.971      | 0.988   | 0.851         |
| Referee      | 0.918          | 0.918      | 0.957   | 0.762         |
| **Média (All)** | **0.938**    | **0.857**  | **0.889** | **0.678**     |

---

## ✅ Comparativo entre YOLOv5s vs YOLOv5m

| Métrica        | YOLOv5s | YOLOv5m |
|----------------|---------|---------|
| Precision média | 0.788   | 0.938   |
| Recall médio    | 0.639   | 0.857   |
| mAP@0.5         | 0.716   | 0.889   |
| mAP@0.5:0.95    | 0.491   | 0.678   |

📌 O modelo **YOLOv5m** apresenta melhorias substanciais, principalmente na detecção da **bola** e **árbitros**, que são mais difíceis por serem menores ou menos frequentes.

---

## 🧠 Tecnologias Utilizadas

- [YOLOv5 – Ultralytics](https://github.com/ultralytics/yolov5)
- [Roboflow](https://roboflow.com/)
- Google Colab
- Python 3

---

