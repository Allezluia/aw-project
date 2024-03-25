## Contexto

Foi considerado um mecanismo que permite aos utilizadores gerir e "salvar" os produtos que desejam manter como favoritos, para posterior visualização ou compra. Com efeito, é guardada uma lista dos produtos guardados (marcados como favoritos), sendo apresentadas as informações relevantes acerca dos mesmos.
Para além disso, temos também um mecanismo que permite ao utilizador dar *feedback*, de 1 a 5 estrelas, relativamente a um produto.

Estes mecanismos visam solucionar o facto dos utilizadores não possuírem uma forma prática de salvar os produtos para posterior revisão/compra e ajuda a empresa a perceber as preferências dos clientes. Também fornece aos utilizadores uma maneira de tomar decisões conscientes nas suas compras com base nas avaliações de outros utilizadores (neste caso, no rating do produto).

## Alternativas consideradas (e motivo de não serem escolhidas)
??

## Decisão

Decidimos considerar o mecanismo de favoritos e *feedback* como um único *micro-frontend*, devido à forte interligação entre estas funcionalidades. A própria *app* sugere que *“é recomendado salvar o produto para mais tarde contribuir com o respetivo feedback”*, ou seja, os utilizadores são incentivados a “salvar” produtos como favoritos para, mais tarde, contribuírem com uma avaliação.

## Justificações

Ter um *micro-frontend* para gerir e “**salvar**” **favoritos** produtos  e que permite dar **feedback** dos mesmos, proporciona uma abordagem mais simples e direta de gerir estas funcionalidades, promovendo também a sua fácil **reutilização** em diferentes partes do sistema.

Ao ter um *micro-frontend*  dedicado aos favoritos e *feedback*, garantimos uma **responsabilidade única**, facilitando a compreensão e manutenção destas funcionalidades.

Correções ou atualizações podem ser **implementadas independentemente** de outros serviços, permitindo uma implementação mais ágil e segura, sem afetar outras partes da aplicação.

Uma **equipa dedicada** pode concentrar-se em manter e melhorar estas funcionalidades, garantindo que atenda às necessidades dos utilizadores de forma eficiente.

**Serviços verticais:** Alinha-se com a arquitetura vertical de serviços do projeto, permitindo um controlo detalhado e escalabilidade.

**Flexibilidade:** Permite modificar e melhorar estas funcionalidades de forma independente, conforme necessário, sem afetar outras partes do sistema.
