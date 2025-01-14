# Processamento de Linguagem Natural 🌐

**Prof. Dr. Hilário Thomaz Alves de Oliveira**  
**Pós-graduação em Desenvolvimento de Aplicações Inteligentes**  
**Processamento de Linguagem Natural — Projeto 01 - Classificação de Decisões Judiciais**  

**Nome:** Otávio Lube dos Santos  
**Matrícula:**cdo  

## Especificação do Trabalho 📝

1. **Tarefa 2:**  
   - Estudar a tarefa de **Reconhecimento de Entidades Nomeadas (REN)**, explorada na Aula 7. 📚
   - Objetivo: Identificar menções de **entidades de interesse** em textos, com foco em documentos jurídicos escritos em português do Brasil. ⚖️
   - Implementar abordagens usando **Redes Neurais Profundas**. 🤖

2. **Bases de Dados Utilizadas:**  
   - LE-NER: [Disponível no GitHub](https://github.com/messias077/ner_pt/tree/main/data/corpora/le_ner)  
   - Lener_br: [Disponível no Hugging Face](https://huggingface.co/datasets/lener_br)  
   - Ulysses-ner-br: [Disponível no GitHub](https://github.com/ulysses-camara/ulysses-ner-br/tree/main/annotated-corpora/PL_corpus_conll/pl_corpus_categorias)

3. **Objetivo do Projeto:**  
   Estender os códigos desenvolvidos em sala de aula para incorporar a base de dados **ulysses-ner-br** e realizar experimentos com as bases **LE-NER** e **ulysses-ner-br**. 🛠️

4. **Parâmetros e Experimentos:**  
   - Alterar os parâmetros de treinamento para:  
     - `max_iterations=100`
     - `all_possible_transitions=True`
   - Executar os experimentos e gerar resultados para ambas as bases de dados. ⚙️

5. **Entrega e Resultados:**  
   - Montar uma planilha com os resultados dos experimentos. 📊
   - Gerar uma tabela para cada tarefa (Classificação e REN).  
   - Compartilhar a planilha e os códigos no GitHub. 🖥️
   - Enviar o link por e-mail para: **hilariotomaz@gmail.com**.  
   - **Data de Entrega:** 13/12/2023. 📆

6. **Resultados da Base LE-NER:**

<div style="overflow-x:auto;">
<table>
  <thead>
    <tr>
      <th>Entidade</th>
      <th>Precisão (P)</th>
      <th>Cobertura (R)</th>
      <th>F1-Score</th>
      <th>Suporte</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>DATA</td>
      <td>0.96</td>
      <td>0.92</td>
      <td style="font-weight:bold; color:green;">0.94</td>
      <td>98</td>
    </tr>
    <tr>
      <td>EVENTO</td>
      <td style="font-weight:bold; color:green;">1.00</td>
      <td>0.22</td>
      <td>0.36</td>
      <td>9</td>
    </tr>
    <tr>
      <td>FUNDAMENTO</td>
      <td>0.82</td>
      <td style="font-weight:bold; color:green;">0.83</td>
      <td>0.82</td>
      <td>124</td>
    </tr>
    <tr>
      <td>LOCAL</td>
      <td>0.75</td>
      <td>0.72</td>
      <td>0.74</td>
      <td>101</td>
    </tr>
    <tr>
      <td>ORGANIZACAO</td>
      <td>0.76</td>
      <td>0.69</td>
      <td>0.72</td>
      <td>94</td>
    </tr>
    <tr>
      <td>PESSOA</td>
      <td>0.90</td>
      <td>0.78</td>
      <td>0.84</td>
      <td>119</td>
    </tr>
    <tr>
      <td>PRODUTOLEI</td>
      <td>0.69</td>
      <td>0.67</td>
      <td>0.68</td>
      <td>54</td>
    </tr>
    <tr>
      <td><strong>Micro Avg</strong></td>
      <td>0.82</td>
      <td>0.77</td>
      <td>0.80</td>
      <td>599</td>
    </tr>
    <tr>
      <td><strong>Macro Avg</strong></td>
      <td style="font-weight:bold; color:green;">0.84</td>
      <td>0.69</td>
      <td>0.73</td>
      <td>599</td>
    </tr>
    <tr>
      <td><strong>Weighted Avg</strong></td>
      <td>0.83</td>
      <td style="font-weight:bold; color:green;">0.77</td>
      <td>0.79</td>
      <td>599</td>
    </tr>
  </tbody>
</table>
</div>

### Interpretação dos Resultados 🌟
- A categoria **DATA** apresentou excelente desempenho com F1-Score de 0.94, indicando alta precisão e cobertura.
- **EVENTO** teve baixa cobertura (0.22), o que sugere que poucos exemplos foram identificados corretamente.
- **FUNDAMENTO** e **LOCAL** tiveram F1-Scores equilibrados, indicando desempenho consistente.
- **PESSOA** destacou-se com F1-Score de 0.84, mostrando bom equilíbrio entre precisão e cobertura.
- **PRODUTOLEI** apresentou menor desempenho geral, com F1-Score de 0.68.
- As médias mostram que o modelo tem desempenho geral razoável, mas pode ser melhorado em categorias com baixa cobertura como **EVENTO**.

6. **Resultados da Base Ulysses-NER:**

<div style="overflow-x:auto;">
<table>
  <thead>
    <tr>
      <th>Entidade</th>
      <th>Precisão (P)</th>
      <th>Cobertura (R)</th>
      <th>F1-Score</th>
      <th>Suporte</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>DATA</td>
      <td>0.96</td>
      <td>0.92</td>
      <td style="font-weight:bold; color:green;">0.94</td>
      <td>98</td>
    </tr>
    <tr>
      <td>EVENTO</td>
      <td style="font-weight:bold; color:green;">1.00</td>
      <td>0.22</td>
      <td>0.36</td>
      <td>9</td>
    </tr>
    <tr>
      <td>FUNDAMENTO</td>
      <td>0.82</td>
      <td style="font-weight:bold; color:green;">0.83</td>
      <td>0.82</td>
      <td>124</td>
    </tr>
    <tr>
      <td>LOCAL</td>
      <td>0.75</td>
      <td>0.72</td>
      <td>0.74</td>
      <td>101</td>
    </tr>
    <tr>
      <td>ORGANIZACAO</td>
      <td>0.76</td>
      <td>0.69</td>
      <td>0.72</td>
      <td>94</td>
    </tr>
    <tr>
      <td>PESSOA</td>
      <td>0.90</td>
      <td>0.78</td>
      <td>0.84</td>
      <td>119</td>
    </tr>
    <tr>
      <td>PRODUTOLEI</td>
      <td>0.69</td>
      <td>0.67</td>
      <td>0.68</td>
      <td>54</td>
    </tr>
    <tr>
      <td><strong>Micro Avg</strong></td>
      <td>0.82</td>
      <td>0.77</td>
      <td>0.80</td>
      <td>599</td>
    </tr>
    <tr>
      <td><strong>Macro Avg</strong></td>
      <td style="font-weight:bold; color:green;">0.84</td>
      <td>0.69</td>
      <td>0.73</td>
      <td>599</td>
    </tr>
    <tr>
      <td><strong>Weighted Avg</strong></td>
      <td>0.83</td>
      <td style="font-weight:bold; color:green;">0.77</td>
      <td>0.79</td>
      <td>599</td>
    </tr>
  </tbody>
</table>
</div>

### Interpretação dos Resultados 🌟
- A categoria **DATA** apresentou excelente desempenho com F1-Score de 0.94, indicando alta precisão e cobertura.
- **EVENTO** teve baixa cobertura (0.22), o que sugere que poucos exemplos foram identificados corretamente.
- **FUNDAMENTO** e **LOCAL** tiveram F1-Scores equilibrados, indicando desempenho consistente.
- **PESSOA** destacou-se com F1-Score de 0.84, mostrando bom equilíbrio entre precisão e cobertura.
- **PRODUTOLEI** apresentou menor desempenho geral, com F1-Score de 0.68.
- As médias mostram que o modelo tem desempenho geral razoável, mas pode ser melhorado em categorias com baixa cobertura como **EVENTO**.
