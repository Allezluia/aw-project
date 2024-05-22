# Task 7

<table border="1">
    <tr>
        <th>Serviços BE</th>
        <th>Pedido</th>
        <th>Recursos</th>
        <th>Descrição do Pedido</th>
    </tr>
  <!-------- Noticias -------->
    <tr>
        <td rowspan = "6">Notícias</td>
        <td>GET</td>
        <td>/news</td>
        <td>Recupera uma lista de todas as notícias.</td>
    </tr>
    <tr>
        <td>GET</td>
        <td>/news/{news_id}</td>
        <td>Recupera uma notícia específica pelo seu identificador único.</td>
    </tr>
    <tr>
        <td>POST</td>
        <td>/news</td>
        <td>Cria uma nova notícia.</td>
    </tr>
    <tr>
        <td>PUT</td>
        <td>/news/{news_id}</td>
        <td>Atualiza uma notícia existente.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/news/{article_id}</td>
        <td>Elimina uma notícia específica.</td>
    </tr>
    <tr>
      <td>PUT</td>
      <td>/news/{news_id}/archive</td>
      <td>Arquiva uma notícia específica.</td>
    </tr>
  <!-------- Supermercado -------->
    <tr>
        <td rowspan = "5">Supermercado</td>
        <td>GET</td>
        <td>/supermarket</td>
        <td>Recupera uma lista de todos os supermercados.</td>
    </tr>
    <tr>
        <td>GET</td>
        <td>/supermarket/{supermarket_id}</td>
        <td>Recupera um supermercado específico pelo seu identificador.</td>
    </tr>
    <tr>
        <td>PUT</td>
        <td>/supermarket/{supermarket_id}</td>
        <td>Atualiza informações sobre um supermercado.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/supermarket</td>
        <td>Elimina um supermercado.</td>
    </tr>
    <tr>
      <td>GET</td>
      <td>/supermarket/search</td>
      <td>Pesquisa supermercados por nome ou localização.</td>
    </tr>
  <!-------- Gestão do Catálogo de Produtos -------->
    <tr>
        <td rowspan = "5">Gestão do Catálogo de Produtos</td>
        <td>GET</td>
        <td>/products</td>
        <td>Recupera uma lista de todos os produtos.</td>
    </tr>
    <tr>
        <td>GET</td>
        <td>/products/{product_id}</td>
        <td>Recupera detalhes de um produto específico.</td>
    </tr>
    <tr>
        <td>POST</td>
        <td>/products</td>
        <td>Adiciona um novo produto ao catálogo.</td>
    </tr>
    <tr>
        <td>PUT</td>
        <td>/products/{product_id}</td>
        <td>Atualiza um produto específico no catálogo.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/products/{product_id}</td>
        <td>Elimina um produto específico do catálogo.</td>
    </tr>
      <!-------- Preços dos Produtos -------->
    <tr>
        <td rowspan = "4">Preços dos Produtos</td>
        <td>GET</td>
        <td>/prices/products/{product_id}</td>
        <td>Recupera o preço de um produto específico.</td>
    </tr>
    <tr>
        <td>PUT</td>
        <td>/prices/products/{product_id}</td>
        <td>Atualiza o preço de um produto específico.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/prices/products/{product_id}</td>
        <td>Elimina o preço de um produto específico.</td>
    </tr>
    <tr>
      <td>PUT</td>
      <td>/prices/adjust</td>
      <td>Ajusta preços com base em fatores sazonais ou promocionais.</td>
    </tr>
    <!-- Revisão de Produtos -->
    <tr>
        <td rowspan = "5">Revisão de Produtos</td>
        <td>GET</td>
        <td>/reviews/products/{product_id}</td>
        <td>Recupera avaliações para um produto específico.</td>
    </tr>
    <tr>
        <td>POST</td>
        <td>/reviews/products/{product_id}</td>
        <td>Adiciona uma nova avaliação para um produto específico.</td>
    </tr>
    <tr>
        <td>PUT</td>
        <td>/reviews/products/{product_id}</td>
        <td>Atualiza uma avaliação existente.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/reviews/products/{product_id}</td>
        <td>Elimina uma avaliação específica.</td>
    </tr>
    <tr>
      <td>GET</td>
      <td>/reviews/products/{product_id}/aggregate</td>
      <td>Calcula avaliações agregadas para produtos.</td>
    </tr>
    <!-- Informação Específica do Produto -->
    <tr>
        <td rowspan = "5">Informação Específica do Produto</td>
        <td>GET</td>
        <td>/details/products/{product_id}</td>
        <td>Recupera detalhes para um produto específico.</td>
    </tr>
    <tr>
        <td>POST</td>
        <td>/details/products/{product_id}</td>
        <td>Adiciona novos detalhes a um produto específico.</td>
    </tr>
    <tr>
        <td>PUT</td>
        <td>/details/products/{product_id}</td>
        <td>Atualiza detalhes de um produto específico.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/details/products/{product_id}</td>
        <td>Elimina detalhes de um produto específico.</td>
    </tr>
    <tr>
      <td>GET</td>
      <td>/details/products/{product_id}/{product_id}</td>
      <td>Permite a comparação entre diferentes produtos.</td>
    </tr>
    <!-- Autenticação de Clientes -->
    <tr>
        <td rowspan = "8">Autenticação de Clientes</td>
        <td>PUT</td>
        <td>/auth/{client_id}</td>
        <td>Atualiza a informação de um cliente específico.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/auth</td>
        <td>Elimina um cliente.</td>
    </tr>
    <tr>
        <td>GET</td>
        <td>/auth/{login_id}</td>
        <td>Permite aos clientes autenticar-se fornecendo credenciais.</td>
    </tr>
    <tr>
        <td>POST</td>
        <td>/auth/{client_id}/details</td>
        <td>Atualiza detalhes específicos de um cliente.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/auth/{client_id}/details</td>
        <td>Elimina detalhes específicos de um cliente.</td>
    </tr>
    <tr>
    <td>PUT</td>
    <td>/auth/{client_id}/refresh</td>
    <td>Renova o token de autenticação de um cliente específico.</td>
