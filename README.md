# particaodeequivalencia

<p>
A partição de equivalência é uma técnica utilizada em testes de software para reduzir a quantidade de casos de teste necessários para garantir a qualidade do programa. Essa técnica se baseia na ideia de que agrupar valores de entrada em classes de equivalência reduz a redundância dos testes e, ao mesmo tempo, garante a cobertura dos cenários mais relevantes.

O conceito chave é que, se um programa funciona corretamente para um valor em uma classe de equivalência, então ele também funcionará corretamente para qualquer outro valor nessa mesma classe. Por outro lado, se um programa falhar para um valor em uma classe de equivalência, então ele provavelmente falhará para todos os outros valores nessa classe também.

Para aplicar a técnica de partição de equivalência, é necessário identificar os conjuntos de entradas que têm comportamentos semelhantes e agrupá-los em classes. Cada classe deve ser representada por um único valor de teste ou uma faixa de valores. Dessa forma, os casos de teste são selecionados para representar cada classe de equivalência, maximizando a cobertura do software com o mínimo de esforço. Vamos supor que a regra de negócio seja a seguinte:

<h2>Regra de negócio:</h2>

<h3>Um sistema de login só permite acesso a usuários com senhas de 6 a 12 caracteres alfanuméricos (combinação de letras e números).</h3>

<h4>Passo 1:</h4> Identificar a variável de entrada, que neste caso é "SENHA".

<h4>Passo 2:</h4> Faça uma linha reta e informe o nome da variável de entrada definida, no caso "SENHA".
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
             
<h4>Passo 5:</h4> Crie um teste para cada partição. Para a regra de negócio, temos 3 casos de testes.

                       SENHA
        ____________|________________|__________
         Inválidas  |    válidas     | Inválidas
             <6     |    6 a 12      |    >12

<h4>Caso de Teste 1:</h4> Informar uma senha de 5 caracteres alfanuméricos.
Resultado: Senha inválida.

<h4>Caso de Teste 2:</h4> Informar uma senha de 8 caracteres alfanuméricos.
Resultado: Senha válida.

<h4>Caso de Teste 3:</h4> Informar uma senha de 15 caracteres alfanuméricos.
Resultado: Senha inválida.

<h4>Com essa partição de equivalência, temos uma representação clara dos casos de teste para verificar se o sistema de login está se comportando corretamente com base nas restrições da regra de negócio.</h4>
