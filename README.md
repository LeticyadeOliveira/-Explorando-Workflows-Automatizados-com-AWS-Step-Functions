# >> Projeto | Explorando Workflows Automatizados com AWS StepFunctions

## O que é o AWS step Functions? 
  - É um **construtor visual** para criar **fluxos de trabalho (Worflows)**. O que isso significa? Basicamente, é um serviço que **facilita a coordenação de aplicativos e microserviços**, usando fluxos de trabalho para **simplificar** e **organizar**. Com ele é possível definir **passo a passo** de como deve ou não funcionar. 
 Ele permite trabalhar com vários serviços da AWS de forma coordenada, como AWS lambda, S3, Dynamo DB, entre outros, para desenvolver aplicações distribuídas e automatizar processos complexos.

## Como ele funciona?
  - Como mecionado anteriormente, você pode criar um fluxo de trabalho para construir aplicativos, automatizar processos e orquestrar microserviços.

    O **Step Function** é baseado em workflows e **tasks (tarefas)**. Cada etapa desse processo é chamado de **estado (state)**. E tudo isso pode ser feito utilizando JSON ou YAML, e pode ser acompanhado por um painel visual no console da AWS. Além disso, é possivel visualizar, editar e depurar esse fluxo de trabalho do aplicativo. Você pode revisar o estado de cada etapa do workflow para garantir que esteja tudo organizado e funcionando conforme o previsto. O AWS Step functions mostra erros, repetições e etapas que estão em andamento para que você possa desenvolver bem e atingir seu objetivo.
  
      Workflows = série de etapas orientadas ao evento.

## Componentes

  1. State Machine (Máquina de estados)
     - Define as etapas e como se conectam.
  2. Estados (States)
     - Etapas individuais dentro do workflow.
     - Cada estado pode realizar uma ação diferente, tomar uma decisão ou apenas passar dados.
  3. Tasks
     - Ações realizadas dentro dos estados, como chamar uma função lamdbda ou enviar uma notificação para o SQS.
  4. Transitions
     - Define a ordem do workflow, com a  informação de qual será o proximo estado depois que outro terminar.
  5. Execution
     - Quantas vezes o fluxo está sendo executado. Um histórico, que mostra os erros e o resultafo final.
  6. Input/Output
     - São os dados que passam de uma etapa para outra durante a execução.

  - Tipos principais de States no AWS Step Functions:
    
    | Tipo de State | Função |
    | ------------- | ------ |
    | Choice | Responsável por decisões condicionais (if/else). | 
    | Fail   | Responsável por encerrar o fluxo em caso de erro. |
    | Map | Responsável por repetir etapas para vários itens, como se fosse um loop. |
    | Parallel | Responsável por executar passos do workflow em paralelo. |
    | Pass | Responsável por repassar informações, mas não executa nada. |
    | Succeed | Finaliza o workflow com êxito. |
    | Wait | Pausa por um período específo (O usuário da Aws escolhe por quanto tempo, especificando em segundos ou como tempo final absoluto, um "timestamp"). |

### Quais são os tipos de workflows no AWS Step Functions?

   - > **Standard Workflows: É mais indicado para processos longos e complexos. Porque mostram o histórico de execução e a depuração de forma visual. A execução é única e pode durar até um ano. Pode ser ideal para fluxos de negócio, processamento de dados e automações.**
  
  - > **Express Workflows: Indicado para cargas de trabalho com alta taxa de eventos. Porque eles tem execução de trabalho pelo menos uma vez e podem durar até 5 minutos, indicando que um ou mais passos podem ser executados mais de uma vez, dentro de um mesmo fluxo. Ideal para o processamento de dados em tempo real, como streaming, funções back-end e entre outros.**

### Quais são as vantagens de utilizar o Step functions? 

   - **Simplificação do código, permitindo criar workflows com pouco código (Low-Code).**
  
   - **Integração com outros serviços da AWS.**
  
   - **Resiliência com tratamento de erros.**
  
   - **Automatizar processos complexos de uma forma intuitiva.**
  
   -  **Criação de fluxos visuais.**

### Casos de uso
  
   1. Processamento de dados em várias etapas.
   2. Gerenciar pedidos dentro de um e-commerce.
   3. Automação de TI.

 ● Existem outras formas de casos de uso também, **a plataforma disponibiliza modelos para diferentes aplicações** nos quais você pode trabalhar ou se basear para criar o seu própio fluxo de trabalho. 

### Considerações finais
Conclui-se que o **AWS Step Functions** é uma ferramenta útil e eficiente, voltada tanto para desenvolvedores quanto para estudantes e empresas. Por meio dela, é possível simplificar processos e visualizar o funcionamento de cada componente dentro da nuvem, compreendendo de forma mais clara suas funções e interações entre si. Uma forma interessante de aprender tentando, visto que ele mostra os erros, acertos e descreve de forma detalhada como o fluxo está funcionando.

#### Referências
[Documentação oficial da AWS](https://aws.amazon.com/pt/step-functions/)\
[Casos de uso AWS Step functions](https://docs.aws.amazon.com/step-functions/latest/dg/use-cases.html)\
[O que é o Step functions?](https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html)

  
