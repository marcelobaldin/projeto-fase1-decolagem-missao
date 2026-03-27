# Projeto Fase I - Decolagem da Missao

## FIAP - Ciencias da Computacao

**Aluno:** Marcelo Bastianello Baldin
**RM:** 568746
**Disciplina:** Atividade Integradora - Fase I

---

## Descricao do Projeto

Este projeto faz parte da Atividade Integradora da Fase I (Decolagem da Missao) do curso de Ciencias da Computacao da FIAP. O objetivo e simular um sistema de verificacao pre-decolagem de uma missao espacial, integrando conceitos de:

- **Computacao**: logica de programacao, algoritmos de verificacao, Python
- **Eficiencia Energetica**: calculos de autonomia, perdas energeticas, rendimento
- **Inteligencia Artificial**: classificacao de dados, deteccao de anomalias
- **Sustentabilidade**: reflexao sobre etica, impacto social e tecnologia verde

## Estrutura do Projeto

```
projeto_fase_I/
├── projeto_decolagem.ipynb    # Notebook principal com todo o codigo e analises
└── README.md                  # Este arquivo
```

## Funcionalidades

### 1.1 Organizacao da Telemetria
- Definicao dos dados de sensores: temperatura, pressao, energia, integridade, modulos
- Apresentacao em formato tabular com indicadores de status
- Definicao de faixas seguras para cada parametro

### 1.2 Algoritmo de Verificacao
- Pseudocodigo estruturado do algoritmo de decisao
- Fluxograma textual do processo de verificacao
- Logica de decisao: "PRONTO PARA DECOLAR" ou "DECOLAGEM ABORTADA"

### 1.3 Script Python
- Funcao `verificar_decolagem()` que realiza todas as verificacoes
- Teste com cenario normal (todos os parametros OK)
- Teste com cenario de anomalias (parametros fora da faixa)

### 1.4 Analise Energetica
- Calculo de energia disponivel com base na capacidade e carga atual
- Calculo de perdas energeticas (dissipacao termica / entropia)
- Calculo de autonomia pos-decolagem em horas e dias
- Calculo de rendimento global (eta)
- Referencia aos conceitos do Cap. 7 (2a Lei da Termodinamica, P = I^2 x R)

### 1.5 Analise Assistida por IA
- Classificacao dos parametros em NORMAL / ATENCAO / CRITICO
- Identificacao automatica de anomalias
- Sugestoes de risco baseadas na analise dos dados
- Analise de correlacao entre parametros

### 1.6 Reflexao Critica
- Etica e responsabilidade na automacao de decisoes criticas
- Impacto social da exploracao espacial
- Sustentabilidade tecnologica e eficiencia energetica

## Como Executar

### Pre-requisitos
- Python 3.x instalado

### Execucao local com Jupyter Notebook
1. Clone este repositorio:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd projeto_fase_I
   ```
2. Instale o Jupyter (se necessario):
   ```bash
   pip install jupyter
   ```
3. Abra o notebook:
   ```bash
   jupyter notebook projeto_decolagem.ipynb
   ```
4. Execute todas as celulas sequencialmente (Kernel > Restart & Run All)

### Execucao no Google Colab
1. Acesse [Google Colab](https://colab.research.google.com/)
2. Faca upload do arquivo `projeto_decolagem.ipynb`
3. Execute todas as celulas sequencialmente

## Prints da Execucao

### 1.1 Relatorio de Telemetria

```
===========================================================================
            RELATORIO DE TELEMETRIA PRE-DECOLAGEM
===========================================================================

Parametro                              Valor        Faixa Segura       Status
---------------------------------------------------------------------------
Temperatura Interna (C)                22.5         15 a 30            [OK]
Temperatura Externa (C)                -45.2        -60 a 50           [OK]
Integridade Estrutural                 1            1 a 1              [OK]
Nivel de Energia (%)                   92           80 a 100           [OK]
Pressao Tanque Principal (bar)         310.5        280 a 350          [OK]
Pressao Tanque Reserva (bar)           295.0        280 a 350          [OK]
---------------------------------------------------------------------------

Modulos Criticos                       Status       Verificacao
---------------------------------------------------------------------------
Modulo Navegacao                       operacional  [OK]
Modulo Comunicacao                     operacional  [OK]
Modulo Suporte de Vida                 operacional  [OK]
Modulo Propulsao                       operacional  [OK]
===========================================================================
```

### 1.3 Verificacao Pre-Decolagem - Cenario Normal

```
======================================================================
       SISTEMA DE VERIFICACAO PRE-DECOLAGEM
              Cenario: Dados Normais
======================================================================

Verificacao                              Resultado
-------------------------------------------------------
  Temperatura Interna (C)                [OK]
  Temperatura Externa (C)                [OK]
  Integridade Estrutural                 [OK]
  Nivel de Energia (%)                   [OK]
  Pressao Tanque Principal (bar)         [OK]
  Pressao Tanque Reserva (bar)           [OK]
  Modulo Navegacao                       [OK]
  Modulo Comunicacao                     [OK]
  Modulo Suporte de Vida                 [OK]
  Modulo Propulsao                       [OK]

======================================================================

>>> DECISAO FINAL: PRONTO PARA DECOLAR
    Todos os sistemas operacionais. Decolagem autorizada.

======================================================================
```

### 1.3 Verificacao Pre-Decolagem - Cenario com Anomalias

```
======================================================================
       SISTEMA DE VERIFICACAO PRE-DECOLAGEM
           Cenario: Dados com Anomalias
======================================================================

