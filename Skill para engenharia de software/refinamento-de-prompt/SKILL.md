---
name: refinamento-de-prompt
description: Refine user-provided prompts into clear, actionable instructions using role, context, task, constraints, and output format. Use whenever a user asks to improve, rewrite, optimize, or structure a prompt. Always ask clarifying questions before producing the refined prompt.
---

# Refinamento de Prompt

Transforme o prompt enviado pelo usuário em instruções claras, específicas e úteis, preservando sua intenção. **Nunca entregue a versão refinada antes de fazer perguntas ao usuário e receber as respostas.**

## Fluxo

1. **Leia o prompt e identifique lacunas.** Avalie os cinco pilares abaixo e note o que já está explícito, o que pode ser inferido com segurança e o que muda materialmente o resultado.
2. **Faça perguntas antes de refinar.** Em uma única mensagem concisa, pergunte apenas o necessário para esclarecer lacunas relevantes. Não pergunte novamente o que o usuário já informou. Se o pedido inicial estiver completo, ainda faça pelo menos uma pergunta de confirmação ou preferência (por exemplo, público/plataforma, nível de detalhe ou se deve preservar a formulação original). Aguarde a resposta antes de escrever o prompt refinado.
3. **Resolva ambiguidades restantes com parcimônia.** Se as respostas não bastarem e a escolha puder alterar materialmente o resultado, faça uma pergunta complementar. Caso contrário, adote a interpretação mais conservadora e explicite a suposição.
4. **Refine sem desviar.** Preserve o objetivo, os fatos e as preferências do usuário. Não invente contexto, dados, requisitos ou capacidades. Torne instruções implícitas explícitas apenas quando apoiadas pelo que foi dito.
5. **Entregue o resultado.** Apresente o prompt pronto para copiar, normalmente em bloco de código. Se útil, acrescente uma nota breve sobre suposições ou mudanças principais. Não sobrecarregue com explicações.

## Pilares de avaliação

Use os pilares como checklist flexível; não force todos quando forem irrelevantes:

- **Papel (persona):** quem a IA deve ser ou que perspectiva deve adotar.
- **Contexto:** cenário, público-alvo, objetivo e informações necessárias.
- **Ação/tarefa:** resultado solicitado, expresso com verbos claros e etapas quando necessário.
- **Restrições:** limites, itens a evitar, tom, idioma, tamanho, fontes ou critérios de qualidade.
- **Formato:** estrutura esperada da resposta, como lista, tabela, roteiro, JSON ou texto corrido.

## Como perguntar

- Prefira de 1 a 4 perguntas curtas, agrupadas numa só mensagem.
- Priorize escolhas concretas e de alto impacto; ofereça opções quando isso facilitar a resposta.
- Não transforme a interação numa entrevista longa. Se uma resposta aberta bastar, faça uma pergunta aberta objetiva.
- Considere questões como: para quem é o resultado; onde será usado; qual é o sucesso esperado; que tom e profundidade prefere; quais limites ou informações devem ser respeitados; em que formato deseja a resposta.
- Pergunte somente sobre elementos que não estejam claros no pedido original.

Exemplo de primeira resposta:

> Posso refinar. Para ajustar o prompt sem mudar sua intenção: **quem será o público-alvo**, **onde você vai usar a resposta** e **qual formato prefere**? Se algum desses pontos não for importante, pode dizer “tanto faz”.

## Formato de entrega sugerido

**Prompt refinado**

```text
[Instruções finais claras, completas e prontas para copiar.]
```

**Nota opcional:** [uma suposição relevante ou breve explicação da principal melhoria].

Adapte o rótulo e a apresentação ao contexto; se o usuário pedir somente o prompt, entregue somente o bloco refinado. Responda no idioma do usuário, a menos que ele peça outro idioma.