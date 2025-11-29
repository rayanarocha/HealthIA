# 🧠 HealthIA

Aplicação de Machine Learning para diagnóstico de doenças.

## 🚀 Visão Geral  
O **HealthIA** é uma aplicação desenvolvida como parte do desafio MasterTech “Grandes Temas”, cujo objetivo é utilizar técnicas de **Machine Learning** e **NLP** para diagnosticar doenças com base em dados textuais ou vetorizados.  
A aplicação combina:
- Vetorização textual via **TF-IDF**
- Classificação usando **XGBoost**
- Exposição do modelo via **FastAPI**

---

## 🧰 Tecnologias Utilizadas  
- **Python**
- **TF-IDF** (Term Frequency – Inverse Document Frequency)  
- **XGBoost**  
- **FastAPI**

Estrutura modular:
```
model/      → artefatos e modelos treinados  
api/        → rotas FastAPI  
services/   → pré-processamento e utilitários  
main.py     → entrada da API  
leitura.py  → leitura e preparação dos dados  
```

---

## ✅ Funcionalidades  
✔ Receber textos/sintomas como entrada  
✔ Vetorização usando TF-IDF  
✔ Predição usando modelo XGBoost  
✔ API REST para consulta  
✔ Processamento estruturado via serviços internos  

---

## 🎯 Motivação  
Este projeto demonstra como **IA e NLP** podem apoiar diagnósticos médicos ao transformar dados brutos em previsões automatizadas.  
É útil como protótipo de:
- sistemas de triagem automatizada  
- apoio à decisão clínica  
- soluções de análise de sintomas  
- estudos acadêmicos de aplicações de IA na área da saúde  

---

## 🛠️ Como Rodar o Projeto Localmente  

### 1. Criar ambiente virtual (opcional, mas recomendado)
```bash
python -m venv venv
```

Ativar:

**Linux/macOS**
```bash
source venv/bin/activate
```

**Windows**
```bash
venv\Scripts\activate
```

---

### 2. Instalar dependências
```bash
pip install -r requirements.txt
```

---

### 3. Utilizar o modelo treinado  
O modelo já está disponível em **model/**.  
(Se houver script de treino, basta executá-lo.)

---

### 4. Rodar a API  
```bash
uvicorn main:app
```

---

### 5. Acessar a API  
Documentação automática do FastAPI:  
👉 **http://127.0.0.1:8000/docs**

---

## 🔧 Exemplo de Uso

### Request  
```
POST /predict
```

Entrada (texto puro):
```
sede constante, micção frequente, perda de peso rápida
```

### Resposta esperada (JSON)
```json
{
  "sintomas": [
    "sede constante",
    "micção frequente",
    "perda de peso rápida"
  ],
  "diagnostico_previsto": [
    "diabetes_tipo1"
  ]
}
```

---

## 📂 Estrutura de Pastas  
```plaintext
HealthIA/
├── api/         # API FastAPI
├── model/       # Modelo de ML treinado / artefatos
├── services/    # Pré-processamento, utilitários, vetorização
├── main.py      # Ponto de entrada
├── leitura.py   # Leitura / pré-processamento de dados
└── README.md    # Documentação do projeto
```

---

## 🤝 Contribuição  
Contribuições são bem-vindas!  
1. Abra uma issue descrevendo a melhoria ou bug  
2. Crie um branch com nome descritivo  
3. Envie o PR com suas alterações  

---

## 👤 Autor  
Criado por **rayanarocha**  
🔗 GitHub: https://github.com/rayanarocha
