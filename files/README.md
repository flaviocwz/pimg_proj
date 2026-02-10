# Segmentação de Bombons em Imagens Digitais

**Autores:** Matheus de Souza Matos e Flavio Henrique de Jesus Cruz  
**Disciplina:** Processamento de Imagens — Universidade Federal de Sergipe  

---

## Descrição

Segmentação automática de bombons em imagens digitais utilizando técnicas clássicas de processamento de imagens. O objetivo é identificar, separar e contar os bombons presentes em uma cena, sem uso de aprendizado de máquina.

**Dataset:** [Valentines Chocolates — Roboflow](https://universe.roboflow.com/chocolates/valentines-chocolates/)

---

## Estrutura do Repositório

```
segmentacao-bombons/
│
├── README.md                       # Este arquivo
├── segmentacao_bombons.ipynb       # Notebook com toda a solução
├── requirements.txt                # Dependências
│
└── imagens/
    └── thumb.jpg                   # Imagem utilizada nos experimentos
```

---

## Metodologia

O pipeline de processamento segue as etapas abaixo:

```
Imagem RGB
    → Escala de cinza
    → Histograma + Binarização (Otsu)
    → Abertura morfológica  (remove ruídos)
    → Fechamento morfológico (preenche buracos)
    → Rotulação de componentes conexos
    → Contagem e análise dos bombons
```

**Elemento estruturante:** disco circular de raio 3 px

---

## Como Executar

```bash
# 1. Instalar dependências
pip install -r requirements.txt

# 2. Abrir o notebook
jupyter notebook segmentacao_bombons.ipynb
```

---

## Bibliotecas Utilizadas

- `numpy` — operações com arrays
- `matplotlib` — visualização
- `scikit-image` — processamento de imagens

> Não foram utilizados OpenCV, PIL como processamento, nem nenhum método de aprendizado de máquina.

---

## Resultado

![Pipeline](imagens/resultado_pipeline.png)

O método detectou corretamente os bombons isolados. Dois bombons muito próximos entre si foram fundidos em uma única região — limitação discutida na conclusão do notebook.

---

## Vídeo de Apresentação

🎥 Link: [inserir link do YouTube]

---

*Trabalho Final — Processamento de Imagens — UFS — Fevereiro 2026*
