# Task 9 : BE - ORCHESTRATION

O Rating Service pode necessitar orquestrar com o Profile Service para associar avaliações a utilizador autenticados e com o Product Service para associar avaliações a produtos.

## Fluxo
1. Utilizador envia avaliação para o Orquestrador.
2. Orquestrador valida a autenticação do utilizador através do Profile Service.
3. Orquestrador registra a avaliação no Rating Service.
4. Orquestrador atualiza a média de avaliações no Product Service.
5. Orquestrador retorna confirmação ao utilizador.

A implementação de um orquestrador para o Rating Service garante que todas as etapas do processo de avaliação sejam gerenciadas de forma eficiente e segura, proporcionando uma experiência de utilizador suave e consistente.


<table>
  <tr>
        <th>BE Services</th>
        <th>Request</th>
        <th>Request Schemas</th>
        <th>Response Schemas</th>
    </tr>
  <tr>
        <td rowspan="3">Rating Service</td>
        <td>GET /products/{product_id}/ratings</td>
        <td></td>
        <td><pre>
            tags:
        - "Rating Service"
      summary: "Search products's ratings by product id"
      parameters:
        - $ref: "#/components/parameters/product_id"
      responses:
        "200":
          description: "Successfully found products's ratings by product id"
          content:
            application/json:
              schema:
                type: "array"
                items:
                  $ref: '#/components/schemas/Rating'
        "404":
          description: "Product's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>PUT /products/{product_id}/ratings</td>
        <td><pre>
            tags:
        - "Rating Service"
      summary: "Add new rating to product"
      parameters:
        - $ref: "#/components/parameters/product_id"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Rating'
        </pre></td>
        <td><pre>
            responses:
        "200":
          description: "Successfully added rating"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Rating'
        </pre></td>
    </tr>
    <tr>
        <td>GET /products/{product_id}/ratings/{rating_id}</td>
        <td></td>
        <td><pre>
            get:
      tags:
        - "Rating Service"
      summary: "Search rating by rating id"
      parameters:
        - $ref: "#/components/parameters/product_id"
        - $ref: "#/components/parameters/rating_id"
      responses:
        "200":
          description: "Successfully found rating by rating id"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Rating'
        "404":
          description: "Product's or Rating's id not found"
        </pre></td>
    </tr>
    
</table>
