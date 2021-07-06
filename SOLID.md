## 01. Orientação a Objetos

Qual a melhor definição de uma classe coesa?    
Uma classe que executa bem a sua única tarefa, de forma concisa.  
Cada classe deve ser responsável por apenas uma coisa, e deve executar esta tarefa muito bem

* Uma classe coesa faz bem uma única coisa
* Classes coesas não devem ter várias responsabilidades

Quais das seguintes alternativas estão corretas sobre encapsulamento?  
Getters e setters por si só não fornecem nenhum tipo de encapsulamento.  
O fato de criar getters e setters para tudo, na verdade, quebra o encapsulamento da nossa classe.  
Encapsulamento ajuda no uso correto dos objetos.  
Ao encapsular o acesso a determinados dados, liberando acesso apenas ao necessário, os objetos da nossa classe se tornam
mais fáceis de serem utilizados.

* Getters e setters não são formas eficientes de aplicar encapsulamento
* É interessante fornecer acesso apenas ao que é necessário em nossas classes
* O encapsulamento torna o uso das nossas classes mais fácil e intuitivo

O que é correto afirmar sobre acoplamento?  
É impossível criar um bom sistema sem nenhum tipo de acoplamento.  
É fato que, se estamos organizando o nosso código, seguindo as recomendações da orientação a objetos, algum acoplamento
acontecerá. Algumas classes precisarão de outras, para que não tenham muitas responsabilidades. Cabe a nós medir quando
faz sentido adicionar tal acoplamento com as dependências e como depender do que é seguro, ao invés de classes
concretas.

* Acoplamento é a dependência entre classes
* Acoplamento nem sempre é ruim, e que é impossível criar um sistema sem nenhum acoplamento
* Devemos controlar o nível de acoplamento na nossa aplicação (falaremos mais sobre isso)

## 02. Melhorando a coesão

O que é uma refatoração?  
É uma alteração no código que visa melhorar sua clareza e entendimento Refatorações servem para melhorar o design do
código, e não o funcionamento do sistema. Uma refatoração não deve influenciar em nada no funcionamento.

- Que classes/métodos/funções/módulos devem ter uma única responsabilidade bem definida;
- Que, segundo o Princípio de Responsabilidade Única (SRP), uma classe deve ter um e apenas um motivo para ser alterada;
- Como realizar uma refatoração no nosso sistema, para aplicar o SRP;
- Como extrair uma classe.

## 03. Reduzindo o acoplamento

O Open Closed Principle, embora complexo em sua definição, é muito útil e pertinente. O que podemos fazer para garantir
que nosso sistema seja extensível da forma correta? Garantir que cada ação/responsabilidade esteja na classe correta
Esta é uma das formas de garantir que o sistema seja extensível.

- Que cada classe deve conhecer e ser responsável por suas próprias regras de negócio;
- Que o princípio Aberto/Fechado (OCP) diz que um sistema deve ser aberto para a extensão, mas fechado para a
  modificação
- Isso significa que devemos poder criar novas funcionalidades e estender o sistema sem precisar modificar muitas
  classes já existentes
- Uma classe que tende a crescer "para sempre" é uma forte candidata a sofrer alguma espécie de refatoração.

## 04. Herança indesejada

Sabemos que, ao estender uma classe através da herança, devemos sempre respeitar os contratos (interfaces) de seus
métodos.  
Por que nossa classe Terceirizado estava estendendo de forma indesejada um comportamento?  
Porque estava herdando métodos que não faziam sentido para ela  
Alguns métodos herdados não deveriam existir nessa classe.

Qual seria uma alternativa quando a herança não fizer sentido?  
Utilizar composição.  
Essa é uma das maneiras de evitar a herança sem duplicação de código.

Nesta aula, aprendemos:

- Que, embora a herança favoreça o reaproveitamento de código, ela pode trazer efeitos colaterais quando não utilizada
  da maneira correta;
- Que o Princípio de Substituição de Liskov (LSP) diz que devemos poder substituir classes base por suas classes
  derivadas em qualquer lugar, sem problema.

## 05. Trabalhando com abstrações

Sobre o conceito de Dependency Inversion Principle. Que vantagem temos ao depender de interfaces e não de
implementações? Caso uma determinada implementação mude, não seremos afetados, pois dependemos apenas de sua interface.
Se um método muda a forma como realiza sua tarefa, desde que a interface se mantenha, não vamos precisar nos preocupar
nem em editar o nosso código.

Ao separar as interfaces, implementamos o Interface Segregation Principle.
Qual a definição formal deste princípio?
Classes não devem ser obrigadas a implementar métodos que não irão precisar.
Uma classe não deve ser obrigada a implementar um método de determinada interface, se ele não será útil. 
Para isso, uma interface deverá ser extraída apenas com os métodos necessários.


SOLID
- Que é mais interessante e mais seguro para o nosso código depender de interfaces 
  (classes abstratas, assinaturas de métodos e interfaces em si) do que das implementações de uma classe;  
- Que as interfaces são menos propensas a sofrer mudanças enquanto implementações podem mudar a qualquer momento;
- Que o Princípio de Inversão de Dependência (DIP) diz que implementações devem depender de abstrações e 
  abstrações não devem depender de implementações;
- Que as interfaces devem definir apenas os métodos que fazem sentido para seu contexto;
- Que o Princípio de Segregação de Interfaces (ISP) diz que uma classe não deve ser obrigada a implementar um método que ela não precisa;
- Os conceitos aprendidos neste treinamento formam o acrônimo SOLID: 
  * Single Responsibility Principle
  * Open Closed Principle
  * Liskov Substitution Principle
  * Interface Segregation Principle
  * Dependency Inversion Principle