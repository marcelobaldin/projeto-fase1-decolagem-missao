# Projeto Fase I - Decolagem da Missão

## FIAP - Ciências da Computação

**Aluno:** Marcelo Bastianello Baldin
**RM:** 568746
**Disciplina:** Atividade Integradora - Fase I

---

## Descrição do Projeto

Este projeto faz parte da Atividade Integradora da Fase I (Decolagem da Missão) do curso de Ciências da Computação da FIAP. O objetivo é simular um sistema de verificação pré-decolagem de uma missão espacial, integrando conceitos de:

- **Computação**: lógica de programação, algoritmos de verificação, Python
- **Eficiência Energética**: cálculos de autonomia, perdas energéticas, rendimento
- **Inteligência Artificial**: classificação de dados, detecção de anomalias, validação por IA generativa
- **Sustentabilidade**: reflexão sobre ética, impacto social, governança espacial e tecnologia verde

## Estrutura do Projeto

```
projeto_fase_I/
├── projeto_decolagem.ipynb                        # Notebook principal com todo o código e análises
├── projeto_decolagem.html                         # Exportação HTML do notebook
├── Relatorio_Projeto_Fase_I_Decolagem_Missao.pdf  # Relatório PDF completo (38 páginas)
├── fluxograma_verificacao.png                     # Fluxograma gerado com Graphviz
├── gerar_pdf.py                                   # Script de geração do PDF
├── insumos/                                       # Material de referência (PDFs, artigos)
├── Captura de Tela *.png                          # 18 screenshots da execução no Google Colab
└── README.md                                      # Este arquivo
```

## Funcionalidades

### 1.1 Organização da Telemetria
- Definição dos dados de sensores: temperatura, pressão, energia, integridade, módulos
- Apresentação em formato tabular com indicadores de status
- Definição de faixas seguras para cada parâmetro

### 1.2 Algoritmo de Verificação
- Pseudocódigo estruturado do algoritmo de decisão
- Fluxograma profissional gerado com **Graphviz** (diagrama colorido com legenda)
- Lógica de decisão: "PRONTO PARA DECOLAR" ou "DECOLAGEM ABORTADA"

### 1.3 Script Python
- Função `verificar_decolagem()` que realiza todas as verificações
- Teste com cenário normal: tabela comparativa com valores, faixas seguras e status
- Teste com cenário de anomalias: parâmetros fora da faixa e módulos em falha

### 1.4 Análise Energética
- Cálculo de energia disponível com base na capacidade e carga atual
- Cálculo de perdas energéticas (dissipação térmica / entropia)
- Cálculo de autonomia pós-decolagem em horas e dias
- Cálculo de rendimento global (η)
- Referência aos conceitos do Cap. 7 (2ª Lei da Termodinâmica, P = I² × R)

### 1.5 Análise Assistida por IA
- Classificação dos parâmetros em NORMAL / ATENÇÃO / CRÍTICO
- Identificação automática de anomalias
- Sugestões de risco baseadas na análise dos dados
- Análise de correlação entre parâmetros

### 1.5.1 Validação por IA Generativa (Claude - Anthropic)
- Formatação dos dados de telemetria como prompt estruturado
- Cenário 1 (dados normais): Claude classifica como **APTO para decolagem**
- Cenário 2 (dados com anomalias): Claude classifica como **NÃO APTO**, com justificativa detalhada e recomendações

### 1.6 Reflexão Crítica
- Ética e responsabilidade na automação de decisões espaciais (framework ELSI)
- Workshop NASA "Artemis, Ethics and Society" (Pirtle et al., 2023)
- Acordos Artemis e princípios de cooperação internacional
- Conferência UNOOSA sobre Atividades Lunares Sustentáveis (2024)
- Exploração sustentável segundo a ESA (ISRU, programa MELiSSA)
- Sustentabilidade espacial (NASA Space Sustainability Strategy, 2024)
- Biotecnologias microbianas para exploração sustentável (Santomartino et al., 2023)
- Eficiência energética e Green IT (Cap. 7 e Cap. 8 da FIAP)

## Como Executar

### Pré-requisitos
- Python 3.x instalado

### Execução local com Jupyter Notebook
1. Clone este repositório:
   ```bash
   git clone https://github.com/marcelobaldin/projeto-fase1-decolagem-missao.git
   cd projeto_fase_I
   ```
2. Instale o Jupyter (se necessário):
   ```bash
   pip install jupyter
   ```
3. Abra o notebook:
   ```bash
   jupyter notebook projeto_decolagem.ipynb
   ```
4. Execute todas as células sequencialmente (Kernel > Restart & Run All)

### Execução no Google Colab
1. Acesse [Google Colab](https://colab.research.google.com/)
2. Faça upload do arquivo `projeto_decolagem.ipynb`
3. Execute todas as células sequencialmente

## Tecnologias Utilizadas

- **Python 3.13**
- **Jupyter Notebook**
- **Graphviz** (geração do fluxograma)
- **fpdf2** (geração do relatório PDF)
- **Claude (Anthropic)** (validação por IA generativa - seção 1.5.1)

## Referências

- Material didático FIAP - Fase I: Decolagem da Missão
  - Cap. 6: O Surgimento da Inteligência que Apoia a Tomada de Decisão
  - Cap. 7: A Energia que Sustenta o Primeiro Impulso da Missão
  - Cap. 8: As Forças Sociais e Tecnológicas que Moldam o Mundo Digital
- NASA (2024). *Responsible Exploration: Ethical, Legal, and Societal Implications of the Artemis Campaign*.
- Pirtle, Z., McBrayer, K. & Beauchemin, A. (2023). *Artemis, Ethics and Society: Synthesis from a Workshop*. NASA OTPS.
- NASA (2024). *Space Sustainability Strategy, Volume 1: Earth Orbit*.
- Palmroth, M. & Hukkinen, J. I. (2025). *Ecology and Society*, 30(2):6.
- Santomartino, R. et al. (2023). *Nature Communications*, 14:1391.
- UNOOSA (2024). *Conference on Sustainable Lunar Activities*.
- ESA (2024). *Sustainable Exploration*.

---

*Projeto desenvolvido como parte do curso de Ciências da Computação - FIAP (2026)*
