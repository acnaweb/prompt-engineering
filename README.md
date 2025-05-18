# Prompt Engineering

Prompt Engineering

##  Prompts Encadeados

Prompts encadeados dentro de um único prompt mestre — ou seja, um prompt composto que simula uma cadeia de raciocínio ou execução, onde cada etapa usa a saída da anterior como entrada, sem precisar dividir isso em várias mensagens. Essa técnica é especialmente útil para criar agentes de raciocínio passo a passo, pipelines de dados, ou transformações complexas em linguagem natural. 


```sh
Você é um [papel do agente]. Sua tarefa será executar um processo em etapas encadeadas. Cada etapa depende da anterior. Execute tudo de uma vez, mas pense passo a passo.

1. Etapa 1 – [Objetivo da etapa 1]
   Entrada: [dados iniciais]
   Saída esperada: [formato ou resultado]

2. Etapa 2 – [Objetivo da etapa 2]
   Entrada: Use a saída da Etapa 1.
   Transforme ou analise conforme: [detalhes da transformação]

3. Etapa 3 – [Objetivo da etapa 3]
   Entrada: Use a saída da Etapa 2.
   Gere: [descrição da saída final]

Retorne o resultado final da Etapa 3, mas inclua também os resultados intermediários (Etapas 1 e 2) com cabeçalhos claros.
```

```sh
Você é um sistema com múltiplos módulos encadeados. Execute o seguinte pipeline lógico:

### Etapa 1 – [nome]
Objetivo: [explicação]
Entrada: [dado]
Saída esperada: [formato]

### Etapa 2 – [nome]
Objetivo: [explicação]
Entrada: resultado da Etapa 1
Transformação: [o que deve ser feito]

### Etapa 3 – [nome]
Objetivo: [explicação]
Entrada: resultado da Etapa 2
Saída esperada: [descrição clara do formato final]

No final, exiba todas as saídas organizadas:
- Resultado da Etapa 1:
- Resultado da Etapa 2:
- Resultado da Etapa 3:
```

* Exemplo

```sh
Você é um assistente editorial. Sua tarefa é executar três etapas encadeadas com base no seguinte artigo:

Texto: 
"""
A inteligência artificial está mudando o mercado de trabalho. Funções repetitivas estão sendo automatizadas, enquanto novas oportunidades surgem para profissionais que dominam IA, dados e automação.
"""

Etapas:
1. Resuma o conteúdo acima em no máximo 2 frases.
2. Gere um título chamativo baseado no resumo.
3. Crie até 5 hashtags relevantes para esse conteúdo.

Retorne:
- 📌 Resumo:
- 📰 Título:
- 🔖 Hashtags:
```
