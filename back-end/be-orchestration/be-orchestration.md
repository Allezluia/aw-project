# Task 9 : BE - ORCHESTRATION

O Feedback Service pode necessitar orquestrar com o Profile Service para associar avaliações a utilizador autenticados e com o Product Service para associar avaliações a produtos.

## Fluxo
1. Utilizador envia avaliação para o Orquestrador.
2. Orquestrador valida a autenticação do utilizador através do Profile Service.
3. Orquestrador registra a avaliação no Feedback Service.
4. Orquestrador atualiza a média de avaliações no Product Service.
5. Orquestrador retorna confirmação ao utilizador.

A implementação de um orquestrador para o Feedback Service garante que todas as etapas do processo de avaliação sejam gerenciadas de forma eficiente e segura, proporcionando uma experiência de utilizador suave e consistente.


<table>
  <tr>
        <th>BE Services</th>
        <th>Request</th>
        <th>Request Schemas</th>
        <th>Response Schemas</th>
    </tr>
  <tr>
        <td rowspan="3">Feedback Service</td>
        <td>GET /products/{product_id}/feedback</td>
        <td></td>
        <td><pre>
            tags:
        - "Feedback Service"
      summary: "Search products's feedback by product id"
      parameters:
        - $ref: "#/components/parameters/product_id"
      responses:
        "200":
          description: "Successfully found products's feedback by product id"
          content:
            application/json:
              schema:
                type: "array"
                items:
                  $ref: '#/components/schemas/Feedback'
        "404":
          description: "Product's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>PUT /products/{product_id}/feedback</td>
        <td><pre>
            tags:
        - "Feedback Service"
      summary: "Add new feedback to product"
      parameters:
        - $ref: "#/components/parameters/product_id"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Feedback'
        </pre></td>
        <td><pre>
            responses:
        "200":
          description: "Successfully added feedback"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Feedback'
        </pre></td>
    </tr>
    <tr>
        <td>GET /products/{product_id}/feedback/{feedback_id}</td>
        <td></td>
        <td><pre>
            get:
      tags:
        - "Feedback Service"
      summary: "Search feedback by feedback id"
      parameters:
        - $ref: "#/components/parameters/product_id"
        - $ref: "#/components/parameters/feedback_id"
      responses:
        "200":
          description: "Successfully found feedback by feedback id"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Feedback'
        "404":
          description: "Product's or Feedback's id not found"
        </pre></td>
    </tr>
    
</table>
