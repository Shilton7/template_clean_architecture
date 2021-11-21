<h1 align="center">Clean Architecture</h1>

<p align="center">
  <a href="#-">Problema</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-">Solução</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-">Clean Architecture</a>&nbsp;&nbsp;&nbsp;
</p>

## 🔥 Problema

Quando criamos projetos usando o template padrão, estamos usando uma arquitetura simples conhecida como monolítica, onde temos toda codificação em um único projeto. </br></br>
Na arquitetura monolítica criamos várias pastas a fim de organizar o código, mas isso traz grandes problemas de responsabilidades à medida que o projeto vai crescendo, como regras de negócio espalhadas em pastas distintas, forte acoplamento entre os componentes do projeto (interface UI, lógica de acesso a dados, ferramentas ORM, frameworks e suas dependências). </br></br>
O projeto que faz uso dessa arquitetura, à medida que cresce se torna cada vez mais difícil de ser mantido, atualizado, testado, estendido e tem alto custo de infra no quesito ligado a escalabilidade. </br></br>
O uso do template padrão (arquitetura monolítica) é indicado para projetos de estudos, testes pequenos, criação de protótipos e POC's.


## 🚀 Solução

Para solução do item citado acima, precisamos definir o uso de uma arquitetura robusta e principalmente DESACOPLADA, onde conseguimos criar projetos distintos dessa forma separando as responsabilidades.
Outro ponto importante seria usarmos a inversão de controle e a injeção de dependência (DI).
A implementação desses torna o projeto testável, escalável e mais fácil de se atualizar. </br></br>
Opções arquiteturais: </br>
✅ Arquitetura de três camadas (tiers); </br>
✅ Arquitetura Cebola (Onion Architecture); </br>
✅ Arquitetura Limpa (Clean Architecture); </br>
✅ Arquitetura Hexagonal (Ports and Adapters);


## 💻 Clean Architecture (Arquitetura Limpa)

Nessa arquitetura a regra de dependência aplicada consiste em que as camadas internas não devem ter qualquer dependência das externas e nem indiretas (termos, funções ou nomes de variáveis).
Ela possui características de testável, independência de Frameworks, Camada de apresentação e DB.

<img src="https://miro.medium.com/max/800/1*0R0r00uF1RyRFxkxo3HVDg.png" height="350" width="600"/>

**Divisão das responsabilidades por projeto:** </br>
✅ Domain: Modelo de domínio, Interfaces (repositories), Regras de Negócio. </br>
✅ Application: DTOs, Regras da aplicação (Services), Mapeamentos e Interfaces (services). </br>
✅ Infrastructure: Contexto DB, ORM, Lógica de acesso a dados (Repositories). </br>
✅ CrossCutting: Registro de serviços (DI). </br>
✅ API: Interface Web (Endpoints, Controlladores) </br>

**Layout do template  no Microsoft Visual Studio:** </br>
<img src="https://i.imgur.com/2bBIQgI.png" height="400" width="400"/>
