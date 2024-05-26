# Task 6
<table>
        <tr>
            <th>Serviço BE</th>
            <th>Descrição do Serviço</th>
            <th>Descrição dos Recursos</th>
            <th>Dependências</th>
        </tr>
        <tr>
            <td>Serviço de Perfil</td>
            <td>Armazena múltiplas contas de utilizadores</td>
            <td>Nome de utilizador, senha, configurações da conta, e-mail</td>
            <td>Nenhuma</td>
        </tr>
        <tr>
            <td>Serviço de Supermercado</td>
            <td>Gerencia a lista de supermercados conhecidos pela aplicação</td>
            <td>Nome, localização</td>
            <td>Nenhuma</td>
        </tr>
        <tr>
            <td>Serviço de Produto</td>
            <td>Armazena todos os produtos disponíveis de todos os mercados</td>
            <td>Nome, preço, imagem do produto, produtor, origem, detalhes, informações adicionais</td>
            <td>Nenhuma</td>
        </tr>
        <tr>
            <td>Serviço de Categoria</td>
            <td>Armazena todas as categorias de produtos de todos os mercados</td>
            <td>Nome</td>
            <td>Nenhuma</td>
        </tr>
        <tr>
            <td>Serviço de Notícias</td>
            <td>Obtém as notícias mais recentes</td>
            <td>Texto das notícias, cabeçalho, imagem, jornal</td>
            <td>Nenhuma</td>
        </tr>
        <tr>
            <td>Serviço de Estatísticas</td>
            <td>Obtém estatísticas positivas e negativas recentes</td>
            <td>Consumo médio de carne, área desmatada, produção animal, emissões de CH4 e CO2, etc.</td>
            <td>Nenhuma</td>
        </tr>
        <tr>
            <td>Serviço de Produtos Guardados</td>
            <td>Associa e armazena produtos guardados pelos utilizadores</td>
            <td>ID do utilizador, lista de IDs de produtos guardados</td>
            <td>Perfil, Produto</td>
        </tr>
        <tr>
            <td>Serviço de Catálogo de Supermercado</td>
            <td>Gerencia a lista de produtos dos supermercados</td>
            <td>Lista de IDs de produtos e IDs de supermercados por categoria</td>
            <td>Supermercado, Produto, Categoria</td>
        </tr>
        <tr>
            <td>Serviço de Avaliação</td>
            <td>Armazena e calcula a média das avaliações dos utilizadores</td>
            <td>Número de estrelas (avaliação), ID do utilizador, ID do produto</td>
            <td>Perfil, Produto</td>
        </tr>
        <tr>
            <td>Serviço de Leitura de QR</td>
            <td>Relaciona códigos QR às referências dos produtos</td>
            <td>Código QR, ID do produto</td>
            <td>Produto</td>
        </tr>
    </table>
