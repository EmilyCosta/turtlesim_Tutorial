# Tutorial Turtlesim

## Rodar o servidor

Antes de qualquer comando ser dado no ambiente do ros, é necessário rodar o servidor:

```Shell
roscore
```
Ele vai ficar rodando em um terminal durante todo o tempo que será trabalhado com o ros

## Rodar o nó

Em outro terminal rodar o nó do turtlesim

```Shell
rosrun turtlesim turtlesim_node
```
o turtlesim é o pacote e turtlesim_node o nó


## Topicos publicados 

Assim que esse nó for rodado algum tópicos serão publicados e podem ser verificados com o comando em um terceiro terminal:

```Shell
rostopic list
```

Também é possivel verificar o tipo de mensagem que está sendo publicada / lida em cada tópico 

```Shell
rostopic type <topico> 
rostopic type /turtle1/cmd_vel 
```

Para mais informações pode-se usar o comando abaixo

```Shell
rostopic info <topico> 
rostopic info /turtle1/cmd_vel 
```

Para vizualiar os dados que estão dentro dos tópicos pode-se utilizar:

```Shell
rostopic echo <topico> 
rostopic echo /turtle1/cmd_vel 
```

## Rodar um segundo nó

Agora em outro terminal pode-se rodar outro nó do mesmo pacote que permite o controle da tartaruga pelo teclado

```Shell
rosrun turtlesim turtle_teleop_key
```