# HO01 -- Respostas

1. **O que é um sistema de banco de dados (SBD)?**
    Um sistema de banco de dados é um conjunto de dados inter-relacionados somado aos softwares e estruturas utilizados para armazená-los, acessá-los e gerenciá-los.

2. **Do que um SBD é composto?**
    O sbd é composto de quatro componentes:
    **Dados**, o banco de dados em si
    **Hardware**, onde os dados sao armazenados fisicamente
    **software**, o SGBD e as aplicacoes
    **Usuarios**, pessoas ou sistemas que interagem com os dados

3. **Como usuarios e aplicacoes interagem com um SBD?**
    Por meio de interfaces de aplicações, programas ou executando comandos diretos utilizando linguagens de consulta(como o SQL).

4. **O que é um banco de dados (BD)?Cite um exemplo de um BD, indicando o link.**
    Um BD é uma colecao organizada de dados relacionados e com significado
        .Um exemplo é o catalogo do IMDB, que é um banco de dados de filmes
        .(anotacao); Ferramentas como o mysql, postgresql sao SGBDs(gerenciadores), enquanto o BD é a colecao de dados que eles guardam

5. **Quais sao as propriedades de um BD?**
    . Representa algum aspecto do mundo real (minimundo)
    . É logicamente coerente e possui significado
    . É projetado e populado com um propósito e públicos específicos

6. **Quais sao as etapas de um projeto de BD?**
    . Levantamento e análise de requisitos
    . Projeto conceitual
    . Projeto lógico
    . Projeto físico

7. **O que é um gerenciador de banco de dados (SGBD)?**
    É o software (como mysql, postgresql, oracle) que serve como interface para criar, manter e gerenciar o acesso aos dados do BD de forma pratica e segura.

8. **Quais sao as propriedades de um SGBD?**
    Controle de redundancia, restricao de acesso(seguranca), garantia de integridade, controle de concorrencia(multiplos acessos simultaneos) e facilidade de backup/recuperacao

9. **Indique situacoes em que o uso de SGBD pode se mostrar inadequado**
    Quando a aplicacao é extremamente simples e nao sofrera mudancas, ou quando o sistema tem restricoes rigorosas de hardware(sistemas embarcados limitados) e exige tempo de resposta de tempo real onde o "peso" extra so SGBD atrapalharia

10. **O que é um modelo de dados?**
    Modelo de dados é um conjunto de ferramentas conceiturais( regras e simbolos) usadas para descrever a estrutura do banco, os tipos de dados, os relacionamentos e as restricoes

11. **Em relacao ao nivel de abstracao, quais sao os tipos de modelos de dados?**
    . Conceitual: alto nivel, focado em como o usuario enxerga o negocio
    . Logico (ou representacional): Medio nivel, focado na estrutura que o SGBD vai usar (ex: tabelas relacionais)
    . Fisico: Baixo nivel, focado em como o dado é gravado no hardware

12. **O que é um Esquema de BD?**
    É a estrutura (metadados) do banco de dados(ex: quais sao as tabelas e as colunas). Ele é estatico e raramente muda

13. **O que é uma instancia de BD?**
    É o conteudo real do banco de dados em um momento especifico. A instancia muda constantemente a cada nova insercao, atualizacao ou exclusao

14. **Quais as vantagens de se adotar uma Arquitetura de Tres esquemas para implementar um BD?**
    A principal vantagem é garantir a **independencia de dados**, alem de permitir multiplas visoes do mesmo banco para diferentes tipos de usuarios sem expor tudo a todos.

15. **Quais niveis existem em uma Arquitetura de Tres esquemas?**
    . Nivel extremo(visao): Descreve apenas a parte do banco que interessa a um grupo de usuarios, ocultando o restante
    . Nivel conceitual: descreve a estrutura logica de todo o banco de dados(entidades, relacionamentos, restricoes)
    . Nivel interno: descreve o armazenamento fisico e os caminhos de acesso no/aos hardware/dados

16. **O que é um mapeamento em uma arquitetura de tres esquemas?**
    É o processo de traducao que o SGBD faz entre os niveis(ex:traduzir a requisicao da visao externa do usuario para encontrar  o dado fisico no nivel interno)

17. **O que é Independencia de dados e qual sua importancia para um SBD?**
    É a capacidade de alterar a estrutura de um nivel inferior sem quebrar o nivel superior. Sua importancia esta em permitir atualizacoes no banco(como adicionar campos ou mudar o disco fisico) sem precisar reescrever o codigo das aplicacoes que o utilizam

18. **O que é uma li