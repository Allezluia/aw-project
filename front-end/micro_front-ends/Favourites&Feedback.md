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
        <tr><td rowspan="12"><img src="./Favourites_&_Feedback_1.png" alt="Feedback" width="100" height="200">
        <tr><td rowspan="2">mainView</td>
        <td>props.meatImage</td></tr>
        </tr>
        <td>props.textBox</td>
        </tr>
        <td rowspan="6">TextBox</td>
        <td>props.tittle</td>
        </tr>
        </tr>
        <td>props.price</td>
        </tr>
        <td>props.feedbackList</td>
        </tr>
        <td>props.textMenssage</td>
        </tr>
        <td>props.saveButton</td>
        </tr>
        <td>props.feedbackButton</td>
        </tr>
        <tr><td rowspan="3">Feedback Box</td>
        <td>props.feedbackIcon</td></tr>
        </tr>
        <td>props.feedbackName</td>
        </tr>
        <td>props.feedbackRating</td>
        </tr>
        <tr><td rowspan="6"><img src="./Favourites_&_Feedback_3.png" alt="Feedback" width="100" height="200">
        <tr><td rowspan="1">mainView</td>
        <td>props.PopUp</td></tr>
        </tr>
        <tr><td rowspan="4">PopUp</td>
        <td>props.PopUpTitle</td></tr>
        </tr>
        <td>props.PopUpRating</td></tr>
        </tr>
        <td>props.PopUpCancelButton</td></tr>
        </tr>
        <td>props.PopUpSaveButton</td></tr>
        </tr>
        <tr><td rowspan="5"><img src="./Favourites_&_Feedback_2.png" alt="Feedback" width="100" height="200">
        <tr><td rowspan="1">mainView</td>
        <td>props.PopUp</td></tr>
        </tr>
        <tr><td rowspan="3">PopUp</td>
        <td>props.PopUpIcon</td></tr>
        </tr>
        <td>props.PopUptextMenssage</td></tr>
        </tr>
        <td>props.PopUpConfirmationButton</td></tr>
        </tr>
      
    
</table>


