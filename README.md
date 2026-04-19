# 📊 Simples Simulador de Economia de Conta de Energia com Geração Solar

## 🎯 Objetivo
Este simulador foi desenvolvido para ajudar no entendimento da conta de energia elétrica com geração solar (GD), utilizando parâmetros típicos da Equatorial MA (São Luís).

A ferramenta permite comparar:
- Conta **com geração solar**
- Conta **sem geração solar**
- Economia gerada
- Indicadores financeiros do investimento

---

## ⚙️ Lógica do Modelo

O simulador parte de duas ideias principais:

- **Autoconsumo (kWh)** = Geração total – Energia injetada  
- **Consumo total da casa (kWh)** = Consumo da rede + Autoconsumo  

Com isso, é possível reconstruir:
- O consumo real da residência
- O impacto da geração solar na fatura

---

## 🧾 Principais Entradas

### 🔵 Campos principais (destacados)
- **Geração total (kWh)** → energia produzida pelo sistema
- **Energia injetada (kWh)** → energia enviada para a rede
- **Consumo da rede (kWh)** → base da fatura

### ⚡ Tarifas
- **Tarifa com geração (R$/kWh)** → usada no cenário com solar  
- **Tarifa normal (R$/kWh)** → usada no cenário sem solar (padrão: 1,17)

⚠️ A tarifa normal pode variar conforme:
- Bandeira tarifária
- Tributos
- Componentes tarifários

---

## 💰 Cálculos Realizados

### 🏠 Conta sem solar
Conta sem solar = (consumo total da casa × tarifa normal) + CIP + outros

### ☀️ Conta com solar
Conta com solar = GD2 + (Benefício bruto – Benefício líquido) + CIP + outros

### 💸 Economia
Economia = Conta sem solar – Conta com solar

### 📊 Economia percentual
Economia (%) = Economia ÷ Conta sem solar

---

## 📈 Indicadores de Investimento

Se informado o investimento inicial:

### ⏳ Payback
Payback = investimento ÷ economia mensal

### 📅 Economia acumulada
- 1 ano → economia × 12  
- 5 anos → economia × 60  

### 📉 Retorno (estimado)
- Mensal → economia ÷ investimento  
- Anual → mensal × 12  

⚠️ Observação: esta não é uma TIR financeira clássica, mas uma aproximação simples.

---

## 🧠 Interpretação dos Resultados

- Se a economia for alta → sistema bem dimensionado  
- Se a conta com solar ainda for alta → pode haver:
  - baixo autoconsumo
  - alta injeção
  - cobrança relevante de GD2  
- Diferença entre estimado e real → ajuste os parâmetros

---

## ⚠️ Limitações

- Não considera:
  - degradação do sistema
  - inflação energética
  - reajustes tarifários futuros
- Baseado em aproximações da fatura real

---

## 🚀 Possíveis Evoluções

- Simulação com inflação energética
- Fluxo de caixa descontado (TIR real)
- Gráficos de fluxo energético
- Comparação entre cenários de dimensionamento

---

## 📌 Conclusão

O simulador é uma ferramenta prática para:
- Entender sua conta
- Validar economia da energia solar
- Apoiar decisões de investimento
