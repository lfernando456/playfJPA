Esse é um clone do exemplo de JPA fornecido pelo site oficial do play framework https://developer.lightbend.com/start/?group=play&project=play-samples-play-java-jpa-example

Segundo a documentação do Play os projetos exemplos ja vem com o SBT instalado

![image](https://user-images.githubusercontent.com/17826590/141324768-ceac19b3-0a22-43a3-9ede-4bef596f0ca2.png)


porém após executar o somando .\sbt run obtenho o seguinte erro:


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------


[info] p.c.s.AkkaHttpServer - Listening for HTTP on /0:0:0:0:0:0:0:0:9000

(Server started, use Enter to stop and go back to the console...)

[info] CoffeeScript compiling on 1 source(s)
[ERROR] [11/11/2021 12:35:25.955] [sbt-web-akka.actor.default-dispatcher-3] [akka://sbt-web/user/$a/process] Cannot run program "node": Malformed argument has embedded quote: [[\"C:\\Users\\luisf\\Downloads\\play-samples-play-java-jpa-example\\play-samples-play-java-jpa-example\\app\\assets\\javascripts\\index.coffee\",\"javascripts\\index.coffee\"]]
akka.actor.ActorInitializationException: akka://sbt-web/user/$a/process: exception during creation
        at akka.actor.ActorInitializationException$.apply(Actor.scala:193)
        at akka.actor.ActorCell.create(ActorCell.scala:669)
        at akka.actor.ActorCell.invokeAll$1(ActorCell.scala:523)
        at akka.actor.ActorCell.systemInvoke(ActorCell.scala:545)
        at akka.dispatch.Mailbox.processAllSystemMessages(Mailbox.scala:283)
        at akka.dispatch.Mailbox.run(Mailbox.scala:224)
        at java.util.concurrent.ThreadPoolExecutor.runWorker(Unknown Source)
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(Unknown Source)
        at java.lang.Thread.run(Unknown Source)
Caused by: java.lang.reflect.InvocationTargetException
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(Unknown Source)
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(Unknown Source)
        at java.lang.reflect.Constructor.newInstance(Unknown Source)
        at akka.util.Reflect$.instantiate(Reflect.scala:66)
        at akka.actor.ArgsReflectConstructor.produce(IndirectActorProducer.scala:96)
        at akka.actor.Props.newActor(Props.scala:212)
        at akka.actor.ActorCell.newActor(ActorCell.scala:624)
        at akka.actor.ActorCell.create(ActorCell.scala:650)
        ... 7 more
Caused by: java.io.IOException: Cannot run program "node": Malformed argument has embedded quote: [[\"C:\\Users\\luisf\\Downloads\\play-samples-play-java-jpa-example\\play-samples-play-java-jpa-example\\app\\assets\\javascripts\\index.coffee\",\"javascripts\\index.coffee\"]]
        at java.lang.ProcessBuilder.start(Unknown Source)
        at akka.contrib.process.BlockingProcess.<init>(BlockingProcess.scala:55)
        ... 16 more
Caused by: java.lang.IllegalArgumentException: Malformed argument has embedded quote: [[\"C:\\Users\\luisf\\Downloads\\play-samples-play-java-jpa-example\\play-samples-play-java-jpa-example\\app\\assets\\javascripts\\index.coffee\",\"javascripts\\index.coffee\"]]
        at java.lang.ProcessImpl.needsEscaping(Unknown Source)
        at java.lang.ProcessImpl.createCommandLine(Unknown Source)
        at java.lang.ProcessImpl.<init>(Unknown Source)
        at java.lang.ProcessImpl.start(Unknown Source)
        ... 18 more
  
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

  segundo esse tópico https://github.com/sbt/sbt-js-engine/issues/68 é algo relacionado a versão. 
  
