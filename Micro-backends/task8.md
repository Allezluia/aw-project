# Task 8

<table border="1">
    <tr>
        <th>BE services</th>
        <th>Method</th>
        <th>Schema</th>
        <th>Requests</th>
        <th>Responses</th>
    </tr>
    <!-- Market Listings -->
    <tr>
        <td>Listagem de Mercados</td>
        <td>GET</td>
        <td>
            properties:<br>
            - marketId: integer<br>
            - name: string<br>
            - location: string<br>
            - vendorCount: integer
        </td>
        <td>
            paths:<br>
            /markets<br>
            summary: Retrieves all market listings.<br>
            parameters: none
        </td>
        <td>
            200:<br>
            description: List of all markets.<br>
            content: application/json;<br>
            schema: array<br>
            items:<br>
            $ref: '#/components/schemas/Market'
        </td>
    </tr>
    <!-- Market Detail -->
    <tr>
        <td>Detalhes do Mercado</td>
        <td>GET</td>
        <td>
            properties:<br>
            - marketId: integer<br>
            - name: string<br>
            - location: string<br>
            - description: string<br>
            - vendorList: array
        </td>
        <td>
            paths:<br>
            /markets/{marketId}<br>
            summary: Retrieves detailed information for a specific market.<br>
            parameters:<br>
            - name: marketId<br>
            - in: path<br>
            - required: true<br>
            - type: integer
        </td>
        <td>
            200:<br>
            description: Detailed information of the market.<br>
            content: application/json;<br>
            schema:<br>
            $ref: '#/components/schemas/Market'
        </td>
    </tr>
    <!-- Update Market -->
    <tr>
        <td>Atualização de Mercado</td>
        <td>PUT</td>
        <td>
            properties:<br>
            - marketId: integer<br>
            - name: string<br>
            - location: string<br>
            - description: string<br>
            - vendorList: array
        </td>
        <td>
            paths:<br>
            /markets/{marketId}<br>
            summary: Updates a specific market.<br>
            parameters:<br>
            - name: marketId<br>
            - in: path<br>
            - required: true<br>
            - type: integer<br>
            requestBody:<br>
            required: true<br>
            content:<br>
            application/json;<br>
            schema:<br>
            $ref: '#/components/schemas/Market'
        </td>
        <td>
            200:<br>
            description: Market updated successfully.<br>
            content: application/json;
        </td>
    </tr>
    <!-- Delete Market -->
    <tr>
        <td>Exclusão de Mercado</td>
        <td>DELETE</td>
        <td>
            properties:<br>
            - marketId: integer
        </td>
        <td>
            paths:<br>
            /markets/{marketId}<br>
            summary: Deletes a specific market.<br>
            parameters:<br>
            - name: marketId<br>
            - in: path<br>
            - required: true<br>
            - type: integer
        </td>
        <td>
            204:<br>
            description: Market deleted successfully.
        </td>
    </tr>
</table>