</tr>
<tr>
    <td>DELETE</td>
    <td>/auth/{client_id}/token</td>
    <td>Revoga o token de autenticação de um cliente específico.</td>
</tr>  
  <tr>
    <td>POST</td>
    <td>/auth/forgot-password</td>
    <td>Gerencia o processo de recuperação ou redefinição de senha.</td>
</tr>
    <!-- Estatísticas -->
    <tr>
        <td rowspan = "4">Estatísticas</td>
        <td>GET</td>
        <td>/statistics</td>
        <td>Recupera todas as estatísticas.</td>
    </tr>
    <tr>
        <td>POST</td>
        <td>/statistics/{statistics_id}</td>
        <td>Adiciona novas estatísticas para uma categoria específica.</td>
    </tr>
    <tr>
        <td>PUT</td>
        <td>/statistics/{statistics_id}</td>
        <td>Atualiza estatísticas existentes.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/statistics/{statistics_id}</td>
        <td>Elimina todas as estatísticas.</td>
    </tr>
    <!-- Informação de Clientes -->
    <tr>
        <td rowspan = "4">Informação de Clientes</td>
        <td>GET</td>
        <td>/clients</td>
        <td>Recupera informação de todos os clientes.</td>
    </tr>
    <tr>
        <td>PUT</td>
        <td>/clients/{client_id}</td>
        <td>Atualiza informação de um cliente.</td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>/clients/{client_id}</td>
        <td>Elimina um cliente.</td>
    </tr>
  <tr>
    <td>PUT</td>
    <td>/clients/{client_id}/privacy</td>
    <td>Gerencia configurações de privacidade e permissões de acesso a dados.</td>
</tr>
    <!-- QReader -->
    <tr>
        <td rowspan = "2">QReader</td>
        <td>GET</td>
        <td>/scan/{product_id}</td>
        <td>Recupera informação ligada a um produto específico.</td>
    </tr>
    <tr>
        <td>POST</td>
        <td>/scan</td>
        <td>Envia uma imagem de um QR Code para ser escaneada e processada.</td>
    </tr>

</table>
