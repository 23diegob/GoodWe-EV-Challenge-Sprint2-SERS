# EcoCharge Smart Grid - Sprint 2
## Prova de Conceito Funcional

### Integrantes

Lucca Bertolini - RM: 569552

Diego de Oliveira Brandão - RM: 569773 

Raphaello Caffettani - RM: 572334

Cristhian Henrique Clementino - RM: 574117

Fabio Pena Vieira - RM: 570441

---

# Descrição do Projeto

O **EcoCharge Smart Grid** é uma solução voltada para mobilidade elétrica inteligente, gestão energética e infraestrutura sustentável. O projeto busca desenvolver uma infraestrutura inteligente para eletropostos urbanos, utilizando análise de dados e distribuição energética estratégica para otimizar o carregamento de veículos elétricos.

A proposta foi criada considerando o crescimento da mobilidade elétrica e os desafios futuros relacionados ao aumento da demanda energética nas cidades inteligentes.

O sistema pretende unir:

- gerenciamento inteligente de energia;
- monitoramento em tempo real;
- eficiência energética;
- integração com energias renováveis;
- redução de desperdícios;
- mobilidade sustentável.

---

# Objetivo da Sprint

O objetivo da Sprint 2 é desenvolver uma **prova de conceito funcional** capaz de demonstrar a viabilidade técnica inicial da solução apresentada na Sprint 1.

Nesta etapa foi desenvolvido um protótipo simulado que representa o funcionamento básico de um sistema inteligente para gerenciamento energético em eletropostos.

O foco principal consiste em demonstrar:

- monitoramento dos níveis de bateria;
- análise automática de dados;
- priorização inteligente do carregamento;
- distribuição eficiente da energia;
- aplicação dos conceitos de sustentabilidade.

---

# Problema Identificado

Com o crescimento do número de veículos elétricos, diversos desafios surgem relacionados à infraestrutura energética:

- aumento da demanda por energia;
- filas em horários de pico;
- sobrecarga da rede elétrica;
- desperdício energético;
- baixa eficiência operacional;
- ausência de priorização entre veículos.

Sem uma gestão inteligente, os eletropostos podem distribuir energia igualmente entre todos os veículos, mesmo quando alguns possuem bateria crítica.

Isso pode aumentar o tempo de espera e reduzir a eficiência do sistema.

---

# Solução Proposta

O EcoCharge Smart Grid propõe um sistema capaz de monitorar continuamente os dados recebidos dos veículos conectados ao eletroposto e utilizar essas informações para tomar decisões automáticas.

No protótipo desenvolvido, o sistema recebe dados simulados referentes aos níveis de bateria dos veículos e determina qual deles possui maior necessidade de carregamento.

A partir dessa análise, a energia é distribuída de maneira estratégica.

---

# Funcionalidade Demonstrada

A funcionalidade principal apresentada nesta Sprint foi:

## Priorização Inteligente de Carregamento

O protótipo simula três veículos:

- Veículo 1 → 80%
- Veículo 2 → 50%
- Veículo 3 → 10%

O sistema identifica automaticamente o veículo mais crítico e define sua prioridade de atendimento.

Resultado esperado:

```txt
Veículo prioritário: Veículo 3
Motivo: menor nível de bateria identificado
Prioridade: Alta
```

---

# Arquitetura do Sistema

A arquitetura foi dividida em três etapas principais:

```txt
┌────────────────────────┐
│ Entrada de Dados       │
│------------------------│
│ • Nível da bateria     │
│ • Veículos conectados  │
│ • Energia disponível   │
│ • Geração solar        │
│ • Demanda energética   │
└──────────┬─────────────┘
           │
           ▼
┌────────────────────────┐
│ Processamento          │
│------------------------│
│ • Análise dos dados    │
│ • Comparação           │
│ • Priorização          │
│ • Decisão automática   │
└──────────┬─────────────┘
           │
           ▼
┌────────────────────────┐
│ Saída de Dados         │
│------------------------│
│ • Veículo prioritário  │
│ • Dashboard            │
│ • Status operacional   │
│ • Fluxo energético     │
└────────────────────────┘
```

---

## Entrada de Dados

Nesta etapa, o sistema recebe informações relacionadas ao carregamento:

Dados utilizados:

- nível de bateria dos veículos;
- demanda energética;
- energia disponível;
- quantidade de veículos conectados;
- geração solar simulada.

