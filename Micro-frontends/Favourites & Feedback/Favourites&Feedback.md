## Contexto e Problema

Foi considerado um mecanismo que permite aos utilizadores gerir e "salvar" os produtos que desejam manter como favoritos, para posterior visualização ou compra. Com efeito, é guardada uma lista dos produtos guardados (marcados como favoritos), sendo apresentadas as informações relevantes acerca dos mesmos.
Para além disso, temos também um mecanismo que permite ao utilizador dar *feedback*, de 1 a 5 estrelas, relativamente a um produto.

Estes mecanismos visam solucionar o facto dos utilizadores não possuírem uma forma prática de salvar os produtos para posterior revisão/compra e ajuda a empresa a perceber as preferências dos clientes. Também fornece aos utilizadores uma maneira de tomar decisões conscientes nas suas compras com base nas avaliações de outros utilizadores (neste caso, no rating do produto).

## Decisão

Decidimos considerar o mecanismo de favoritos e *feedback* como um único *micro-frontend*, devido à forte interligação entre estas funcionalidades. A própria *app* sugere que *“é recomendado salvar o produto para mais tarde contribuir com o respetivo feedback”*, ou seja, os utilizadores são incentivados a “salvar” produtos como favoritos para, mais tarde, contribuírem com uma avaliação.

## Justificações

Ter um *micro-frontend* para gerir e “**salvar**” **favoritos** produtos  e que permite dar **feedback** dos mesmos, proporciona uma abordagem mais simples e direta de gerir estas funcionalidades, promovendo também a sua fácil **reutilização** em diferentes partes do sistema.

Ao ter um *micro-frontend*  dedicado aos favoritos e *feedback*, garantimos uma **responsabilidade única**, facilitando a compreensão e manutenção destas funcionalidades.

Correções ou atualizações podem ser **implementadas independentemente** de outros serviços, permitindo uma implementação mais ágil e segura, sem afetar outras partes da aplicação.

Uma **equipa dedicada** pode concentrar-se em manter e melhorar estas funcionalidades, garantindo que atenda às necessidades dos utilizadores de forma eficiente.

**Serviços verticais:** Alinha-se com a arquitetura vertical de serviços do projeto, permitindo um controlo detalhado e escalabilidade.

**Flexibilidade:** Permite modificar e melhorar estas funcionalidades de forma independente, conforme necessário, sem afetar outras partes do sistema.

## Task 2

<table>
    <tr>
        <td>Micro-Frontend</td>
        <td>View</td>
        <td>FE Service</td>
    </tr>
    <tr>
        <td rowspan="12">Favourites & Feedback </td>
        <td rowspan="4"><img src="./Favourites_&_Feedback_4.png" alt="Favourite" width="100" height="200"></td>
    <tr><td>RemoveFromFavourites</td></tr>
    <tr><td>GetFavouritesForUser</td></tr>
    <tr><td>SendFavouriteRemovedNotification</td></tr>
    <tr><td rowspan="8"><img src="./Favourites_&_Feedback_1.png" alt="Feedback" width="100" height="200">
    <td>SubmitFeedback</td></tr> 
    <tr><td>GetFeedbackDetails</td></tr>
    <tr><td>AddToFavourites</td></tr>
    <tr><td>SendfavouriteAddedNotification</td></tr>
    <tr><td>RecordFeedbackSubmission</td></tr>
    <tr><td>GenerateFeedbackReports</td></tr>
    <tr><td>SendFeedbackAcknowledgementNotification</td></tr>
    <tr><td>SendFeedbackResolvedNotification</td></tr>
</table>


## Task 3

<table>
    <tr>
        <td>Views</td>
        <td>Components</td>
        <td>View models</td>
    </tr>
    <tr>
        <td rowspan="7"><img src="./Favourites_&_Feedback_4.png" alt="Favourite" width="100" height="200"></td>
        <td rowspan="2">mainView</td>
        <td>props.titleName</td>
        </tr>
        <td>props.textBox</td>
        </tr>
        <tr><td rowspan="3">Single Card</td>
        <td>props.superMarketLocation</td></tr>
        </tr>
        <td>props.meatImage</td>
        </tr>
        </tr>
        <td>props.price</td>
        </tr>
        <tr><td rowspan="2">Card List</td>
        <td>props.cards</td></tr>
        </tr>
        <td>props.favouriteList</td>
        </tr>
        <tr><td rowspan="8"><img src="./Favourites_&_Feedback_1.png" alt="Feedback" width="100" height="200">
        <td rowspan="3">Top View</td>
        <td>props.meatLogo</td>
        </tr>
        <td>props.tittle</td>
        </tr>
        </tr>
        <td>props.price</td>
        </tr>
        <tr><td rowspan="2">Feedback Box</td>
        <td>props.feedbackTitle</td></tr>
        </tr>
        <td>props.feedbackList</td>
        </tr>
        <tr><td rowspan="1"> Bottom view</td>
        <td>props.informations</td></tr>
    
</table>

## Task 3 - versao 2

<table>
    <tr>
        <td>Views</td>
        <td>Components</td>
        <td>View models</td>
    </tr>
    <tr>
        <td rowspan="7"><img src="./Favourites_&_Feedback_4.png" alt="Favourite" width="100" height="200"></td>
        <td rowspan="2">mainView</td>
        <td>props.titleName</td>
        </tr>
        <td>props.textBox</td>
        </tr>
        <tr><td rowspan="4">Single Card</td>
        <td>props.superMarketLocation</td></tr>
        </tr>
        <td>props.meatImage</td>
        </tr>
        <td>props.meatDescription</td>
        </tr>
        </tr>
        <td>props.price</td>
        </tr>
        <tr><td rowspan="1">Card List</td>
        <td>props.cards</td></tr>
        </tr>
        <tr><td rowspan="8"><img src="./Favourites_&_Feedback_1.png" alt="Feedback" width="100" height="200">
        <tr><td rowspan="2">mainView</td>
        <td>props.meatImage</td></tr>
        </tr>
        <td>props.textBox</td>
        </tr>
        <td rowspan="3">TextBox</td>
        <td>props.tittle</td>
        </tr>
        </tr>
        <td>props.price</td>
        </tr>
        <td>props.feedbackList</td>
        </tr>
        <tr><td rowspan="2">Feedback Box</td>
        <td>props.feedbackTitle</td></tr>
        </tr>
        <td>props.feedbackList</td>
        </tr>
        <tr><td rowspan="1"> Bottom view</td>
        <td>props.informations</td></tr>
    
</table>



