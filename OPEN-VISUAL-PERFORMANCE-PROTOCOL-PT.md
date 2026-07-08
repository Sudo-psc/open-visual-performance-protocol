# Protocolo Aberto de Desempenho Visual (OVPP)

**Versão 1.1 — implementação operacional.**
Protocolo prático e aberto para organizações adotarem na redução da fricção visual em trabalho intensivo em telas, preservando privacidade e confiança.

> Projetado para ser **implementado, não comercializado**. Use seus próprios dados, sua própria estrutura operacional e seus próprios parceiros clínicos.

## 1) Objetivo deste protocolo

O OVPP é para organizações que querem:

- medir carga visual como variável operacional,
- reduzir fricção visual com intervenções de baixo risco,
- definir fluxo seguro de encaminhamento clínico para quem precisa,
- e decidir expansão por evidência, e não por impressão.

Este protocolo **não substitui** a prática oftalmológica e não autoriza diagnóstico por gestores.

## 2) Princípios (inegociáveis)

1. **Meça padrões, não pessoas.** Toda a análise rotineira é agregada por time/função, sem expor informação médica individual.
2. **Camadas universais e de baixo custo antes da etapa clínica.** Ajustar ambiente, rotina e comportamento vem antes de encaminhamento.
3. **Instrumento fixo ao longo do tempo.** Manter um único questionário validado no baseline, no meio e na reavaliação.
4. **Conservadorismo por padrão.** Use premissas explícitas, faixas de cenário e evite inflar ganhos.
5. **Participação voluntária e possibilidade de recusa.** A participação não é critério de desempenho.
6. **Trabalho visível.** O protocolo precisa entrar no ritmo operacional da empresa, não em campanha isolada.

## 3) Modelo operacional do programa

### 3.1 Papéis e limites

- **Dono do programa (Pessoas/People Ops):** dono de cronograma, comunicação e adoção.
- **Responsável de dados:** mantém relatórios agregados e controles de retenção.
- **Facilities/TI:** executa ajustes ambientais e configurações.
- **Saúde ocupacional:** recebe encaminhamentos e gerencia a trilha de avaliação.
- **Médico oftalmologista/Clínica:** realiza diagnóstico e tratamento quando clinicamente indicado.

Regra de fronteira: gestores e RH atuam nas camadas 0–3; clínica nas camadas 4+.

### 3.2 Fluxo em camadas

1. **Camada 0 — Triagem anônima de base**
2. **Camada 1 — Mapa de risco e priorização por função**
3. **Camada 2 — Padronização ambiental**
4. **Camada 3 — Pausas visuais desenhadas no fluxo**
5. **Camada 4 — Encaminhamento seletivo**
6. **Camada 5 — Reavaliação e governança**

**Ordem invariável:** linha de base → correção ambiental → micro-pausas programadas → encaminhamento seletivo → reavaliação.

## 4) Camada 0: triagem e linha de base

Use um instrumento validado e único durante todo o ciclo (exemplos: CVS-Q, DEQ-5, OSDI, SPEED).

Regras operacionais:

- Definir cronograma fixo: baseline (D+0), linha de meio (opcional D+60), final (D+90), depois cadência trimestral/semestral.
- Não alterar questionário durante a execução.
- Evitar troca de instrumento sem reinício formal do ciclo.
- Coletar apenas identificadores agregáveis: área, grupo de função, senioridade (opcional), modalidade (escritório/home).

Saída da camada:

- prevalência inicial por grupo,
- intensidade inicial (leve/moderada/severa).

## 5) Camada 1: mapa de risco por função

Estratificar por função e exposição:

- desenvolvimento/revisão,
- QA,
- design,
- suporte de alto uso de vídeo,
- análise/finanças,
- funções mistas com alta exposição de tela.

Combinar:

- escores de sintomas,
- horas de tela e carga de chamadas,
- número de monitores,
- condição base de ambiente/ergonomia.

Saída:

- mapa de carga visual por função,
- lista de áreas prioritárias,
- sem mapa por indivíduo.

## 6) Camada 2: checklist ambiental

Aplicar em todas as estações e validar equivalente no home office:

- distância de tela: 50–70 cm,
- borda superior do monitor no nível dos olhos ou ligeiramente abaixo,
- antirreflexo e superfícies mate,
- monitor alinhado ao eixo natural de visão,
- evitar reflexos de janelas diretas/alta luz lateral,
- umidade alvo de 40–60%,
- temperatura em torno de 21–23 °C,
- fluxo de ar direcionado para longe do rosto,
- contraste/brilho e tamanho de fonte revisados,
- layout de software com menos ruído visual.

Observação de investimento:

- **Evitar priorizar filtro de luz azul como prevenção**, salvo revisão consistente de evidência futura.

## 7) Camada 3: pausas como infraestrutura

