# Task 8 : BE - BUSINESS-OBJECTS
<table>
    <tr>
        <th>BE Services</th>
        <th>Request</th>
        <th>Request Schemas</th>
        <th>Response Schemas</th>
    </tr>
    <tr>
        <td rowspan="4">Profile Service</td>
        <td>POST /profiles</td>
        <td><pre>
            tags:
        - "Profile Service"
      summary: "Create new profile"
      responses:
        "201":
          description: "Successfully created new profile"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Profile'
        </pre></td>
        <td><pre>
            tags:
        - "Profile Service"
      summary: "Create new profile"
      responses:
        "201":
          description: "Successfully created new profile"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Profile'
        </pre></td>
    </tr>
    <tr>
        <td>GET /profiles</td>
        <td></td>
        <td><pre>
            tags:
        - "Profile Service"
      summary: "Search profiles"
      responses:
        "200":
          description: "Successfully found profiles"
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Profile'
        </pre></td>
    </tr>
    <tr>
        <td>GET /profiles/{profile_id}</td>
        <td></td>
        <td><pre>
      tags:
        - "Profile Service"
      summary: "Search profile by id"
      parameters:
        - $ref: "#/components/parameters/profile_id"
      responses:
        "200":
          description: "Successfully found profile by id"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Profile'
        "404":
          description: "Profile's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>PUT /profiles/{profile_id}</td>
        <td><pre>
      tags:
        - "Profile Service"
      summary: "Update profile by id"
      parameters:
        - $ref: "#/components/parameters/profile_id"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Profile'
        </pre></td>
        <td><pre>
      responses:
        "200":
          description: "Successfully updated profile by id"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Profile'
        "404":
          description: "Profile's id not found"
        </pre></td>
    </tr>
    <!-------- Supermarket Service ------->
    <tr>
        <td rowspan="5">Supermarket Service</td>
        <td>GET /supermarkets/{supermarket_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "Supermarket Service"
      summary: "Search supermarket by id"
      parameters:
        - $ref: "#/components/parameters/supermarket_id"
      responses:
        "200":
          description: "Successfully found supermarket"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Supermarket'
        "404":
          description: "Supermarket's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>PUT /supermarkets/{supermarket_id}</td>
        <td><pre>
            tags:
        - "Supermarket Service"
      summary: "Update supermarket by id"
      parameters:
        - $ref: "#/components/parameters/supermarket_id"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Supermarket'
        </pre></td>
        <td><pre>
            responses:
        "200":
          description: "Successfully updated supermarket"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Supermarket'
        "404":
          description: "Supermarket's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>DELETE /supermarkets/{supermarket_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "Supermarket Service"
      summary: "Delete supermarket by id"
      parameters:
        - $ref: "#/components/parameters/supermarket_id"
      responses:
        "200":
          description: "Successfully removed supermarket"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Supermarket'
        "404":
          description: "Supermarket's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>GET /supermarkets</td>
        <td></td>
        <td><pre>
            responses:
        "200":
          description: "Successfully found supermarkets"
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Supermarket'
        </pre></td>
    </tr>
    <tr>
        <td>POST /supermarkets</td>
        <td><pre>
            tags:
        - "Supermarket Service"
      summary: "Create new supermarket"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Supermarket'
        </pre></td>
        <td><pre>
            responses:
        "201":
          description: "Successfully created new supermarket"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Supermarket'
        </pre></td>
    </tr>
    <!-------- Product Service ------->
    <tr>
        <td rowspan="5">Product Service</td>
        <td>POST /products</td>
        <td><pre>
            tags:
        - "Product Service"
      summary: "Create new product"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Product'
        </pre></td>
        <td><pre>
            responses:
        "201":
          description: "Successfully created new product"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Product'
        </pre></td>
    </tr>
    <tr>
        <td>GET /products</td>
        <td></td>
        <td><pre>
            get:
      tags:
        - "Product Service"
      summary: "Search products"
      responses:
        "200":
          description: "Successfully found products"
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Product'
        </pre></td>
    </tr>
    <tr>
        <td>GET /products/{product_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "Product Service"
      summary: "Search product by id"
      parameters:
        - $ref: "#/components/parameters/product_id"
      responses:
        "200":
          description: "Successfully found product"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Product'
        "404":
          description: "Product's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>DELETE /products/{product_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "Product Service"
      summary: "Delete product by id"
      parameters:
        - $ref: "#/components/parameters/product_id"
      responses:
        "200":
          description: "Successfully remove product"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Product'
        "404":
          description: "Product's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>PUT /products/{product_id}</td>
        <td><pre>
            tags:
        - "Product Service"
      summary: "Update product by id"
      parameters:
        - $ref: "#/components/parameters/product_id"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Product'
        </pre></td>
        <td><pre>
            responses:
        "200":
          description: "Successfully updated product"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Product'
        "404":
          description: "Product's id not found"
        </pre></td>
    </tr>
    <!------ Category Service -------->
    <tr>
        <td rowspan="4">Category Service</td>
        <td>POST /categories</td>
        <td><pre>
            tags:
        - "Category Service"
      summary: "Create new category"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Category'
        </pre></td>
        <td><pre>
            responses:
        "201":
          description: "Successfully created new category"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Category'
        </pre></td>
    </tr>
    <tr>
        <td>GET /categories</td>
        <td></td>
        <td><pre>
            tags:
        - "Category Service"
      summary: "Search categories"
      responses:
        "200":
          description: "Successfully found categories"
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Category'
        </pre></td>
    </tr>
    <tr>
        <td>GET /categories/{category_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "Category Service"
      summary: "Search category by id"
      parameters:
        - $ref: "#/components/parameters/category_id"
      responses:
        "200":
          description: "Successfully found category"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Category'
        "404":
          description: "Category's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>DELETE /categories/{category_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "Category Service"
      summary: "Delete category by id"
      parameters:
        - $ref: "#/components/parameters/category_id"
      responses:
        "200":
          description: "Successfully removed category"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Category'
        "404":
          description: "Category's id not found"
        </pre></td>
    </tr>
    <!------ News Service -------->
    <tr>
        <td rowspan="2">News Service</td>
        <td>GET /news</td>
        <td></td>
        <td><pre>
            tags:
        - "News Service"
      summary: "Search recent news"
      responses:
        "200":
          description: "Successfully got recent news"
          content:
            application/json:
              schema:
                type: "array"
                items:
                  $ref: '#/components/schemas/News'
        </pre></td>
    </tr>
    <tr>
        <td>GET /news/{news_id}</td>
        <td></td>
        <td><pre>tags:
        - "News Service"
      summary: "Get news by id"
      parameters:
        - $ref: "#/components/parameters/news_id"
      responses:
        "200":
          description: "Successfully found news by id"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/News'
        "404":
          description: "News' id not found"</pre></td>
    </tr>
     <!------ Statistics Service -------->
    <tr>
        <td rowspan="1">Statistics Service</td>
        <td>GET /statistics</td>
        <td></td>
        <td><pre>
            tags:
        - "Statistics Service"
      summary: "Get updated statistics"
      responses:
        "200":
          description: "Successfully got recent statistics"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Statistics'
        </pre></td>
    </tr>
     <!------ Favourite Products Service -------->
    <tr>
        <td rowspan="3">Favourite Products Service</td>
        <td>GET /profiles/{profile_id}/favourite-products</td>
        <td></td>
        <td><pre>
            tags:
        - "Favourite Products Service"
      summary: "Search favourite products by profile id"
      parameters:
        - $ref: "#/components/parameters/profile_id"
      responses:
        "200":
          description: "Successfully found favourite products by profile id"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Favourite_products'
        "404":
          description: "Profile's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>PUT /profiles/{profile_id}/favourite-products</td>
        <td><pre>
            tags:
        - "Favourite Products Service"
      summary: "Add new favourite product to profile"
      parameters:
        - $ref: "#/components/parameters/profile_id"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Favourite_products'
        </pre></td>
        <td><pre>
            responses:
        "200":
          description: "Successfully created new category"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Favourite_products'
        </pre></td>
    </tr>
    <tr>
        <td>DELETE /profiles/{profile_id}/favourite-products/{product_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "Favourite Products Service"
      summary: "Remove favourite product from profile"
      parameters:
        - $ref: "#/components/parameters/profile_id"
        - $ref: "#/components/parameters/product_id"
      responses:
        "200":
          description: "Successfully remove favourite product from profile"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Favourites_products'
        "404":
          description: "Profile's or Product's id not found"
        </pre></td>
    </tr>
    <!------ Supermarket Categories Service -------->
    <tr>
        <td rowspan="4">Supermarket Categories Service</td>
        <td>GET /supermarkets/{supermarket_id}/categories/{category_id}/products</td>
        <td></td>
        <td><pre>
            tags:
        - "Supermarket Categories Service"
      summary: "Search supermarket's products by supermarket id"
      parameters:
        - $ref: "#/components/parameters/supermarket_id"
        - $ref: "#/components/parameters/category_id"
      responses:
        "200":
          description: "Successfully found supermarket's products by supermarket id"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Supermarket_categories'
        "404":
          description: "Supermarket' or Category's not found"
        </pre></td>
    </tr>
    <tr>
        <td>PUT /supermarkets/{supermarket_id}/categories/{category_id}/products</td>
        <td><pre>
            tags:
        - "Supermarket Categories Service"
      summary: "Add new product to supermarket"
      parameters:
        - $ref: "#/components/parameters/supermarket_id"
        - $ref: "#/components/parameters/category_id"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Supermarket_categories'
        </pre></td>
        <td><pre>
            responses:
        "200":
          description: "Successfully added product to supermarket"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Supermarket_categories'
        "404":
          description: "Supermarket' or Category's not found"
        </pre></td>
    </tr>
    <tr>
        <td>DELETE /supermarkets/{supermarket_id}/categories/{category_id}</td>
        <td></td>
        <td><pre>
             tags:
        - "Supermarket Categories Service"
      summary: "Remove category from supermarket"
      parameters:
        - $ref: "#/components/parameters/supermarket_id"
        - $ref: "#/components/parameters/category_id"
      responses:
        "200":
          description: "Successfully removed category from supermarket"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Supermarket_categories'
        "404":
          description: "Supermarket's or Category's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>DELETE /supermarkets/{supermarket_id}/categories/{category_id}/products/{product_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "Supermarket Categories Service"
      summary: "Remove product from supermarket"
      parameters:
        - $ref: "#/components/parameters/supermarket_id"
        - $ref: "#/components/parameters/product_id"
        - $ref: "#/components/parameters/category_id"
      responses:
        "200":
          description: "Successfully removed product from supermarket"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Supermarket_categories'
        "404":
          description: "Supermarket's, Category's or Product's id not found"
        </pre></td>
    </tr>
    <!------ Feedback Service -------->
    <tr>
        <td rowspan="3">Feedback Service</td>
        <td>GET /products/{product_id}/feddback</td>
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
      summary: "Search Feedback by feedback id"
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
    <!------ QRScan Service -------->
    <tr>
        <td rowspan="3">QRScan Service</td>
        <td>GET /qrcodes/{qrcode_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "QRScan Service"
      summary: "Search QRcode by id"
      parameters:
        - $ref: "#/components/parameters/qrcode_id"
      responses:
        "200":
          description: "Successfully found qrcode "
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/QRScan'
        "404":
          description: "QRcode's id not found"
        </pre></td>
    </tr>
    <tr>
        <td>DELETE /qrcodes/{qrcode_id}</td>
        <td></td>
        <td><pre>
            tags:
        - "QRScan Service"
      summary: "Delete QRcode by id"
      parameters:
        - $ref: "#/components/parameters/qrcode_id"
      responses:
        "200":
          description: "Successfully removed qrcode"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/QRScan'
        </pre></td>
    </tr>
    <tr>
        <td>PUT /qrcodes</td>
        <td><pre>
            tags:
        - "QRScan Service"
      summary: "Add QRcode"
      parameters:
        - $ref: "#/components/parameters/qrcode_id"
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/QRScan'
        </pre></td>
        <td><pre>
            responses:
        "200":
          description: "Successfully added QRcode"
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/QRScan'
        </pre></td>
    </tr>
</table>
