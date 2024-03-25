## Contexto

A aplicação deve incluir um Perfil, associado ao utilizador que está autenticado, que lhe permite aceder e gerir as suas informações pessoais, tais como foto de perfil, *email*, nome de utilizador, entre outros. Além disso, fornece acesso às definições da app para configuração e personalização, bem como o contacto da empresa.

**Problema**: Não existir uma forma conveniente de visualizar e editar as informações do seu perfil, poderia resultar numa experiência menos satisfatória, intuitiva e eficiente do utilizador, podendo afetar a experiência geral do mesmo.

## Alternativas consideradas (e motivo de não serem escolhidas)

Manter o *micro-frontend d*o perfil separada, sem integração com o *micro-frontend* do *login*. Isto teria aumentado a complexidade da implementação e poderia resultar em problemas de consistência e sincronização de dados.

## Decisão

Decidiu-se implementar o Perfil do utilizador como um *micro-frontend* integrado no *micro-frontend* do *login* existente.

## Justificações

Ter um *micro-frontend* para gerir o **perfil** do cliente/utilizador **simplifica** a navegação para os utilizadores, fornecendo-lhes uma experiência direta e coesa.

A integração do perfil no *micro-frontend* de *login* permite a **implementação independente** e a **reutilização**  eficiente de componentes de interface do utilizador relacionados à autenticação e ao perfil, reduzindo a carga de manutenção e facilitando a evolução contínua da aplicação.

Este *micro-frontend* tem a **responsabilidade única** de gerir e exibir as informações do perfil do utilizador (referido anteriormente, na seção contexto), mantendo-o focado e coeso.

Uma **equipa dedicada** pode focar-se em projetar, melhorar e manter esta funcionalidade, tomando decisões autónomas e assim, garantindo a sua eficácia e coesão dentro da arquitetura da aplicação.

**Serviços verticais:** ??

Este *micro-frontend* integrado permite maior **flexibilidade** e escalabilidade, facilitando a adição de novas funcionalidades.
