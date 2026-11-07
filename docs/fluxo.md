# Análise curricular — regras e fluxo de negócio

**Status da documentação de origem: em desenvolvimento.** Esta página resume a especificação da equipe no Confluence: [Análise Curricular — Fluxo e Regras de Negócio do equivalencIA](https://edu-team-wv8ssvt9.atlassian.net/wiki/x/sAA3).

## Objetivo

Apoiar o aproveitamento de estudos comparando disciplinas cursadas pelo estudante com disciplinas da matriz curricular do curso de destino. O resultado do EquivalencIA é uma **possibilidade de equivalência**, sujeita à validação acadêmica do responsável pela análise curricular.

## Atores

| Ator | Papel no processo |
|---|---|
| Responsável pela análise curricular (coordenador) | Usuário direto: cadastra ou seleciona o estudante, escolhe curso e matriz, informa dados, anexa documentos, executa a análise, revisa e valida resultados e gera o documento final. |
| Estudante | Beneficiário do aproveitamento. No fluxo documentado, não interage diretamente com o sistema; seus dados e documentos são informados pelo responsável. |

## Pré-condições

Antes de iniciar uma análise, o curso de destino e sua matriz curricular devem estar cadastrados; o estudante deve estar cadastrado ou ser informado no processo; o histórico escolar deve estar disponível; e o responsável deve ter acesso ao sistema.

## Regras de negócio

| ID | Regra |
|---|---|
| RN01 | A carga horária da disciplina de origem deve ser igual ou superior à carga horária da disciplina de destino. |
| RN02 | O conteúdo de origem deve apresentar aproximadamente 60% de compatibilidade com o conteúdo de destino, conforme o critério acadêmico definido para o projeto. |
| RN03 | A reprovação em uma disciplina não elimina automaticamente a possibilidade de análise; a situação acadêmica deve ser considerada. |
| RN04 | O resultado é uma possibilidade de equivalência e deve ser revisado pelo responsável pela análise curricular. |
| RN05 | O histórico escolar é obrigatório para realizar a análise. |
| RN06 | Os planos de ensino são opcionais e podem complementar a análise de compatibilidade dos conteúdos. |
| RN07 | Atender a apenas um critério não garante equivalência; os critérios definidos devem ser considerados em conjunto. |

O processamento automatizado ainda está em desenvolvimento. O sistema apoia a análise, mas não substitui a decisão acadêmica do responsável.

## Documentos

| Documento | Obrigatoriedade | Uso |
|---|---|---|
| Histórico escolar | Obrigatório | Identifica as disciplinas cursadas e seus dados acadêmicos. |
| Planos de ensino | Opcional | Complementam a avaliação de compatibilidade dos conteúdos. |

## Fluxo principal

| Etapa | Responsável | Ação |
|---:|---|---|
| 1 | Responsável | Acessa o EquivalencIA. |
| 2 | Responsável | Cadastra ou seleciona o estudante. |
| 3 | Responsável | Seleciona o curso e a matriz curricular de destino. |
| 4 | Responsável | Informa os dados acadêmicos. |
| 5 | Responsável | Anexa o histórico escolar obrigatório. |
| 6 | Responsável | Anexa planos de ensino, se disponíveis. |
| 7 | Responsável | Inicia a análise curricular. |
| 8 | Sistema | Compara disciplinas de origem com as disciplinas de destino. |
| 9 | Sistema | Verifica carga horária e compatibilidade de conteúdo. |
| 10 | Sistema | Apresenta possíveis equivalências. |
| 11 | Responsável | Revisa e valida os resultados. |
| 12 | Sistema | Gera o documento final da análise. |

### Casos de uso cobertos

O sistema permite cadastrar estudante, selecionar curso e matriz, informar dados acadêmicos, anexar documentos, realizar a análise, consultar resultados, validar equivalências e gerar o documento final. Durante a análise, inclui comparar disciplinas, verificar carga horária e verificar compatibilidade de conteúdo.

## Fluxos alternativos

| Situação | Comportamento esperado |
|---|---|
| Histórico escolar ausente | Impedir o início da análise e solicitar o documento obrigatório. |
| Plano de ensino ausente | Permitir continuar, pois o documento é opcional. |
| Carga horária insuficiente | Informar que a disciplina não atende ao critério de carga horária. |
| Compatibilidade de conteúdo insuficiente | Informar que a disciplina não atende ao critério de compatibilidade. |
| Dados obrigatórios ausentes | Solicitar o preenchimento dos campos pendentes. |
| Nenhuma equivalência identificada | Informar que não foram encontradas possíveis equivalências. |
| Possível equivalência identificada | Apresentar o resultado para revisão do responsável. |

## Exemplo de aplicação

Um estudante cursou **Algoritmos** (80 horas), com lógica de programação, algoritmos e estruturas condicionais, e solicita aproveitamento de **Pensamento Computacional** (80 horas), cujo conteúdo inclui pensamento lógico, algoritmos e resolução de problemas. A carga horária atende à RN01. A possibilidade de equivalência ainda depende da análise conjunta da compatibilidade dos conteúdos, conforme a RN02; o atendimento de um critério isolado não determina a aprovação.

## Estado do projeto

As regras descrevem o comportamento previsto e podem ser revisadas conforme as funcionalidades forem implementadas, testadas e validadas. Consulte a [página original no Confluence](https://edu-team-wv8ssvt9.atlassian.net/wiki/x/sAA3) para o contexto completo e o diagrama de casos de uso UML.