Verificacao                              Resultado
-------------------------------------------------------
  Temperatura Interna (C)                [FALHA]
  Temperatura Externa (C)                [OK]
  Integridade Estrutural                 [OK]
  Nivel de Energia (%)                   [FALHA]
  Pressao Tanque Principal (bar)         [OK]
  Pressao Tanque Reserva (bar)           [FALHA]
  Modulo Navegacao                       [OK]
  Modulo Comunicacao                     [FALHA]
  Modulo Suporte de Vida                 [OK]
  Modulo Propulsao                       [OK]

======================================================================

>>> DECISAO FINAL: DECOLAGEM ABORTADA
    Problemas detectados:
    -> ALERTA: Temperatura Interna (C) = 35.8 (faixa segura: 15 a 30)
    -> ALERTA: Nivel de Energia (%) = 72 (faixa segura: 80 a 100)
    -> ALERTA: Pressao Tanque Reserva (bar) = 270.0 (faixa segura: 280 a 350)
    -> ALERTA: Modulo Comunicacao esta com status 'falha'

======================================================================
```

### 1.4 Analise Energetica

```
======================================================================
            ANALISE ENERGETICA DA MISSAO
======================================================================

PARAMETROS DE ENTRADA:
  Capacidade total dos bancos:     500 kWh
  Carga atual:                     92%
  Consumo estimado (decolagem):    150 kWh
  Taxa de perdas energeticas:      5%
  Consumo medio em orbita:         12 kWh/h

CALCULOS:
  1. Energia disponivel:           500 x 92% = 460.0 kWh
  2. Perdas energeticas:           460.0 x 5% = 23.0 kWh
  3. Energia pos-decolagem:        460.0 - 150 - 23.0 = 287.0 kWh
  4. Autonomia em orbita:          287.0 / 12 = 23.9 horas
  5. Rendimento global (eta):      95.0%

RESULTADO:
  Energia restante pos-decolagem:  287.0 kWh
  Autonomia estimada:              23.9 horas (1.0 dias)
  Status:                          AUTONOMIA LIMITADA - monitorar

======================================================================
```

### 1.5 Analise IA - Cenario Normal

```
======================================================================
       ANALISE ASSISTIDA POR IA - CENARIO NORMAL
======================================================================

CLASSIFICACAO DOS DADOS:
  Parametro                              Valor        Classe
  --------------------------------------------------------------
  Temperatura Interna (C)                22.5         [N] NORMAL
  Temperatura Externa (C)                -45.2        [A] ATENCAO
  Integridade Estrutural                 1            [N] NORMAL
  Nivel de Energia (%)                   92           [N] NORMAL
  Pressao Tanque Principal (bar)         310.5        [N] NORMAL
  Pressao Tanque Reserva (bar)           295.0        [N] NORMAL
  Modulo Navegacao                       operacional  [N] NORMAL
  Modulo Comunicacao                     operacional  [N] NORMAL
  Modulo Suporte de Vida                 operacional  [N] NORMAL
  Modulo Propulsao                       operacional  [N] NORMAL

ANOMALIAS DETECTADAS:
  -> Temperatura Externa (C): valor -45.2 PROXIMO ao limite da faixa segura

SUGESTOES DE RISCO:
  [RISCO MEDIO] 1 parametro(s) em ATENCAO
    Recomendacao: verificar tendencia nas proximas leituras

======================================================================
```

### 1.5 Analise IA - Cenario com Anomalias

```
======================================================================
     ANALISE ASSISTIDA POR IA - CENARIO COM ANOMALIAS
======================================================================

CLASSIFICACAO DOS DADOS:
  Parametro                              Valor        Classe
  --------------------------------------------------------------
  Temperatura Interna (C)                35.8         [C] CRITICO
  Temperatura Externa (C)                -45.2        [A] ATENCAO
  Integridade Estrutural                 1            [N] NORMAL
  Nivel de Energia (%)                   72           [C] CRITICO
  Pressao Tanque Principal (bar)         310.5        [N] NORMAL
  Pressao Tanque Reserva (bar)           270.0        [C] CRITICO
  Modulo Navegacao                       operacional  [N] NORMAL
  Modulo Comunicacao                     falha        [C] CRITICO
  Modulo Suporte de Vida                 operacional  [N] NORMAL
  Modulo Propulsao                       operacional  [N] NORMAL

ANOMALIAS DETECTADAS:
  -> Temperatura Interna (C): valor 35.8 FORA da faixa segura (15 a 30)
  -> Temperatura Externa (C): valor -45.2 PROXIMO ao limite da faixa segura
  -> Nivel de Energia (%): valor 72 FORA da faixa segura (80 a 100)
  -> Pressao Tanque Reserva (bar): valor 270.0 FORA da faixa segura (280 a 350)
  -> Modulo Comunicacao: status 'falha' - NAO OPERACIONAL

SUGESTOES DE RISCO:
  [RISCO ALTO] 4 parametro(s) em estado CRITICO
    Recomendacao: manutencao corretiva antes de nova tentativa
  [RISCO MEDIO] 1 parametro(s) em ATENCAO
    Recomendacao: verificar tendencia nas proximas leituras
  [CORRELACAO] Temperatura alta + energia baixa pode indicar
    sobrecarga nos sistemas de refrigeracao

======================================================================
```

## Tecnologias Utilizadas

- **Python 3.13**
- **Jupyter Notebook**

## Referencias

- Material didatico FIAP - Fase I: Decolagem da Missao
  - Cap. 6: O Surgimento da Inteligencia que Apoia a Tomada de Decisao
  - Cap. 7: A Energia que Sustenta o Primeiro Impulso da Missao
  - Cap. 8: As Forcas Sociais e Tecnologicas que Moldam o Mundo Digital

---

*Projeto desenvolvido como parte do curso de Ciencias da Computacao - FIAP (2026)*