Trate recuperação visual como infraestrutura contínua:

- prompts integrados a ferramentas de fluxo (calendário, IDE, repositório, mensagens),
- alinhamento ao ritmo já existente (blocos de sprint, janelas de revisão, agenda de reuniões),
- janelas padrão de pausa.

Cadência recomendada:

- a cada 20 min: pausa de 20 segundos com foco distante,
- a cada 90 min: 5–10 minutos com menor demanda de foco próximo,
- em reuniões longas: inserir pelo menos um bloco com redução de tela quando possível.

Princípio: instrução por si só tem baixa aderência; prompt persistente e sistemático escala melhor.

## 8) Camada 4: protocolo de encaminhamento

Aplicar após camadas 0–3 e checagens ambientais.

### 8.1 Triagem inicial

- **Baixo risco**
  - sintomas raros e leves,
  - sem impacto funcional,
  - melhora com pausas simples.

- **Risco moderado**
  - sintomas semanais recorrentes,
  - impacto funcional leve a moderado,
  - associação clara com tela/ambiente.

- **Alto risco**
  - sintomas persistentes,
  - embaçamento recorrente ou desconforto importante,
  - dor, fotofobia, vermelhidão persistente,
  - uso frequente de colírios sem orientação,
  - piora em usuário de lente de contato.

### 8.2 Encaminhamento imediato

Encaminhar imediatamente quando houver:

- dor ocular relevante,
- piora importante da visão,
- sintomas assimétricos intensos,
- secreção,
- suspeita de infecção/inflamação aguda,
- trauma ocular,
- fotofobia importante,
- piora relevante em usuário de lente.

### 8.3 Pacote de encaminhamento

Com consentimento:

- função/cargo e carga de exposição,
- horas de tela e chamadas,
- condições de home office/escritório,
- escore de triagem e padrão de sintomas,
- medidas ambientais já realizadas.

## 9) Camada 5: governança e painel

Indicadores mínimos (agregados):

| Indicador | Fonte | Cadência |
|---|---|---|
| Prevalência de sintomas | questionário de triagem | semestral |
| Intensidade de sintomas | questionário de triagem | trimestral |
| Carga de exposição | TI/autodeclaração | trimestral |
| Conformidade ambiental | checklist de facilities | mensal |
| Aderência a pausas | dados de software/autodeclaração | mensal |
| Participação no programa | logs da campanha | mensal |
| Percepção de produtividade e qualidade | mini-enquete interna | trimestral |

Ritmos obrigatórios:

- **mensal:** ambiente e adesão às pausas,
- **trimestral:** exposição e intensidade de sintomas,
- **semestral:** prevalência e revisão estratégica.

## 10) Estrutura de piloto de 90 dias

| Semana | Marco |
|---|---|
| 1–2 | triagem inicial + mapa da situação |
| 2–3 | mapa de risco + escolha de áreas prioritárias |
| 3–6 | correções ambientais |
| 4–12 | comunicação + rotina de pausas |
| 6–12 | execução da trilha de encaminhamento |
| 12–13 | reavaliação + revisão executiva |

Critérios de saída:

- melhoria mensurável mínima em adesão/sintomas **ou** razão documentada para resultado nulo,
- decisão registrada de escalar, ajustar ou interromper.

## 11) ROI e política anti-hipérbole

Modelo de simulação:

- **Custo da inação** = `N × custo_líquido_por_pessoa × prevalência × perda_produtividade`
- **Benefício recuperado** = `custo_da_inação × fração_recuperável`

Faixas de cenário (somente simulação):

- conservador / base / risco alto,
- premissas explícitas acompanhadas de cada cálculo,
- nunca apresentar um único valor determinístico.

Nunca afirmar que toda a perda produtiva observada é causada por fadiga visual ou que o protocolo recuperará toda perda possível.

## 12) Privacidade, ética e postura legal

- Relatórios agregados; nada de resultado individual para gestores.
- Sem participação obrigatória.
- Nenhum diagnóstico por equipe não clínica.
- Encaminhamento e cuidados separados de avaliação de performance.
- Termo de propósito em linguagem simples para participantes.

**Minimização de dados:** apenas o necessário para decisão operacional.

## 13) Checklist de implantação

- [ ] Escolher e travar um instrumento de triagem.
- [ ] Definir grupos de função e área alvo.
- [ ] Publicar as regras não negociáveis com liderança e participantes.
- [ ] Rodar baseline e publicar mapa de risco por função.
- [ ] Acionar ambiente + pausas em paralelo.
- [ ] Ativar critérios de encaminhamento imediato.
- [ ] Reavaliar e fechar piloto por evidência.

## Fechamento

Este protocolo é aberto e deliberadamente conservador. Ajuste limiares clínicos para requisitos legais locais e operacionais, mas mantenha sequência e ética inalteradas.
