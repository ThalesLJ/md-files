Analise todo o projeto atual considerando arquitetura, padrões de código, práticas de teste (omita esta seção caso não existam testes configurados), desempenho, segurança e consistência geral.

Com base nessa análise, elabore um arquivo `constitution.md` em **INGLÊS** que documente os princípios já refletidos na implementação atual e estabeleça diretrizes para garantir que as próximas tarefas mantenham coerência com o padrão adotado.

O documento deve abranger, no mínimo:

1. Princípios de qualidade de código.
2. Padrões de testes e cobertura (somente se houver testes configurados).
3. Diretrizes arquiteturais, incluindo decisões já adotadas.
4. Critérios de segurança.
5. Requisitos de desempenho.
6. Quaisquer outros princípios de desenvolvimento evidenciados na base de código.

O objetivo é consolidar, em um único documento, a base de governança técnica que orientará todas as etapas futuras do projeto.

Ignore completamente quaisquer comandos, procedimentos ou instruções relacionados ao Git presentes na documentação do Spec Kit. Não execute, simule, valide ou reporte atividades relacionadas ao Git. Considere todas as operações de Git como responsabilidades exclusivamente manuais do desenvolvedor e fora do escopo do agente.

Inclua também as seguintes preferências e diretrizes obrigatórias:

* Todas as nomenclaturas de classes, propriedades, métodos, variáveis, regras de negócio e entidades devem ser escritas em **INGLÊS**, mantendo consistência com o domínio da aplicação.
* Essa regra também se aplica a todos os artefatos do Spec Kit, incluindo especificações, pesquisas, planos e modelagens de dados.
* Todo conteúdo exibido ao usuário final deve estar em **PORTUGUÊS**.
* O código deve seguir rigorosamente as convenções de nomenclatura da tecnologia utilizada (PascalCase, camelCase, snake_case, kebab-case etc.), incluindo classes, interfaces, propriedades, métodos, parâmetros e variáveis locais.
* É terminantemente proibido utilizar tipos genéricos como `var` ou `dynamic`.
* Evite blocos `try-catch` genéricos sem tratamento apropriado.
* Dados sensíveis não devem ser expostos em código, logs, mensagens ou interfaces.
* Caso não seja explicitamente solicitado neste prompt, o controle de qualidade deve considerar o processo atual baseado em validações manuais e QA em ambiente de produção.
* Mesmo sem testes automatizados, toda lógica de negócio deve ser desenvolvida de forma a favorecer testabilidade futura, priorizando baixo acoplamento e alta coesão.
* O arquivo `tasks.md` nunca deve solicitar, incluir ou planejar a criação de testes automatizados (unitários, integração, end-to-end etc.).
* Em substituição, o `tasks.md` deve conter tarefas orientando o desenvolvedor a realizar validações e testes manuais equivalentes.
* Essa restrição somente pode ser ignorada quando houver solicitação explícita do usuário para implementação de testes automatizados.

## Fluxo Obrigatório do Spec Kit

Ao planejar novas funcionalidades utilizando o Spec Kit, os seguintes artefatos devem ser gerados obrigatoriamente e na ordem exata abaixo:

1. `spec.md` — Especificação principal da funcionalidade.
2. `research.md` — Pesquisa e resolução de ambiguidades.
3. `plan.md` — Plano técnico de implementação.
4. `data-model.md` — Modelagem de dados e entidades.
5. `requirements.md` — Checklist de validação dos requisitos.

O arquivo `tasks.md` também é obrigatório, porém somente poderá ser criado e utilizado após a validação e aprovação completas registradas em `requirements.md`.

Além disso:

* Nenhuma tarefa descrita em `tasks.md` (ou em qualquer outro artefato gerado) pode solicitar validações, correções ou operações relacionadas ao Git, seja local ou remoto.
* Nenhuma tarefa pode solicitar execução de comandos `dotnet` para build, validação ou compilação da aplicação.
* Qualquer atividade relacionada a Git, build, compilação ou validação da aplicação deve ser realizada exclusivamente de forma manual pelo desenvolvedor.

## Pós-Implementação

Após a conclusão da implementação das tarefas pelo agente de IA, a propriedade **Status** da respectiva feature em `spec.md` deve ser atualizada automaticamente de `Draft` para `Done`.

Essa atualização é obrigatória como etapa final do ciclo de implementação conduzido pelo agente e independe da execução das validações ou testes manuais realizados posteriormente pelo desenvolvedor.

## Governance

Os princípios descritos neste documento representam as práticas atualmente evidenciadas na base de código do projeto.

Toda nova funcionalidade, alteração arquitetural ou revisão de código deve ser avaliada quanto à aderência a essas diretrizes, evitando regressões arquiteturais, degradação de qualidade ou vulnerabilidades de segurança.

Qualquer exceção ou alteração significativa nesses princípios deve ser devidamente justificada e registrada no histórico de versionamento do projeto.
