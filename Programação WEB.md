### ✨ Como funciona o método de envio de dados GET?
O metodo get usa sua propria URL para enviar os dados ao servidor, ou seja, quando um formulario é enviado pelo GET, o navegador pega as informações contidas no formulario e coloca junto com a sua URL de origem.

Exemplo de uma URL:

http://site.com/teste?nome=valor

O ponto de interrogação (?), significa o inicio da separação dos dados do formulario.
Nome seria o propriamente dito, o que foi inserido no codigo HTML e o valor seria o dado enviado.

Exemplo do campo no código HTML:

<form action="nomeDestino.php" method="get">

### ✨ Quais são as diferenças entre o método GET e POST? Qual é o melhor?

As diferenças entre GET e POST é no envio de informações, GET é usado para pegar os dados e POST é usado para postar os dados.

POST é mais seguro que o método GET pois as informações inseridas nunca ficam visiveis na URL, ou seja, ficam encapsulados, diferente do GET.

Outras diferenças entre o POST e GET é que o POST permite o envio de caracteres especiais, além de ter um limite maior na quantidade de dados que pode transmitir e pode-se enviar dados de texto, tal como dados binarios (fazer um upload de arquivo).

O melhor método depende do objetivo: Caso queira enviar arquivos e tratar de dados sensíveis como senhas, telefones, documentos pessoais, numeros de cartões de crédito, o POST é o mais aconselhável, caso contrário somente o GET já é o suficiente.

Onde Eu informo o destino para recebimento de dados de um formulário. Traga exemplo de código.

O destino precisa ser informado dentro do código HTML, especificamente em um atributo do <form> que se chama <action>, nele colocaremos o nome do arquivo PHP que será o nosso destino, exemplo abaixo:

`<form   action="nomeDestino.php" method="post" enctype="multipart/form-data">`
</form>

### ✨ O que devo me preocupar para garantir que os dados e arquivos sejam corretamente enviados para o destino?

Além de colocar o nome do destino no código HTML, dado pelo campo form action="nomeDestino", é necessário descrever o método, pois dependendo do método utilizado no formulário, as informações chegam na matriz $_GET ou $_POST.

O que devo me preocupar para enviar arquivos do formulário?

Certificar que o enctype="multipart/form-data" está presente, pois somente com ele o método post é possível o envio de arquivos.

### ✨ Onde chegam os dados e arquivos que foram coletados no formulário (PHP/Servidor)?
Dê alguns exemplos.

Eles chegam em navegadores, tais como: Mozilla Firefox, Google Chrome, Opera, Edge...

### ✨ O que devo me preocupar para enviar e receber arquivos (do formulário e no PHP/Servidor)?

Primeiramente, confirmar se o código HTML, o PHP e o SQL está sincronizado e formulado corretamente, se o método (GET ou POST) foi inserido, e caso tenha utilizado o POST, verificar se o atributo enctype="multipart/form-data" está presente.

---
