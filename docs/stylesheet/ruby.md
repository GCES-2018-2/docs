
## SUMÁRIO
1. [Declaração de classes, funções e variáveis](#head1)<br />
2. [Identação chaves e colchetes](#head2)<br />
3. [Rotas](#head3)<br />
4. [Comentários](#head4)<br />

### Considerações gerais
Todos os nomes de variáveis, métodos, rotas, classes e funções devem ser em inglês <br>
Comentários devem ser um português

<a name="head1"></a>
## 1. Declaração de classes, funções e variáveis:
###### [Summary](#summary1)

### 1.1. Declaração de clases
Classes sempre começam com letra maiúscula e em caso de uma classe com nome composto usa-se camel case <br>
Exemplos:

```ruby
class CompanyDenunciation < ActiveRecord::Base
end
```
```ruby
class Notification < ActiveRecord::Base
end
```

### 1.2. Depois da declação da classe
Depois da declação da classe e suas dependências deve-se pular uma linha para escrever os métodos.
<br>
Exemplos:

```ruby
class CommentsController < ApplicationController
  before_action :authenticate_user
  before_action :verify_user_permission, only: [:destroy, :edit]

  def new
     @comment = Comment.new
  end

...

end
```

### 1.3. Declaração de atributos:
Exemplos:

```ruby
has_many :active_battles
has_many :passive_battles
has_many :won_battles
```

### 1.4. Declaração de variáveis e métodos/funções
Nunca abreviar os nomes e sempre separar nomes compostos por _ (underline)
<br>
Exemplos:

```ruby
@battle_answer_notification
@pending_battles
```

```ruby
def um_exemplo
  @meu_metodo
end
```
### 1.5. Variáveis para lops
Variáveis dentro de lops devem sempre corresponder ao singular do nome do array (que deve ser composto)<br>
Exemplos:

```ruby
  def read
    
    render :nothing => true
    @notifications = current_user.notifications.where(visualized: false)
    @notifications.each do |notification|
       notification.update_attribute(:visualized, true)
    end
  
  end
```
<a name="head2"></a>
## 2. Identação chaves e colchetes
###### [Summary](#summary2)

Identação sempre com 2 espaços.<br>
Parênteses e colchetes sempre na mesma linha.<br>
Chaves sempre separadas do conteúdo por um espaço.
<br>Exemplos:

```ruby
def update
  @vote = Vote.new(vote_params)
  @vote.question_id = params[:question_id]
  @vote.option_id = params[:vote][:option_id]
  @votes.each do |vote|
    vote.description = nil
  end

  if @vote.save
    redirect_to "/questions/#{ @vote.question_id }/results" 
  end 

end
```

<a name="head4"></a>
## 3. Rotas:
###### [Summary](#summary3)
Rotas devem sempre começar com letra minúscula<br>
Os nomes devem ser intuitivos e em inglês<br>
Exemplos:

```ruby
#questions
  get 'questions/humans' => 'questions#humans'
  get 'questions/languages' => 'questions#languages'
  get 'questions/math' => 'questions#math'
  get 'questions/nature' => 'questions#nature'
  get 'questions/recommended' => 'questions#recommended'
  get 'questions/upload' => 'questions#new'
  post 'questions/upload_questions'
  post 'questions/upload_candidates_data'
```

<a name="head6"></a>
## 4. Comentários:
###### [Summary](#summary4)
Os comentários devem sempre de acordo com a identação.<br>
Devem começar com letra maiúscula.<br>
Devem estar em português.

```ruby
  # Meu exemplo de comentário
  # Continua meu exemplo de comentário
  
```


