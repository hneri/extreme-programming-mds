# Integração Contínua #

É uma das práticas da [eXtreme Programming](XP.md) na qual o código é integrado e testado continuamente após algumas horas - no máximo um dia de desenvolvimento.
Tecnicamente, o termo "Integração Contínua" significa que todos do time integram as suas mudanças no repositório frequentemente, verificando se com as mudanças feitas os testes continuam passando 100%. A definição e configuração exata para a Integração Contínua depende do time que deve definir como e com qual frequência a integração deverá ser feita. Aqui será discutida a Integração Contínua de forma automatizada.

“Integração Contínua é uma pratica de desenvolvimento de software onde os membros de um time integram seu trabalho frequentemente, geralmente cada pessoa integra pelo menos diariamente – podendo haver multiplas integrações por dia. Cada integração é verificada por um build automatizado (incluindo testes) para detectar erros de integração o mais rápido possível. Muitos times acham que essa abordagem leva a uma significante redução nos problemas de integração e permite que um time desenvolva software coeso mais rapidamente.” ([Martin Fowler](http://martinfowler.com/))

Basicamente, a grande vantagem da Integração Contínua está no feedback instantâneo. Isso funciona da seguinte forma: a cada commit no repositório, o build é feito automaticamente, com todos os testes sendo executados de forma automática e falhas sendo detectadas. Se algum commit não compilar ou quebrar qualquer um dos testes, a equipe toma conhecimento instantaneamente (através de email, por exemplo, indicando as falhas e o commit causador das mesmas). A equipe pode então corrigir o problema o mais rápido possível, o que é fundamental para não introduzir erros ao criar novas funcionalidades, refatorar, etc. Integração Contínua é mais uma forma de trazer segurança em relação a mudanças: você pode fazer modificações sem medo, pois será avisado caso algo saia diferente do esperado.


---

## Integração Contínua Síncrona ##

Apenas um par integra seu trabalho de cada vez e outros pares só são liberados para integrar ao serem informados do término da integração corrente. Mas não são todos os projetos que podem usar esse modelo de integração, pois ele exige que os desenvolvedores trabalhem juntos, normalmente em uma mesma sala. Desse modo se pode garantir que apenas um par integre de cada vez, utilizando-se um computador dedicado à integração, por exemplo.

## Integração Contínua Assíncrona ##

Projetos nos quais os desenvolvedores não trabalhem juntos em uma mesma sala, como por exemplo a maioria dos projetos open source, não comportam a utilização do modelo de integração síncrona, pois em tais casos torna-se difícil ou impossível garantir que apenas um desenvolvedor irá integrar de cada vez. Nessas situações, o modelo assíncrono de integração contínua é mais apropriado.

Nesse modelo, o desenvolvedor integra seu código, executando um subconjunto dos passos descritos anteriormente:

  1. Assegurar que o projeto compila e todos os testes automatizados executam com sucesso
  1. Criar um backup do projeto na estação de trabalho
  1. Fazer update do projeto
  1. Assegurar que o software continua compilando e os testes executam com sucesso
  1. Fazer commit do projeto

Depois disso, uma ferramenta de apoio à integração contínua assíncrona, como o [Cruise Control](CruiseControl.md), monitora o repositório permanentemente. Sempre que detecta mudanças (porque alguém fez um commit), o [Cruise Control](CruiseControl.md) faz checkout de todo o projeto automaticamente, pode usar, como exemplo, o [Maven](Maven.md) para gerenciar o build do projeto e executar todos os testes. Quando ocorre algum erro de compilação, de merge ou na execução dos testes, a ferramenta envia um e-mail para o desenvolvedor responsável pelo problema. O desenvolvedor, por sua vez, deve fazer as correções o mais brevemente possível e colocá-las no repositório.


---

## Processo de Integração Contínua ##

![http://siep.ifpe.edu.br/anderson/blog/wp-content/uploads/2010/08/Processo_de_IC.jpg](http://siep.ifpe.edu.br/anderson/blog/wp-content/uploads/2010/08/Processo_de_IC.jpg)

O cenário acima pode ser descrito como:
  1. O desenvolvedor envia o código para o controle de versão (SVN, CVS, etc). Enquanto isso a máquina de integração (servidor de Integração Contínua) está verificando o repositório buscando por modificações
  1. Logo após um commit ser efetuado, o servidor ao verificar que alguma mudança ocorreu no repositório inicia o processo de build baixando os arquivos do Servidor de Controle de Versão. Assim, o script de build é executado, testes são realizados, relatórios gerados, e todo o projeto é integrado.
  1. O Servidor de Integração envia por e-mail ou outros dispositivos o feedback sobre build para usuários específicos do projeto
  1. O servidor volta ao estado de Poll buscando por mudanças no repositório

---

# Referências #

  1. [Continuous Integration, Martin Fowler](http://martinfowler.com/articles/continuousIntegration.html)
  1. [Integração Contínua, Caelum](http://blog.caelum.com.br/integracao-continua/)
  1. [Integração Contínua, ImproveIT](http://improveit.com.br/xp/praticas/integracao)
  1. [Continuous Integration: Improving Software Quality and Reducing Risk, Paul M. Duvall, Steve Matyas, Andrew Glover](http://www.amazon.com/gp/product/0321336380?ie=UTF8&tag=martinfowlerc-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0321336380)
  1. [Beck, Kent. Programação Extrema Explicada: Acolha as mudanças. Bookman, 2004.](http://books.google.com.br/books?id=xWWPkGLIuxMC&printsec=frontcover&hl=pt-BR#v=onepage&q&f=false)