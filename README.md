# Trabalho Prático: Programação de Soluções Computacionais
Esse trabalho será realizado como componente final do primeiro semestre do bacharelado em ciência da computação. A fonte do trabalho e suas diretrizes são acessíveis por [este link](https://github.com/alexmontanha/trabalho_final_psc).

A linguagem selecionada para elaborar o trabalho será java.
## Sistema de Aluguel e Compra de Imóveis e Aluguel de Quartos
### Contexto
Uma atividade semelhante foi realizada durante o curso técnico de informática e pode ser acessada por [este link](https://github.com/MattNogueira/MyMoveis/). O trabalho atual é uma releitura da solução do trabalho anterior que será codificado com uma linguagem diferente e sob circunstâncias diferentes. Será, portanto, uma versão simples do projeto mencionado mas com tratamento de exceção, manipulação de arquivos e classes re-elaboradas.
### Proposta de Problema
O sistema consiste em uma plataforma onde o usuário pode comprar ou alugar imóveis e alugar quartos. O sistema deve permitir:
- Cadastro de imóveis para alugar ou vender;
- Cadastro de quartos de um imóvel, caso um quarto esteja sendo alugado mas não o imóvel como um todo;
- Cadastro do usuário;
- Filtrar opções de compra e aluguel dependendo de algumas especificações;
### Requisitos Funcionais, segundo IA (Chat GPT)
Um prompt equivalente ao que está escrito no [segmento anterior](https://github.com/MattNogueira/MyMoveis_Try2/edit/main/README.md#proposta-de-problema) foi entregue à IA enquanto pedia por requisitos funcionais do sistema. O software entregou a seguinte resposta:
> Claro! Aqui estão alguns requisitos funcionais para o seu sistema de compra e aluguel de imóveis e quartos:
>
>### Requisitos Funcionais
>
>#### Cadastro de Imóveis
>1. **Cadastro de Imóveis para Venda**
>   - O sistema deve permitir que o proprietário cadastre um imóvel para venda.
>   - O cadastro deve incluir informações como: endereço, número de quartos, número de banheiros, área em metros quadrados, preço, descrição detalhada e fotos.
>
>2. **Cadastro de Imóveis para Aluguel**
>   - O sistema deve permitir que o proprietário cadastre um imóvel para aluguel.
>   - O cadastro deve incluir informações como: endereço, número de quartos, número de banheiros, área em metros quadrados, preço do aluguel mensal, descrição detalhada e fotos.
>
>3. **Cadastro de Quartos para Aluguel**
>   - O sistema deve permitir que o proprietário cadastre um quarto para aluguel, especificando se faz parte de um imóvel maior.
>   - O cadastro deve incluir informações como: endereço do imóvel, características do quarto (tamanho, mobília, etc.), preço do aluguel mensal, descrição detalhada e fotos.
>
>#### Cadastro de Usuários
>4. **Cadastro de Usuário**
>   - O sistema deve permitir que novos usuários se cadastrem.
>   - O cadastro deve incluir informações como: nome completo, e-mail, senha, telefone e endereço.
>   - O sistema deve verificar a unicidade do e-mail para garantir que não haja duplicidade.
>
>5. **Login de Usuário**
>   - O sistema deve permitir que os usuários façam login utilizando e-mail e senha.
>   - O sistema deve fornecer uma opção de recuperação de senha.
>
>#### Gerenciamento de Imóveis e Quartos
>6. **Edição e Exclusão de Imóveis e Quartos**
>   - O sistema deve permitir que os proprietários editem ou excluam seus cadastros de imóveis e quartos.
>   - O sistema deve manter um histórico de alterações.
>
>7. **Visualização de Detalhes dos Imóveis e Quartos**
>   - O sistema deve permitir que os usuários visualizem os detalhes completos dos imóveis e quartos cadastrados, incluindo todas as informações e fotos.
>
>#### Filtros e Pesquisa
>8. **Filtragem de Imóveis e Quartos**
>   - O sistema deve permitir que os usuários filtrem imóveis e quartos com base em critérios como: localização, preço, número de quartos, tipo de imóvel (casa, apartamento, quarto), entre outros.
>   - O sistema deve permitir a combinação de múltiplos critérios para uma pesquisa mais refinada.
>
>9. **Pesquisa por Palavra-Chave**
>   - O sistema deve permitir que os usuários realizem buscas utilizando palavras-chave relacionadas aos imóveis e quartos.
>
>#### Funcionalidades de Transação
>10. **Interesse e Contato**
>    - O sistema deve permitir que os usuários manifestem interesse em um imóvel ou quarto.
>    - O sistema deve fornecer opções de contato direto entre o interessado e o proprietário, como e-mail ou telefone.
>
>11. **Favoritos**
>    - O sistema deve permitir que os usuários adicionem imóveis e quartos aos favoritos para uma visualização rápida posterior.
>
>#### Segurança e Privacidade
>12. **Autenticação e Autorização**
>    - O sistema deve garantir que apenas usuários autenticados possam cadastrar e gerenciar imóveis e quartos.
>    - O sistema deve garantir que um usuário não possa editar ou excluir cadastros que não sejam de sua propriedade.
>
>13. **Proteção de Dados**
>    - O sistema deve garantir a proteção dos dados pessoais dos usuários, seguindo as normas de privacidade aplicáveis.
>
>### Funcionalidades Adicionais
>14. **Avaliações e Comentários**
>    - O sistema pode permitir que os usuários avaliem e comentem sobre os imóveis e quartos que visitaram ou alugaram/compraram.
>
>15. **Notificações**
>    - O sistema pode enviar notificações aos usuários sobre novos imóveis e quartos que atendam aos seus critérios de busca ou sobre atualizações importantes relacionadas aos seus cadastros.
>
>Esses requisitos funcionais cobrem as principais funcionalidades esperadas para um sistema de compra e aluguel de imóveis e quartos. É importante também considerar a implementação de uma interface amigável e intuitiva, bem como a performance e escalabilidade do sistema, para garantir uma boa experiência ao usuário.
### Crítica à IA
Agora, cada item oferecido como requisito funcional pela IA será analisado criticamente e terá sua integração ao sistema discutida.
>#### Cadastro de Imóveis
>1. **Cadastro de Imóveis para Venda**
>   - O sistema deve permitir que o proprietário cadastre um imóvel para venda.
>   - O cadastro deve incluir informações como: endereço, número de quartos, número de banheiros, área em metros quadrados, preço, descrição detalhada e fotos.
>
>2. **Cadastro de Imóveis para Aluguel**
>   - O sistema deve permitir que o proprietário cadastre um imóvel para aluguel.
>   - O cadastro deve incluir informações como: endereço, número de quartos, número de banheiros, área em metros quadrados, preço do aluguel mensal, descrição detalhada e fotos.
>
>3. **Cadastro de Quartos para Aluguel**
>   - O sistema deve permitir que o proprietário cadastre um quarto para aluguel, especificando se faz parte de um imóvel maior.
>   - O cadastro deve incluir informações como: endereço do imóvel, características do quarto (tamanho, mobília, etc.), preço do aluguel mensal, descrição detalhada e fotos.

Os dois primeiros itens, 1 e 2, estão aceitáveis e serão incluídos no passo seguinte, com a exceção de que dada a inexistência de controle de acesso, não será de responsabilidade de um usuário cadastrado, vulgo proprietário, realizar o cadastro. Além disso, não se incluirá imagens dentre os atributos dos imóveis. O último item do trecho, item 3, é insuficiente: Sempre que um quarto é criado, ele deve ser parte de um imóvel, não sendo opcional. Ademais, o campo 'características do quarto' é muito abrangente e deve ser separado nas informações relevantes, que determinarei serem: tamanho e se é mobiliado ou não, apenas.
>#### Cadastro de Usuários
>4. **Cadastro de Usuário**
>   - O sistema deve permitir que novos usuários se cadastrem.
>   - O cadastro deve incluir informações como: nome completo, e-mail, senha, telefone, saldo e endereço.
>   - O sistema deve verificar a unicidade do e-mail para garantir que não haja duplicidade.
>
>5. **Login de Usuário**
>   - O sistema deve permitir que os usuários façam login utilizando e-mail e senha.
>   - O sistema deve fornecer uma opção de recuperação de senha.

O sistema é isento de interface e não pretende possibilitar que os usuários se cadastrem ou mesmo que iniciem uma sessão através do login. O que será aproveitado será apenas a não duplicidade de email e os atributos vinvulados ao usuário.
>#### Gerenciamento de Imóveis e Quartos
>6. **Edição e Exclusão de Imóveis e Quartos**
>   - O sistema deve permitir que os proprietários editem ou excluam seus cadastros de imóveis e quartos.
>   - O sistema deve manter um histórico de alterações.
>
>7. **Visualização de Detalhes dos Imóveis e Quartos**
>   - O sistema deve permitir que os usuários visualizem os detalhes completos dos imóveis e quartos cadastrados, incluindo todas as informações e fotos.

O sistema não possuirá a possibilidade de um usuário cadastrado, vulgo proprietário, editar ou cadastrar os imóveis. As demais especificações, o histórico de alterações e a apresentação dos imóveis cadastrados, serão mantidas.
>#### Filtros e Pesquisa
>8. **Filtragem de Imóveis e Quartos**
>   - O sistema deve permitir que os usuários filtrem imóveis e quartos com base em critérios como: localização, preço, número de quartos, tipo de imóvel (casa, apartamento, quarto), entre outros.
>   - O sistema deve permitir a combinação de múltiplos critérios para uma pesquisa mais refinada.
>
>9. **Pesquisa por Palavra-Chave**
>   - O sistema deve permitir que os usuários realizem buscas utilizando palavras-chave relacionadas aos imóveis e quartos.

A filtragem dará-se apenas por fatores como preço, número de quarto e tipo de imóvel, não utilizando a localização. O sistema permitirá a filtragem por apenas um dos critérios. Não haverá busca com palavras-chave.
>10. **Interesse e Contato**
>    - O sistema deve permitir que os usuários manifestem interesse em um imóvel ou quarto.
>    - O sistema deve fornecer opções de contato direto entre o interessado e o proprietário, como e-mail ou telefone.
>
>11. **Favoritos**
>    - O sistema deve permitir que os usuários adicionem imóveis e quartos aos favoritos para uma visualização rápida posterior.

Nada daqui será aproveitado. Não é a proposta do projeto.
>#### Segurança e Privacidade
>12. **Autenticação e Autorização**
>    - O sistema deve garantir que apenas usuários autenticados possam cadastrar e gerenciar imóveis e quartos.
>    - O sistema deve garantir que um usuário não possa editar ou excluir cadastros que não sejam de sua propriedade.
>
>13. **Proteção de Dados**
>    - O sistema deve garantir a proteção dos dados pessoais dos usuários, seguindo as normas de privacidade aplicáveis.
>
>### Funcionalidades Adicionais
>14. **Avaliações e Comentários**
>    - O sistema pode permitir que os usuários avaliem e comentem sobre os imóveis e quartos que visitaram ou alugaram/compraram.
>
>15. **Notificações**
>    - O sistema pode enviar notificações aos usuários sobre novos imóveis e quartos que atendam aos seus critérios de busca ou sobre atualizações importantes relacionadas aos seus cadastros.

Desses requisitos, apenas se utilizará da proteção de dados através de atributos private e protected, manipulados através de métodos. O resto vai além do escopo do projeto.

### Diagrama de Classes