Em aplicações futuras, essas informações poderiam ser obtidas por:

- sensores inteligentes;
- Internet das Coisas (IoT);
- APIs dos veículos;
- painéis solares;
- medidores energéticos.

---

## Processamento

Após receber as informações, o sistema executa uma lógica de decisão.

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

## Saída de Dados

Após a análise, o sistema apresenta:

- veículo prioritário;
- ordem de carregamento;
- status operacional;
- distribuição energética;
- informações do dashboard.

---

# Justificativas Técnicas

As decisões adotadas foram baseadas em critérios de eficiência energética e sustentabilidade.

## Priorização automática

Justificativa:

Um sistema convencional trata todos os veículos da mesma maneira.

A solução proposta utiliza análise de dados para identificar necessidades prioritárias.

Benefícios:

- redução do tempo de espera;
- melhor distribuição energética;
- redução de desperdícios;
- maior eficiência.

---

## Simulação de energia solar

Justificativa:

A energia solar representa uma das principais fontes renováveis utilizadas atualmente.

Benefícios:

- redução da dependência da rede elétrica;
- menor emissão de poluentes;
- redução de custos;
- incentivo ao uso de energia limpa.

---

## Dashboard e monitoramento

Justificativa:

Monitoramento em tempo real permite decisões rápidas.

Benefícios:

- maior controle operacional;
- acompanhamento do sistema;
- análise de desempenho;
- maior confiabilidade.

---

# Diagramas

## Fluxo operacional

```txt
Veículos conectados
        ↓
Leitura dos níveis de bateria
        ↓
Análise dos dados
        ↓
Sistema define prioridade
        ↓
Distribuição energética
        ↓
Exibição dos resultados
```

---

## Diagrama conceitual

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

# Exemplo de Simulação

| Veículo | Nível de bateria | Prioridade |
|---|---:|---|
| Veículo 1 | 80% | Baixa |
| Veículo 2 | 50% | Média |
| Veículo 3 | 10% | Alta |

Resultado:

```txt
Veículo priorizado: Veículo 3
Motivo: menor nível de bateria identificado
Status: Prioridade Alta
```

---

# Sustentabilidade e Energias Renováveis

A sustentabilidade representa um dos principais pilares do EcoCharge Smart Grid.

O sistema considera a utilização de energia solar através de painéis fotovoltaicos instalados nos eletropostos.

Objetivos:

- utilizar energia limpa;
- reduzir consumo da rede elétrica;
- diminuir emissão indireta de carbono;
- aumentar eficiência energética.

Aplicações sustentáveis:

- redução de desperdícios;
- aproveitamento energético inteligente;
- menor impacto ambiental;
- incentivo à mobilidade elétrica.

---

# Eficiência Energética

O sistema busca otimizar a utilização da energia disponível.

Benefícios:

- menor desperdício;
- equilíbrio entre demanda e consumo;
- distribuição inteligente;
- melhor utilização dos recursos.

---

# Tecnologias Utilizadas

Possíveis tecnologias utilizadas:

- Python
- HTML
- CSS
- JavaScript
- GitHub
- Simulações energéticas
- Dashboards

---

# Instruções de Uso

1. Clonar o repositório:

```bash
git clone LINK_DO_REPOSITORIO
```

2. Abrir o projeto.

3. Executar a simulação.

4. Inserir ou visualizar os níveis de bateria:

Exemplo:

```txt
Veículo 1 → 80%
Veículo 2 → 50%
Veículo 3 → 10%
```

5. Executar a lógica de decisão.

6. Observar a prioridade definida pelo sistema.

7. Analisar os resultados exibidos.

---

# Melhorias Futuras

Como evolução do projeto:

- sensores reais;
- integração com Arduino/ESP32;
- inteligência artificial;
- dashboard em tempo real;
- integração com cidades inteligentes;
- armazenamento energético inteligente;
- aplicativo para usuários;
- previsão de demanda energética.

---

# Conclusão

A Sprint 2 demonstrou a viabilidade técnica inicial do EcoCharge Smart Grid por meio de uma prova de conceito funcional.

O sistema foi capaz de monitorar dados simulados, analisar níveis de bateria e definir prioridades automáticas de carregamento.

Além disso, o projeto incorpora princípios de energias renováveis e sustentabilidade, reforçando seu potencial para aplicações futuras em infraestrutura energética inteligente.
