# Task 7 : BE - RESOURCES
<table>
<tr>
    <th>BE Services</th>
    <th>Request</th>
    <th>Resources</th>
    <th>Description</th>
</tr>
<tr>
    <td rowspan="4">Serviço de Perfil</td>
    <td>POST</td>
    <td>/profiles</td>
    <td>Criar um novo perfil</td>
</tr>
<tr>
    <td>GET</td>
    <td>/profiles</td>
    <td>Obter a lista de perfis</td>
</tr>
<tr>
    <td>GET</td>
    <td>/profiles/{profile_id}</td>
    <td>Obter detalhes de um perfil específico</td>
</tr>
<tr>
    <td>PUT</td>
    <td>/profiles/{profile_id}</td>
    <td>Atualizar um perfil específico</td>
</tr>
<tr>
    <td rowspan="5">Serviço de Supermercado</td>
    <td>POST</td>
    <td>/supermarkets</td>
    <td>Criar um novo supermercado</td>
</tr>
<tr>
    <td>GET</td>
    <td>/supermarkets/{supermarket_id}</td>
    <td>Obter detalhes de um supermercado específico</td>
</tr>
<tr>
    <td>GET</td>
    <td>/supermarkets</td>
    <td>Obter a lista de supermercados</td>
</tr>
<tr>
    <td>DELETE</td>
    <td>/supermarkets/{supermarket_id}</td>
    <td>Eliminar um supermercado específico</td>
</tr>
<tr>
    <td>PUT</td>
    <td>/supermarkets/{supermarket_id}</td>
    <td>Atualizar um supermercado específico</td>
</tr>
<tr>
    <td rowspan="5">Serviço de Produto</td>
    <td>POST</td>
    <td>/products</td>
    <td>Criar um novo produto</td>
</tr>
<tr>
    <td>GET</td>
    <td>/products/{product_id}</td>
    <td>Obter detalhes de um produto específico</td>
</tr>
<tr>
    <td>GET</td>
    <td>/products</td>
    <td>Obter a lista de produtos</td>
</tr>
<tr>
    <td>DELETE</td>
    <td>/products/{product_id}</td>
    <td>Eliminar um produto específico</td>
</tr>
<tr>
    <td>PUT</td>
    <td>/products/{product_id}</td>
    <td>Atualizar um produto específico</td>
</tr>
<tr>
    <td rowspan="4">Serviço de Categoria</td>
    <td>POST</td>
    <td>/categories</td>
    <td>Criar uma nova categoria</td>
</tr>
<tr>
    <td>GET</td>
    <td>/categories/{category_id}</td>
    <td>Obter detalhes de uma categoria específica</td>
</tr>
<tr>
    <td>GET</td>
    <td>/categories</td>
    <td>Obter a lista de categorias</td>
</tr>
<tr>
    <td>DELETE</td>
    <td>/categories/{category_id}</td>
    <td>Eliminar uma categoria específica</td>
</tr>
<tr>
    <td rowspan="2">Serviço de Notícias</td>
    <td>GET</td>
    <td>/news</td>
    <td>Obter a lista de notícias</td>
</tr>
<tr>
    <td>GET</td>
    <td>/news/{news_id}</td>
    <td>Obter detalhes de uma notícia específica</td>
</tr>
<tr>
    <td rowspan="1">Serviço de Estatísticas</td>
    <td>GET</td>
    <td>/statistics</td>
    <td>Obter as estatísticas disponíveis</td>
</tr>
<tr>
    <td rowspan="3">Serviço de Produtos Guardados</td>
    <td>GET</td>
    <td>/profiles/{profile_id}/favourite-products</td>
    <td>Obter a lista de produtos guardados de um perfil</td>
</tr>
<tr>
    <td>PUT</td>
    <td>/profiles/{profile_id}/favourite-products</td>
    <td>Guardar um novo produto no perfil</td>
</tr>
<tr>
    <td>DELETE</td>
    <td>/profiles/{profile_id}/favourite-products/{product_id}</td>
    <td>Eliminar um produto guardado de um perfil</td>
</tr>
<tr>
    <td rowspan="3">Serviço de Categoria de Supermercado</td>
    <td>GET</td>
    <td>/supermarkets/{supermarket_id}/categories/{category_id}/products</td>
    <td>Obter a lista de produtos de uma categoria específica de um supermercado</td>
</tr>
<tr>
    <td>PUT</td>
    <td>/supermarkets/{supermarket_id}/categories/{category_id}/products</td>
    <td>Adicionar ou atualizar um produto numa categoria específica de um supermercado</td>
</tr>
<tr>
    <td>DELETE</td>
    <td>/supermarkets/{supermarket_id}/categories/{category_id}/products/{product_id}</td>
    <td>Eliminar um produto de uma categoria específica de um supermercado</td>
</tr>
<tr>
    <td rowspan="3">Serviço de Avaliação</td>
    <td>GET</td>
    <td>/products/{product_id}/feedback</td>
    <td>Obter a lista de avaliações de um produto específico</td>
</tr>
<tr>
    <td>PUT</td>
    <td>/products/{product_id}/feedback</td>
    <td>Adicionar ou atualizar uma avaliação de um produto</td>
</tr>
<tr>
    <td>GET</td>
    <td>/products/{product_id}/feedback/{feedback_id}</td>
    <td>Obter detalhes de uma avaliação específica de um produto</td>
</tr>
<tr>
    <td rowspan="3">Serviço de Leitura de QR</td>
    <td>PUT</td>
    <td>/qrcodes</td>
    <td>Criar um novo código QR</td>
</tr>
<tr>
    <td>GET</td>
    <td>/qrcodes/{qrcode_id}</td>
    <td>Obter detalhes de um código QR específico</td>
</tr>
<tr>
    <td>DELETE</td>
    <td>/qrcodes/{qrcode_id}</td>
    <td>Eliminar um código QR específico</td>
</tr>
</table>
