# Task 9

<table>
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
