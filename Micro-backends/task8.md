# Task 8

<table border="1">
    <tr>
        <th>BE services </th>
        <th>Method</th>
        <th>Schema</th>
        <th>Requests</th>
        <th>Responses</th>
    </tr>
    <!-- GET all products -->
    <tr>
        <td rowspan="5">Gestão do Catálogo de Produtos</td>
        <td>GET</td>
        <td>
            type: object<br>
            properties:<br>
            - productId: integer (Identificador único do produto)<br>
            - name: string (Nome do produto)<br>
            - price: decimal (Preço do produto)<br>
            - description: string (Descrição do produto)
        </td>
        <td>
            paths:<br>
            /products<br>
            summary: Recupera uma lista de todos os produtos.<br>
            parameters: none
        </td>
        <td>
            200:<br>
            description: Lista de todos os produtos.<br>
            content: application/json;<br>
            schema: array<br>
            items: $ref: '#/components/schemas/Product'
        </td>
    </tr>
    <!-- GET specific product -->
    <tr>
        <td>GET</td>
        <td>
            type: object<br>
            properties:<br>
            - productId: integer (Identificador único do produto)<br>
            - name: string (Nome do produto)<br>
            - price: decimal (Preço do produto)<br>
            - description: string (Descrição do produto)
        </td>
        <td>
            paths:<br>
            /products/{product_id}<br>
            summary: Recupera detalhes de um produto específico.<br>
            parameters:<br>
            - name: product_id<br>
            - in: path<br>
            - required: true<br>
            - type: integer
        </td>
        <td>
            200:<br>
            description: Detalhes do produto especificado.<br>
            content: application/json;<br>
            schema: $ref: '#/components/schemas/Product'
        </td>
    </tr>
    <!-- POST new product -->
    <tr>
        <td>POST</td>
        <td>
            type: object<br>
            properties:<br>
            - name: string (Nome do produto)<br>
            - price: decimal (Preço do produto)<br>
            - description: string (Descrição do produto)
        </td>
        <td>
            paths:<br>
            /products<br>
            summary: Adiciona um novo produto ao catálogo.<br>
            requestBody:<br>
            required: true<br>
            content:<br>
            application/json;<br>
            schema: $ref: '#/components/schemas/Product'
        </td>
        <td>
            201:<br>
            description: Produto criado com sucesso.<br>
            content: application/json;
        </td>
    </tr>
    <!-- PUT update product -->
    <tr>
        <td>PUT</td>
        <td>
            type: object<br>
            properties:<br>
            - productId: integer (Identificador único do produto)<br>
            - name: string (Nome do produto)<br>
            - price: decimal (Preço do produto)<br>
            - description: string (Descrição do produto)
        </td>
        <td>
            paths:<br>
            /products/{product_id}<br>
            summary: Atualiza um produto específico no catálogo.<br>
            parameters:<br>
            - name: product_id<br>
            - in: path<br>
            - required: true<br>
            - type: integer<br>
            requestBody:<br>
            required: true<br>
            content:<br>
            application/json;<br>
            schema: $ref: '#/components/schemas/Product'
        </td>
        <td>
            200:<br>
            description: Produto atualizado com sucesso.<br>
            content: application/json;
        </td>
    </tr>
    <!-- DELETE specific product -->
    <tr>
        <td>DELETE</td>
        <td>
            type: object<br>
            properties:<br>
            - productId: integer (Identificador único do produto)
        </td>
        <td>
            paths:<br>
            /products/{product_id}<br>
            summary: Elimina um produto específico do catálogo.<br>
            parameters:<br>
            - name: product_id<br>
            - in: path<br>
            - required: true<br>
            - type: integer
        </td>
        <td>
            204:<br>
            description: Produto eliminado com sucesso.
        </td>
    </tr>
    <!-- GET all statistics -->
    <tr>
        <td rowspan="4">Estatísticas</td>
        <td>GET</td>
        <td>
            type: object<br>
            properties:<br>
            - statisticsId: integer (Identificador único das estatísticas)<br>
            - category: string (Categoria das estatísticas)<br>
            - value: decimal (Valor associado)<br>
            - timestamp: datetime (Data e hora da geração da estatística)
        </td>
        <td>
            paths:<br>
            /statistics<br>
            summary: Recupera todas as estatísticas.<br>
            parameters: none
        </td>
        <td>
            200:<br>
            description: Lista de todas as estatísticas.<br>
            content: application/json;<br>
            schema: array<br>
            items: $ref: '#/components/schemas/Statistics'
        </td>
    </tr>
    <!-- POST new statistics -->
    <tr>
        <td>POST</td>
        <td>
            type: object<br>
            properties:<br>
            - category: string (Categoria das estatísticas)<br>
            - value: decimal (Valor associado)<br>
            - timestamp: datetime (Data e hora da geração da estatística)
        </td>
        <td>
            paths:<br>
            /statistics/{statistics_id}<br>
            summary: Adiciona novas estatísticas para uma categoria específica.<br>
            requestBody:<br>
            required: true<br>
            content:<br>
            application/json;<br>
            schema: $ref: '#/components/schemas/Statistics'
        </td>
        <td>
            201:<br>
            description: Estatísticas criadas com sucesso.<br>
            content: application/json;
        </td>
    </tr>
    <!-- PUT update statistics -->
    <tr>
        <td>PUT</td>
        <td>
            type: object<br>
            properties:<br>
            - statisticsId: integer (Identificador único das estatísticas)<br>
            - category: string (Categoria das estatísticas)<br>
            - value: decimal (Valor atualizado)<br>
            - timestamp: datetime (Data e hora da atualização)
        </td>
        <td>
            paths:<br>
            /statistics/{statistics_id}<br>
            summary: Atualiza estatísticas existentes.<br>
            parameters:<br>
            - name: statistics_id<br>
            - in: path<br>
            - required: true<br>
            - type: integer<br>
            requestBody:<br>
            required: true<br>
            content:<br>
            application/json;<br>
            schema: $ref: '#/components/schemas/Statistics'
        </td>
        <td>
            200:<br>
            description: Estatísticas atualizadas com sucesso.<br>
            content: application/json;
        </td>
    </tr>
    <!-- DELETE all statistics -->
    <tr>
        <td>DELETE</td>
        <td>
            type: object<br>
            properties:<br>
            - statisticsId: integer (Identificador único das estatísticas)
        </td>
        <td>
            paths:<br>
            /statistics/{statistics_id}<br>
            summary: Elimina todas as estatísticas.<br>
            parameters:<br>
            - name: statistics_id<br>
            - in: path<br>
            - required: true<br>
            - type: integer
        </td>
        <td>
            204:<br>
            description: Estatísticas eliminadas com sucesso.
        </td>
    </tr>
</table>

