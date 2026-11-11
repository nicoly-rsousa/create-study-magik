def_slotted_exemplar - Define o modelo e seus atributos.
new	                 - Cria uma nova instância usando _clone.
init	             - Inicializa os atributos do objeto.
_super	             - Aproveita a inicialização da classe pai.
_self	             - Retorna o próprio objeto.

Você precisa criar um clone de um exemplar quando deseja criar um novo objeto baseado em um exemplar que já existe, mantendo sua estrutura e características, mas podendo trabalhar com valores próprios.


Suponha que você tenha um exemplar chamado pessoa:
DEFINE NOME E IDADE - PARA PESSOA
def_slotted_exemplar(:pessoa,  {
{:nome:_unset},
{:idade:_unset}
})
$

_method pessoa.new(nome,idade)
.nome << nome
.idade << idade
_return _self

RESUMO: 
Herança: um objeto herda características de outro.
Encapsulamento: protege e organiza os dados
Polimorfismo: uma mesma ação pode ter diferentes comportamentos.