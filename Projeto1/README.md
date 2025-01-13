# Relatório de Performance dos Algoritmos de Classificação 🔖

## Introdução 📊
Na Aula 6 da disciplina, foram exploradas as técnicas de **Classificação Automática de Textos** ✍️, uma das tarefas mais comuns na área de **Processamento de Linguagem Natural** (PLN) 🤖. Esta atividade teve como objetivo implementar abordagens tradicionais de **Aprendizado de Máquina** 🧪 e **Modelos Neurais de Linguagens** 🧠 para classificação automática de decisões judiciais escritas em português do Brasil.

Utilizamos a base de dados disponibilizada no Hugging Face 🔍:
[https://huggingface.co/datasets/joelniklaus/brazilian_court_decisions](https://huggingface.co/datasets/joelniklaus/brazilian_court_decisions).

O objetivo do projeto foi **estender os códigos desenvolvidos em sala de aula** para incorporar novos algoritmos e configurações, permitindo a avaliação de desempenho comparativo.

---

## Resultados 📊

### Tabela 1 - Resultados com Algoritmos de Aprendizado de Máquina 🎮
Os resultados apresentados na Tabela 1 correspondem aos experimentos realizados utilizando abordagens baseadas na medida **TF-IDF**. O melhor resultado em cada métrica está destacado em **negrito**.

<table>
  <tr>
    <th>Classificador</th>
    <th>Acurácia</th>
    <th>Precisão</th>
    <th>Recall</th>
    <th>F1-Score</th>
  </tr>
  <tr>
    <td>Logistic Regression</td>
    <td>70.864</td>
    <td>72.817</td>
    <td>70.864</td>
    <td>71.479</td>
  </tr>
  <tr>
    <td>Multinomial NB</td>
    <td>61.481</td>
    <td>52.165</td>
    <td>61.481</td>
    <td>51.091</td>
  </tr>
  <tr>
    <td>KNN</td>
    <td>66.420</td>
    <td>65.006</td>
    <td>66.420</td>
    <td>64.867</td>
  </tr>
  <tr>
    <td>SVM</td>
    <td>70.123</td>
    <td>73.405</td>
    <td>70.123</td>
    <td>66.452</td>
  </tr>
  <tr>
    <td>Random Forest</td>
    <td>72.099</td>
    <td>73.616</td>
    <td>72.099</td>
    <td>69.206</td>
  </tr>
  <tr>
    <td>XGBoost</td>
    <td><b>74.815</b></td>
    <td><b>74.086</b></td>
    <td><b>74.815</b></td>
    <td><b>73.732</b></td>
  </tr>
  <tr>
    <td>Decision Tree</td>
    <td>69.630</td>
    <td>68.828</td>
    <td>69.630</td>
    <td>69.079</td>
  </tr>
  <tr>
    <td>Quadratic Discriminant</td>
    <td>23.704</td>
    <td>65.074</td>
    <td>23.704</td>
    <td>19.645</td>
  </tr>
  <tr>
    <td>Passive Aggressive</td>
    <td>74.074</td>
    <td>73.566</td>
    <td>74.074</td>
    <td>73.766</td>
  </tr>
  <tr>
    <td>MLP Classifier</td>
    <td>73.333</td>
    <td>72.636</td>
    <td>73.333</td>
    <td>72.825</td>
  </tr>
</table>

🔹 O **XGBoost** apresentou os melhores resultados em todas as métricas, tornando-se o modelo mais eficiente na abordagem baseada em TF-IDF.

---

### Tabela 2 - Resultados do Modelo Binary 🎯
Esta tabela avalia o desempenho dos modelos aplicados ao conjunto de dados no formato binário. Os melhores resultados em cada métrica estão destacados em **negrito**.

<table>
  <tr>
    <th>Classificador</th>
    <th>Acurácia</th>
    <th>Precisão</th>
    <th>Recall</th>
    <th>F1-Score</th>
  </tr>
  <tr>
    <td>Logistic Regression</td>
    <td>74.074</td>
    <td>73.862</td>
    <td>74.074</td>
    <td>73.936</td>
  </tr>
  <tr>
    <td>Multinomial NB</td>
    <td>62.222</td>
    <td>65.468</td>
    <td>62.222</td>
    <td>63.162</td>
  </tr>
  <tr>
    <td>KNN</td>
    <td>67.160</td>
    <td>66.994</td>
    <td>67.160</td>
    <td>64.539</td>
  </tr>
  <tr>
    <td>SVM</td>
    <td>73.086</td>
    <td>74.454</td>
    <td>73.086</td>
    <td>70.501</td>
  </tr>
  <tr>
    <td>Random Forest</td>
    <td>73.333</td>
    <td>75.763</td>
    <td>73.333</td>
    <td>70.534</td>
  </tr>
  <tr>
    <td>XGBoost</td>
    <td><b>76.543</b></td>
    <td><b>75.849</b></td>
    <td><b>76.543</b></td>
    <td><b>75.602</b></td>
  </tr>
  <tr>
    <td>Decision Tree</td>
    <td>66.667</td>
    <td>66.115</td>
    <td>66.667</td>
    <td>66.343</td>
  </tr>
  <tr>
    <td>Quadratic Discriminant</td>
    <td>27.407</td>
    <td>61.290</td>
    <td>27.407</td>
    <td>23.712</td>
  </tr>
  <tr>
    <td>Passive Aggressive</td>
    <td>72.840</td>
    <td>72.158</td>
    <td>72.840</td>
    <td>72.335</td>
  </tr>
  <tr>
    <td>MLP Classifier</td>
    <td>73.333</td>
    <td>72.159</td>
    <td>73.333</td>
    <td>72.431</td>
  </tr>
</table>

🔹 O **XGBoost** novamente apresentou a melhor performance em todas as métricas, sendo o mais indicado para dados binários.

---

### Tabela 3 - Resultados para Modelos Legais ⚖️
Os modelos especializados em linguagem jurídica foram avaliados com os resultados destacados abaixo.

<table>
  <tr>
    <th>Modelos</th>
    <th>Épocas</th>
    <th>Acurácia</th>
    <th>Precisão</th>
    <th>Recall</th>
    <th>F1-Score</th>
  </tr>
  <tr>
    <td rowspan="3">Legal-BERTimbau-base</td>
    <td>1</td>
    <td>73.333</td>
    <td>72.608</td>
    <td>73.333</td>
    <td>72.062</td>
  </tr>
  <tr>
    <td>3</td>
    <td>77.284</td>
    <td>76.766</td>
    <td>77.284</td>
    <td>76.859</td>
  </tr>
  <tr>
    <td>5</td>
    <td>76.543</td>
    <td>76.000</td>
    <td>76.543</td>
    <td>76.029</td>
  </tr>
  <tr>
    <td rowspan="3">BERTimbau-base</td>
    <td>1</td>
    <td>72.840</td>
    <td>71.870</td>
    <td>72.840</td>
    <td>71.607</td>
  </tr>
  <tr>
    <td>3</td>
    <td>73.580</td>
    <td>72.428</td>
    <td>73.580</td>
    <td>72.273</td>
  </tr>
  <tr>
    <td>5</td>
    <td>74.321</td>
    <td>73.955</td>
    <td>74.321</td>
    <td>74.078</td>
  </tr>
  <tr>
    <td rowspan="3">Legal_BERT_pt</td>
    <td>1</td>
    <td>73.086</td>
    <td>72.340</td>
    <td>73.086</td>
    <td>71.742</td>
  </tr>
  <tr>
    <td>3</td>
    <td>78.519</td>
    <td>78.072</td>
    <td>78.519</td>
    <td>77.794</td>
  </tr>
  <tr>
    <td>5</td>
    <td><b>78.519</b></td>
    <td><b>78.072</b></td>
    <td><b>78.519</b></td>
    <td><b>77.947</b></td>
  </tr>
</table>

🔹 O **Legal_BERT_pt** obteve os melhores resultados entre os modelos especializados, especialmente nas métricas de **Acurácia**, **Precisão**, **Recall** e **F1-Score** após 5 épocas.

---

### Tabela 4 - Resultados no Formato Count 📊
A Tabela 4 avalia o desempenho dos classificadores utilizando dados no formato **Count**. Os melhores resultados em cada métrica estão destacados em **negrito**.

<table>
  <tr>
    <th>Classificador</th>
    <th>Acurácia</th>
    <th>Precisão</th>
    <th>Recall</th>
    <th>F1-Score</th>
  </tr>
  <tr>
    <td>Logistic Regression</td>
    <td>74.321</td>
    <td>74.634</td>
    <td>74.321</td>
    <td>74.457</td>
  </tr>
  <tr>
    <td>Multinomial NB</td>
    <td>60.247</td>
    <td>64.622</td>
    <td>60.247</td>
    <td>61.294</td>
  </tr>
  <tr>
    <td>KNN</td>
    <td>62.963</td>
    <td>60.688</td>
    <td>62.963</td>
    <td>60.237</td>
  </tr>
  <tr>
    <td>SVM</td>
    <td>69.383</td>
    <td>70.862</td>
    <td>69.383</td>
    <td>66.083</td>
  </tr>
  <tr>
    <td>Random Forest</td>
    <td>73.580</td>
    <td>74.948</td>
    <td>73.580</td>
    <td>71.227</td>
  </tr>
  <tr>
    <td>XGBoost</td>
    <td><b>77.037</b></td>
    <td><b>76.492</b></td>
    <td><b>77.037</b></td>
    <td><b>76.082</b></td>
  </tr>
  <tr>
    <td>Decision Tree</td>
    <td>66.914</td>
    <td>66.519</td>
    <td>66.914</td>
    <td>66.696</td>
  </tr>
  <tr>
    <td>Quadratic Discriminant</td>
    <td>37.778</td>
    <td>53.879</td>
    <td>37.778</td>
    <td>38.372</td>
  </tr>
  <tr>
    <td>Passive Aggressive</td>
    <td>73.333</td>
    <td>72.629</td>
    <td>73.333</td>
    <td>72.780</td>
  </tr>
  <tr>
    <td>MLP Classifier</td>
    <td>75.309</td>
    <td>74.606</td>
    <td>75.309</td>
    <td>74.739</td>
  </tr>
</table>

🔹 O **XGBoost** novamente destacou-se como o melhor modelo neste cenário, apresentando as maiores métricas em **Acurácia**, **Precisão**, **Recall** e **F1-Score**.

---

## Conclusão 🎯

Os resultados apresentados demonstram que:

- O **XGBoost** destacou-se consistentemente para abordagens tradicionais de aprendizado de máquina.
- Os modelos de linguagem pré-treinados, especialmente o **Legal_BERT_pt**, são mais indicados para contextos jurídicos, mostrando superioridade em tarefas de classificação de textos legais.

Recomenda-se a utilização dos modelos baseados em redes neurais para tarefas que envolvam linguagem especializada e contextos jurídicos.
