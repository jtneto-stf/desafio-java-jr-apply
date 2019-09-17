# Seleção Dev Java
Se você chegou até aqui é porque se interessou em fazer parte do nosso quadro de funcionarios. Como temos muitas oportunidades para você colocar a mão na massa, queremos ver como você se sai com o cenário abaixo, por meio do qual conseguiremos avaliar várias de suas competências.

## A demanda
Deverá ser criada uma aplicação de cadastro de **autores** e **obras**, seguindo as regras de relacionamento abaixo:
 - Cada autor poderá ter 0 (zero) ou n obra(s);
 - Cada obra deverá ter 1 (um) ou n autor(es);
 - A partir de uma obra deverá ser posível acessar o(s) autor(es);
 - A partir de um autor deverá ser possível acessar a(s) obra(s).

###  1) Back-end
A aplicação, a ser desenvolvida em Java, deverá expor uma API REST de cadastro, alteração, remoção e consulta de **autores** e **obras** com as seguintes propriedades básicas definidas para cada entidade:

#### Autor
 - Nome - obrigatório
 - Sexo
 - E-mail - não obrigatório, deve ser validado caso preenchido (não pode haver dois cadastros com mesmo e-mail)
 - Data de nascimento - obrigatório, deve ser validada
 - País de origem - obrigatório (deve ser um país existente)
 - CPF - somente deve ser informado caso país de origem seja o Brasil, desta forma torna-se obrigatório. Deve ser validado (formatado e não pode haver dois cadastros com mesmo CPF)

#### Obra
 - Nome - obrigatório
 - Descrição - obrigatório (deve conter no máximo 240 caracteres)
 - Data de publicação - obrigatória caso a data de exposição não seja informada (é utilizada mais para livros e demais publicações escritas)
 - Data de exposição - obrigatória caso a data de publicação não seja informada (é utilizada mais para obras que são expostas, como pinturas, esculturas e demais)
 
##### Obs.: a data de publicação e a data de criação não podem ser nulas ao mesmo tempo, devendo sempre uma ou outra ser informada.

### 2) Front-end
A aplicação deverá ser acessível via navegador e possuir telas com formulários para cadastro de autores e obras. 

 - Na tela de cadastro e edição dos **autores**, além de informar seus atributos básicos, deverá ser possível associar qual(is) **obra(s)** (cadastradas no sistema) são de sua autoria.
 - Na tela de cadastro e edição das **obras**, além de informar seus atributos básicos, deverá ser possível associar seu(s) **autor(es)** (cadastrados no sistema).

##### Regras de exclusão
 - **Autor**: somente pode ser excluído caso não possua **obras** associadas.
 - **Obra**: não há restrição para exclusão.

Não há restrição em relação à tecnologia para o desenvolvimento do front-end.

### 3) Código fonte
 Todo o código fonte da aplicação deverá estar em um repositório Git de sua preferência (Github, Gitlab ou outro).
 
## Extras
Se você possui conhecimento um pouco mais avançado, pode implementar as tarefas abaixo que serão consideradas como diferencial na sua análise. Atente-se para o prazo de entrega ;)
* **Extra 1 (deploy/hospedagem):** tornar a aplicação disponível em algum ambiente de nuvem, como o Heroku:
  * Não deverá ser necessária nenhuma configuração por parte do usuário para usar a aplicação, bastando apenas acessar a URL onde o sistema está hospedado.
  * O sistema deve estar funcional ao ser acessado.
* **Extra 2 (autenticação/segurança):** implementar algum tipo de autenticação, como a **basic** ou outra de sua preferência (o usuário pode ser fixo no banco, caso prefira, não precisando que a aplicação envolva a criação de uma conta).
* **Extra 3 (testes):** implementar testes de unidade utilizando JUnit. Os testes devem contemplar as operações abaixo validando as restrições informadas anteriormente:
  * **Inserção**: validar regras informadas anteriormente (ex.: obrigatoriedade dos campos em cada situação).
  * **Edição**: manter a consistência garantida anteriormente na inserção, impedindo que a entidade seja modificada para um estado inválido (ex.: obra sem autor).
  * **Consulta**: validar os dados retornados do service (pode-se utilizar mock's).
  * **Exclusão**: validar regras de exclusão informadas anteriormente.

## Prazo e retorno
Isso será combinado com quem você fez a entrevista. Você terá tempo para entender o cenário e nos retornar um prazo.
Lembre-se: prazo dado é prazo cumprido.

Boa sorte!
