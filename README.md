# >> Projeto | Explorando Workflows Automatizados com AWS StepFunctions

## O que é o AWS step Functions? 
  - É um **construtor visual** para criar **fluxos de trabalho (Worflows)**. O que isso significa? Basicamente, é um serviço que **facilita a coordenação de aplicativos e microserviços**, usando fluxos de trabalho para **simplificar** e **organizar**. Com ele é possível definir **passo a passo** de como deve ou não funcionar. 
 Ele permite trabalhar com vários serviços da AWS de forma coordenada, como AWS lambda, S3, Dynamo DB, entre outros, para desenvolver aplicações distribuídas e automatizar processos complexos.

## Como ele funciona?
  - Como mecionado anteriormente, você pode criar um fluxo de trabalho para construir aplicativos, automatizar processos e orquestrar microserviços.

    O **Step Function** é baseado em workflows e **tasks (tarefas)**. Cada etapa desse processo é chamado de **estado (state)**. E tudo isso pode ser feito utilizando JSON ou YAML, e pode ser acompanhado por um painel visual no console da AWS. Além disso, é possivel visualizar, editar e depurar esse fluxo de trabalho do aplicativo. Você pode revisar o estado de cada etapa do workflow para garantir que esteja tudo organizado e funcionando confoorme o previsto. O AWS Step functions mostra erros, repetições e etapas que estão em andamento para que você possa desenvolver bem e atingir seu objetivo.
  
      Workflows = série de etapas orientadas a evento.

## Componentes

  1. State Machine (Máquina de estados)
     - Define as etapas e como se conectam.
  2. Estados (States)
     - Etapas individuais dentro do worflow.
     - Cada estado pode realizar uma ação diferente, tomar uma decisão ou apenas passar dados.
     - Há alguns tipos principais de Estados:
     - 
  3. Tasks
     - Ações realizadas dentro dos states, como chamar uma função lamdbda ou enviar uma notificação para o SQS.
  4. Transitions
     - Define a ordem do worflow, com a  informação de qual será o proximo estado depois que outro terminar.
  5. Execution
     - Quantas vezes o fluxo está sendo executado. Um histórico, que mostra os erros e o resultafo final.
  6. Input/Output
     - São os dados que passam de uma etapa para outra durante a execução. 
