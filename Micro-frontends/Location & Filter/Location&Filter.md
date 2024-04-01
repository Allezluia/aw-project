## Contexto e Problema

Um mecanismo que fornece uma barra de pesquisa ao utilizador, permitindo-lhe selecionar um supermercado específico, associado a uma determinada localização, que pode ser visualizada através da *API* do *Google Maps* e, por sua vez, outros supermercados próximos. Além disso, esta funcionalidade permite ainda selecionar uma dada categoria de carne, permitindo a visualização (e futuras operações) das diversas carnes disponíveis no mesmo.

Este mecanismo ajuda os utilizadores a encontrar produtos desejados com maior facilidade e conveniência, economizando tempo e esforço durante as compras.

## Decisão

Decidiu-se implementar um sistema de localização do supermercado utilizando a *API* do *Google Maps* como um *micro-frontend*, integrando ainda as categorias de carne disponíveis no supermercado selecionado, bem como os destaques da respectiva categoria selecionada.

## Justificações

Este *micro-frontend* com o *API* do *Google Maps* integrado **simplifica** a implementação da funcionalidade de localização, **reduzindo** a complexidade técnica e o tempo de desenvolvimento . Além disso, garante uma representação **precisa** das localizações dos supermercados e **facilita** a navegação para os utilizadores.

**Implementação independente:** Permite atualizações rápidas e pontuais, bem como a **reutilização**, sem afetar o funcionamento de outras áreas da *app*.

Uma **equipa dedicada** pode concentrar-se na melhoria e manutenção destas funcionalidades, tomando **decisões autónomas,** garantindo a sua eficácia.

**Serviços verticais:** A funcionalidade de localização está inerentemente ligada aos serviços relacionados a compras no supermercado. Ao integrarmos as categorias de carnes disponíveis no supermercado e os seus respectivos destaques, este *micro-frontend* oferece uma solução integrada e coesa, alinhada com a arquitetura vertical de serviços do projeto, permitindo um controlo detalhado e escalabilidade.

**Flexibilidade:** Permite ajustar e melhorar estas funcionalidades de forma independente, de forma a responder às necessidades, em constante mudança, do mercado e dos utilizadores.

## Task 2

<table>
  <tr>
    <th>Micro-frontends</th>
    <th>Views</th>
    <th>FE services</th>
  </tr>
  <tr>
    <td rowspan="18">Location & Filter</td>
    <td rowspan="5"><img src="./Location_1.png" alt="location_1" width="100" height="200"></td>
    <td>Search for Supermarket</td>
  </tr>
  <tr>
    <td>Display selected supermarket </td>
  </tr>
  <tr>
    <td>Display Featured Products </td>
  </tr>
   <tr>
    <td>Scroll Right And Left To See More Products </td>
  </tr>
   <tr>
    <td>Highlights Of A Specific Product </td>
  </tr>
    <td rowspan="3"><img src="./Location_2.png" alt="location_2" width="100" height="200"></td>
    <td>View Location on the map</td>
  </tr>
  <tr>
    <td>Product categorization</td>
  </tr>
  <tr>
    <td>Filtering Type of Product</td>
  </tr>
    <td rowspan="6"><img src="./Location_3.png" alt="product_3" width="100" height="200"></td>
    <td>View Location and Selected Category</td>
  </tr>
  <tr>
    <td>Highlights Of A Specific Product </td>
  </tr>
   <tr>
    <td>Display Highlights Product Details</td>
  </tr>
  <tr>
    <td>Scroll Right And Left To See More Highlights Product</td>
  </tr>
  <tr>
    <td>Display All Products</td>
  </tr>
  <tr>
    <td>Scroll Right And Left To See More Products</td>
  </tr>
</table>

