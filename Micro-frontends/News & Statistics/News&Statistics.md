## Contexto

Foi considerado uma funcionalidade que fornece aos utilizadores notícias relativamente à carne, como artigos em destaque, artigos na íntegra e outras notícias relacionadas com os mesmos.

Para além disso, fornece ainda a funcionalidade de estatísticas (negativas e positivas) acedidas através de um botão (no canto superior direito) na página de notícias. Esta funcionalidade disponibiliza informações acerca da carne desde 2021, como a percentagem de “área associada de desmatamento”, “produção animal”, “consumo médio de carne”, bem como quantas toneladas foram emitidas de metano e CO2eq, bem como a “quantidade de excrementos na água”, “químicos encontrados na água”, “uso de rações industriais” e “gado ao ar livre”.

**Problema**: Estes mecanismos visam suportar o cliente na sua tomada de decisões de compra, abordando questões como sustentabilidade, preferências alimentares e consumo responsável.

Além disso, oferece consciencialização ambiental, promovendo a transparência da empresa, ao divulgar informações sobre práticas de produção, consumo, qualidade da água, entre outros, permitindo aos utilizadores fazer escolhas mais conscientes e baseadas em informações sólidas.

## Alternativas consideradas (e motivo de não serem escolhidas)


***Third-Party:*** Utilização de um serviço externo/API para fornecer notícias e estatísticas sobre a carne, integrando esses dados diretamente na *app* sem a necessidade de desenvolver *micro-frontends* dedicados para essas funcionalidades.

## Decisão

Existe um botão na página das notícias que nos redireciona para as estatísticas, o que nos sugere que essas funcionalidades estão fortemente relacionadas, podendo ser tratadas como um único *micro-frontend* independente, dentro da arquitetura da aplicação.

## Justificações

Ter um *micro-frontend* específico para fornecer e gerir **notícias** e **estatísticas** **simplifica** a apresentação destas informações, de forma clara e direta, permitindo também a sua **reutilização** em diferentes partes da aplicação.

Correções ou atualizações podem ser **implementadas independentemente** de outros serviços, permitindo uma resposta mais ágil às necessidades dos utilizadores.

Uma **equipa dedicada** pode concentrar-se exclusivamente em manter e melhorar estas funcionalidades, garantindo a sua eficácia.

Este *micro-frontend* integrado permite maior **flexibilidade**, escalabilidade e personalização facilitando a adição de novas funcionalidades.
