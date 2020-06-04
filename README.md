#  Diagrama casos de uso Cajero Automático 

### Raúl Eduardo Pachón Alarcón - 20171020167 

## Objetivo: 

_En este repositorio se realiza descripcion del funcionamiento y la interaccion basica de un usuario con un cajero automatico_

#### Diagrama de casos de uso 

![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/UseCaseCAJERO.jpg)

#### Diagrama de clases

![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/diagrama_de_clases_Cajero.jpg)

#### Diagrama de Actividades

![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/SequenceRetiro.jpg)
![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/SequenceDiagramTransferencia.jpg)
![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/SequenceDiagramDeposito.jpg)
![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/SequenceDiagramConsulta.jpg)

#### Modelo de análisis a partir de los casos de uso

![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/modeloAnalisis.jpg)
![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/modeloAnalisis2.jpg)

#### Modelo de diseño a partir del modelo de análisis

![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/modeloDiseño.jpg)
![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/modeloDiseño2.jpg)
![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/modeloDiseño3.jpg)

#### Modelo de implementación a partir del modelo de diseño

![imagen referencia](https://github.com/raulpachon/casos-de-uso-Cajero/blob/master/modeloImplementacion.jpg)

#### Prueba de casos de uso
##### prueba 1
###### Entradas:
- La cuenta 12-121-1211 del Cliente de Banco tiene un saldo de $500
- El Cliente de Banco se identifica correctamente
- El Cliente de Banco solicita la transferencia de $200 de la cuenta 12-121-1211 a la cuenta 12-132-1240
- Hay suficiente dinero en el Cajero Automático

###### Resultados
- El saldo de la cuenta 12-121-1211 disminuye a 300 \$
- El saldo de la cuenta 12-132-12401 aumenta en 200 \$

###### Condiciones
- No se permite que ningún otro caso de uso (instancias de) acceda a la cuenta 12-121-1211 durante la ejecución del caso de prueba.
- El proceso de retiro de una cuenta y depósito en otra es una única operación, en caso de fallar una de las dos partes se revierte el    proceso. 

##### prueba 2
###### Entradas:
- La cuenta 12-121-1211 del Cliente de Banco tiene un saldo de $500
- El Cliente de Banco se identifica correctamente
- El Cliente de Banco solicita la transferencia de $600 de la cuenta 12-121-1211 a la cuenta 12-132-1240
- Hay suficiente dinero en el Cajero Automático

###### Resultados
- El saldo de la cuenta 12-121-1211 no se altera
- El saldo de la cuenta 12-132-12401 no se altera

###### Condiciones
- No se permite que ningún otro caso de uso (instancias de) acceda a la cuenta 12-121-1211 durante la ejecución del caso de prueba.
- El proceso de retiro de una cuenta y depósito en otra es una única operación, en caso de fallar una de las dos partes se revierte el    proceso


##### prueba 3
###### Entradas:
- La cuenta 12-121-1211 del Cliente de Banco tiene un saldo de $500
- El Cliente de Banco se identifica correctamente
- El Cliente de Banco solicita la transferencia de $200 de la cuenta 12-121-1211 a la cuenta 12-132-1240
- No hay suficiente dinero en el Cajero Automático

###### Resultados
- El saldo de la cuenta 12-121-1211 disminuye a 300 \$
- El saldo de la cuenta 12-132-12401 aumenta en 200 \$

###### Condiciones
- No se permite que ningún otro caso de uso (instancias de) acceda a la cuenta 12-121-1211 durante la ejecución del caso de prueba.
- El proceso de retiro de una cuenta y depósito en otra es una única operación, en caso de fallar una de las dos partes se revierte el    proceso

_diagramas realizados con starUML_
