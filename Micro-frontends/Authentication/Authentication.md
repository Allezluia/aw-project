## Contexto e Problema

É necessário um mecanismo de autenticação para a aplicação. Sem este, a gestão das credenciais do utilizador apresenta potenciais riscos de segurança, incluindo o acesso não autorizado e/ou violação de dados.

## Alternativas consideradas (e motivo de não serem escolhidas)

**Abordagem monolítica:** Implica que todas as funcionalidades da aplicação estariam integradas e implementadas como uma única unidade de *software,* o que resultaria na falta de modularidade e escalabilidade.

**Third-party:** Poderiam limitar a personalização e o controlo do *login/registo*.

## Decisão
Decidiu-se implementar o sistema de *login/registo* como um *micro-frontend* independente dentro da arquitetura da aplicação.

## Justificações

Ter um *micro-frontend* dedicado ao *login* e *registo* **simplifica** o código, uma vez que separa as funcionalidades de autenticação do restante da aplicação, promovendo a sua **reutilização** facilmente em diferentes partes do sistema, ao encapsulá-las num *micro-frontend.*

Este *micro-frontend* tem a **responsabilidade única** de lidar com a autenticação de usuários, mantendo-o focado e coeso.

Uma vez que, a autenticação é uma funcionalidade crítica, ter um *micro-frontend* separado, permite-nos atualizá-lo **independentemente** de outros serviços, garantindo **implementações** rápidas e seguras.

Uma **equipa dedicada** pode concentrar-se em melhorar e manter a funcionalidade do *login/registo*, tomando **decisões autónoma**s, garantindo a sua eficácia e segurança.

**Serviços verticais:** Alinha-se com a arquitetura vertical de serviços do projeto, permitindo um controlo detalhado e escalabilidade.


**Flexibilidade:** Permite ajustar e melhorar estas funcionalidades de forma independente, respondendo rapidamente a mudanças nos requisitos ou no ambiente.

## Task 2

<table>
    <tr>
        <td>Micro-Frontend</td>
        <td>View</td>
        <td>FE Service</td>
    </tr>
    <tr>
        <td rowspan="9">Authentication</td>
        <td rowspan="9"><img src="./Authentication.png" alt="Authentication" width="100" height="200"></td>
    <td>LoginUser</td></tr>
    <tr><td>RegisterUser</td></tr>
    <tr><td>AuthenticateUser</td></tr>
    <tr><td>VerifyUser</td></tr>
    <tr><td>ResetPassword</td></tr>
    <tr><td>GenerateAuthToken</td></tr>
    <tr><td>InvalidateAuthToken</td></tr>
    <tr><td>SendVerificationEmail</td></tr>
    <tr><td>SendPasswordResetEmail</td></tr>
</table>

