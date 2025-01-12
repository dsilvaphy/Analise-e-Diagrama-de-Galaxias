# 🌌 Análise e Diagrama de Galáxias

Este repositório contém um script em Python e um arquivo de dados para análise e visualização de galáxias observadas pelo projeto **SDSS (Sloan Digital Sky Survey)**. O objetivo principal é gerar um **Diagrama de Cor em Função do Brilho Intrínseco**, classificando galáxias como espirais ou elípticas.

---

## 📂 Estrutura do Repositório

- **`diagrama_galáxias.ipynb`**: Jupyter Notebook com a análise completa, desde a importação dos dados até a visualização final.
- **`galaxias.txt`**: Arquivo de dados contendo as propriedades das galáxias observadas.
  
---

## 🪐 Dados das Galáxias

O arquivo `galaxias.txt` contém uma tabela com 18.525 galáxias e as seguintes colunas:

1. **`Mg`**: Magnitude absoluta na banda g.
2. **`Mr`**: Magnitude absoluta na banda r.
3. **`mr`**: Magnitude aparente na banda r.
4. **`z`**: Redshift (desvio para o vermelho).
5. **`CI`**: Índice de concentração na banda r.

Cada linha do arquivo representa uma galáxia, e essas informações são usadas para calcular propriedades como:
- Magnitude aparente.
- Diagrama de cor `(Mg - Mr)`.

---

## 🔍 Análise Realizada

1. **Importação e Processamento dos Dados**:
   - O arquivo `galaxias.txt` é lido e os dados são organizados em arrays para manipulação.

2. **Seleção de Amostras**:
   - Filtro aplicado para selecionar galáxias próximas e brilhantes com:
     - `z < 0.1`
     - `mr < 17`

3. **Cálculo da Magnitude Aparente**:
   - Fórmula utilizada:
     \[
     m_v = -2.5 \log(F_v) + C
     \]
   - Onde `C` é uma constante ajustável.

4. **Classificação das Galáxias**:
   - **Espirais**: `CI < 2.5`
   - **Elípticas**: `CI > 2.5`

5. **Visualização**:
   - Geração de dois gráficos principais:
     - **Diagrama de Cor em Função do Brilho Intrínseco**.
     - **Scatterplot das Galáxias Espirais vs Elípticas**.

---

## 📊 Resultado
 <div align="center">
    <img src="https://github.com/dsilvaphy/Analise-e-Diagrama-de-Galaxias/blob/main/diagramafinal.png" alt="printmapas" width="550" height="460">
 </div>

---

## 💻 Como Utilizar

1. **Pré-requisitos**:
   - Python 3.x
   - Jupyter Notebook
   - Bibliotecas: `numpy`, `matplotlib`

2. **Execução**:
   - Clone este repositório:
     ```bash
     git clone https://github.com/seu-usuario/diagrama-galaxias.git
     ```
   - Abra o arquivo Jupyter Notebook:
     ```bash
     jupyter notebook diagrama_galáxias.ipynb
     ```
   - Siga as células para executar a análise e visualizar os gráficos.

---

## 📖 Referência

Os dados foram obtidos do **Sloan Digital Sky Survey (SDSS)**, um dos maiores projetos de levantamento astronômico.

---

## 📜 Licença

📄 Este projeto está sob a licença MIT. Sinta-se à vontade para utilizar e modificar, exceto para fins comerciais.

Veja a licença completa [CC BY-NC 4.0](/creativecommons.org/licenses/by-nc/4.0/deed.pt-br).

---

Com este script e conjunto de dados, você pode explorar as propriedades físicas e visuais das galáxias de maneira prática e científica. ✨
