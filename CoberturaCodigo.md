# Cobertura de código #

A análise da cobertura de código é o processo de:
  * Procurar áreas do programa que não são exercitadas por um conjunto de casos de testes;
  * Criar casos de testes adicionais para melhorar a cobertura e determinar a medida quantitativa de cobertura de código que é uma medida indireta da qualidade;
  * Identificar casos de testes redundantes que não aumentam a cobertura de código;

A análise da Cobertura de Código é usada para garantir a qualidade do conjunto de testes, não a qualidade do produto.


The Premise

The basic assumptions behind coverage analysis tell us about the strengths and limitations of this testing technique. Some fundamental assumptions are listed below.

Bugs relate to control flow and you can expose Bugs by varying the control flow [p.60](Beizer1990.md). For example, a programmer wrote "if (c)" rather than "if (!c)".
You can look for failures without knowing what failures might occur and all tests are reliable, in that successful test runs imply program correctness [Morell1990](Morell1990.md). The tester understands what a correct version of the program would do and can identify differences from the correct behavior.
Other assumptions include achievable specifications, no errors of omission, and no unreachable code.
Clearly, these assumptions do not always hold. Coverage analysis exposes some plausible bugs but does not come close to exposing all classes of bugs. Coverage analysis provides more benefit when applied to an application that makes a lot of decisions rather than data-centric applications, such as a database application.