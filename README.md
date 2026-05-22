# GoodWe-EV-Challenge-Sprint2-SERS
# Arquitetura do Sistema

A arquitetura do EcoCharge Smart Grid foi organizada em três camadas principais: Entrada de Dados, Processamento Inteligente e Saída de Dados.

Fluxo de funcionamento:

```txt
┌────────────────────────┐
│ Entrada de Dados       │
│------------------------│
│ • Nível da bateria     │
│ • Veículos conectados  │
│ • Demanda energética   │
│ • Energia solar        │
│ • Energia disponível   │
└──────────┬─────────────┘
           │
           ▼
┌────────────────────────┐
│ Processamento          │
│------------------------│
│ • Análise dos dados    │
│ • Comparação dos níveis│
│ • Priorização          │
│ • Decisão automática   │
└──────────┬─────────────┘
           │
           ▼
┌────────────────────────┐
│ Saída de Dados         │
│------------------------│
│ • Veículo prioritário  │
│ • Status do sistema    │
│ • Fluxo energético     │
│ • Dashboard            │
└────────────────────────┘
```

## Funcionamento da Arquitetura

### Entrada de Dados

Nesta etapa, o sistema recebe dados necessários para o gerenciamento energético.

Dados utilizados na simulação:

- nível de bateria dos veículos;
- demanda energética atual;
- energia solar gerada;
- energia disponível;
- quantidade de veículos conectados.

Em uma implementação real, essas informações poderiam ser captadas através de:

- sensores inteligentes;
- sistemas IoT;
- APIs de veículos elétricos;
- painéis solares;
- medidores energéticos.

---

### Processamento Inteligente

Após receber as informações, o sistema executa uma lógica de decisão responsável pela priorização energética.

Lógica aplicada:

```txt
SE bateria ≤ 20%
→ Prioridade Alta

SE bateria >20% e ≤60%
→ Prioridade Média

SE bateria >60%
→ Prioridade Baixa
```

Exemplo:

```txt
Veículo 1 → 80%
Veículo 2 → 50%
Veículo 3 → 10%

Resultado:

Veículo prioritário:
Veículo 3
```

---

### Saída de Dados

Após o processamento, o sistema retorna:

- veículo priorizado;
- ordem de carregamento;
- distribuição energética;
- status operacional;
- informações do dashboard.

Esses dados podem ser visualizados em:

- aplicativo mobile;
- dashboard web;
- painel do eletroposto;
- central de monitoramento.

---

# Justificativas Técnicas

As decisões tomadas no desenvolvimento do EcoCharge Smart Grid foram baseadas em critérios técnicos relacionados à eficiência energética, sustentabilidade e viabilidade de implementação.

### Uso de priorização automática

Justificativa:

Um sistema tradicional distribui energia igualmente entre veículos conectados, independentemente do nível de bateria.

A solução proposta utiliza análise de dados para identificar necessidades prioritárias.

Benefícios:

- redução do tempo de espera;
- melhor distribuição energética;
- menor desperdício;
- maior eficiência operacional.

---

### Simulação de energia solar

Justificativa:

A energia solar é uma das principais fontes renováveis utilizadas atualmente devido à baixa emissão de poluentes e possibilidade de geração distribuída.

Benefícios:

- redução do consumo da rede elétrica;
- menor impacto ambiental;
- diminuição de custos operacionais;
- incentivo ao uso de energia limpa.

---

### Utilização de dashboards e monitoramento

Justificativa:

O monitoramento em tempo real permite identificar rapidamente variações de demanda energética.

Benefícios:

- tomada de decisão mais rápida;
- controle operacional;
- acompanhamento do desempenho do sistema;
- maior confiabilidade.

---

# Diagramas

## Diagrama de Fluxo

```txt
Veículos conectados
        ↓
Leitura do nível da bateria
        ↓
Análise dos dados
        ↓
Sistema define prioridade
        ↓
Distribuição inteligente
        ↓
Exibição dos resultados
```

---

## Diagrama Conceitual

```txt
Painéis solares
       ↓
Armazenamento energético
       ↓
EcoCharge Smart Grid
       ↓
Análise inteligente
       ↓
Distribuição energética
       ↓
Veículos elétricos
```

---

# Instruções de Uso

1. Baixar ou clonar o repositório:

```bash
git clone LINK_DO_REPOSITORIO
```

2. Abrir a simulação.

3. Inserir ou visualizar os dados dos veículos:

Exemplo:

```txt
Veículo 1 → 80%
Veículo 2 → 50%
Veículo 3 → 10%
```

4. Executar a lógica do sistema.

5. Observar o veículo priorizado.

6. Verificar o fluxo energético apresentado no dashboard.

---

# Aplicação dos Princípios de Energias Renováveis e Sustentabilidade

O EcoCharge Smart Grid incorpora princípios de sustentabilidade em diferentes partes da solução.

### Energia Renovável

O sistema considera o uso de energia solar por meio de painéis fotovoltaicos instalados nos eletropostos.

Objetivos:

- aproveitar energia limpa;
- reduzir dependência da rede elétrica;
- diminuir emissão indireta de carbono.

---

### Eficiência Energética

A solução busca utilizar a energia disponível de forma inteligente.

Aplicações:

- priorização automática;
- redução de desperdícios;
- distribuição equilibrada;
- controle do consumo.

---

### Sustentabilidade Ambiental

A proposta contribui para:

- incentivo à mobilidade elétrica;
- redução da emissão de gases poluentes;
- menor impacto ambiental;
- utilização consciente dos recursos energéticos.

---

### Sustentabilidade Tecnológica

O projeto também foi pensado para crescimento futuro:

- integração com sensores reais;
- inteligência artificial;
- cidades inteligentes;
- Internet das Coisas (IoT);
- armazenamento energético inteligente.
