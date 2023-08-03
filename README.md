# particaodeequivalencia

<p>
  A partição de equivalência é uma técnica de teste muito útil para definir casos de teste de forma eficiente. Agora, vamos criar a partição de equivalência para uma nova regra de negócio utilizando uma variável diferente. Vamos supor que a regra de negócio seja a seguinte:

<h2>Regra de negócio:</h2>

<h3>Um sistema de login só permite acesso a usuários com senhas de 6 a 12 caracteres alfanuméricos (combinação de letras e números).</h3>

<h4>Passo 1:</h4> Identificar a variável de entrada, que neste caso é "SENHA".

Passo 2: Faça uma linha reta e informe o nome da variável de entrada definida, no caso "SENHA".
</p>
                     
                      
                      SENHA
        _________________________________________

<h4>Passo 3:</h4> Faça os riscos para separar variáveis válidas e inválidas.

                       SENHA
        ____________|________________|__________
         Inválidas  |    válidas     | Inválidas

<h4>Passo 4:</h4> Informe os valores das partições. Conforme a regra de negócio, senhas válidas têm 6 a 12 caracteres alfanuméricos, e senhas inválidas têm menos de 6 ou mais de 12 caracteres.

                       SENHA
        ____________|________________|__________
         Inválidas  |    válidas     | Inválidas
             <6     |    6 a 12      |    >12
             
<h4>Passo 5:</h4> Crie um teste para cada partição. Para a regra de negócio 4, temos 3 casos de testes.

                       SENHA
        ____________|________________|__________
         Inválidas  |    válidas     | Inválidas
             <6     |    6 a 12      |    >12

Caso de Teste 1: Informar uma senha de 5 caracteres alfanuméricos.
Resultado: Senha inválida.

Caso de Teste 2: Informar uma senha de 8 caracteres alfanuméricos.
Resultado: Senha válida.

Caso de Teste 3: Informar uma senha de 15 caracteres alfanuméricos.
Resultado: Senha inválida.

Com essa partição de equivalência, temos uma representação clara dos casos de teste para verificar se o sistema de login está se comportando corretamente com base nas restrições da regra de negócio.
