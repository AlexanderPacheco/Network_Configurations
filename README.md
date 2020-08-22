# Reporte de configuracion

> A continuacion se detalla las configuraciones para el siguiente modelo.

![](https://github.com/alexdevep/Recursos/blob/master/modelo.JPG)

## Configurando Router

> A continuacion se detallan los comandos de la configuracion del router.

> Inicialmente ingresamos este comando, para verificar que realmente no tengamos IP asignada al router

```javascript
Router#sh ip interface brief
```

> Con este comando inicializamos la configuracion del terminal
```javascript
Router#configure terminal
```

> Establecemos el tipo de comunicacion del router
```javascript
Router(config-if)#duplex full
```


> Establecemos la direccion IP y mascara de red
```javascript
Router(config-if)#ip address 192.168.10.254 255.255.255.0
```


> Este comando hace que no se apague el router
```javascript
Router(config-if)#no shutdown
```


> Finalizamos la configuracion
```javascript
Router(config-if)#exit
```

> Para configurar el otro puerto se hace el mismo procedimiento :star:

> Al Finalizar ingresamos este comando y verificamos si nuestros cambios fueron realizados
```javascript
Router(config)#interface fastEthernet 0
```

![](https://github.com/alexdevep/Recursos/blob/master/r2.JPG)

![](https://github.com/alexdevep/Recursos/blob/master/r1.JPG)


## Configurando Host Linux

> A continuacion se detalla la configuracion del host de linux

> Al ser un Tiny Linux podemos configurar la IP, Mask y Broadcast de manera grafica, lo cual es mucho mas sensillo, aplicando cambios

![](https://github.com/alexdevep/Recursos/blob/master/p1.JPG)

> Para ver que realmente se actualizo la configuracion, abrimos la terminal e ingresamos el comando

```javascript
$ ifconfig
```

> Automaticamente despues de ingresar el comando nos despliega la configuracion en consola

![](https://github.com/alexdevep/Recursos/blob/master/p2.JPG)

### Conexion Host de Linux

> Para probar la conexion del Host Linux con las otras vpcs abrimos la terminal y escribimos

```javascript
$ ip <direccion deseada>
"Ejemplo de prueba"
$ ip 192.168.14.15
```

## Configurando VPCS

> Para configurar las vpcs unicamente necesitamos de un comando, el cual seria 

```javascript
$ ip <IP_Address> <Mask> <Gateway>
```

> Podemos ingresar el comando tal como vimos anterior mente o simplemente obviando la mascara, y obtenemos el mismo resultado

```javascript
$ ip <IP_Address>/24 <Gateway>
```

```javascript
"Forma #1"
$ ip 192.168.14.30 255.255.255.0 192.168.14.254
"Forma #2"
$ ip 192.168.14.30/24 192.168.14.254
```

> Para ver la configuracion de nuestras vpcs basta con ingresar el siguiente comando

```javascript
PC2> show ip
```

> Para probar nuestra conexion con otras vpcs, ingresamos el siguiente comando

```javascript
PC2> ping <IP_Address>

"Ejemplo"
PC2> ping 192.168.16.30
```

### Conexion Host de Linux

> Detalle de configuracion y prueba de VPC 1

![](https://github.com/alexdevep/Recursos/blob/master/p4.JPG)

> Detalle de configuracion y prueba de VPC 2

![](https://github.com/alexdevep/Recursos/blob/master/p5.JPG)

> Detalle de configuracion y prueba de VPC 3

![](https://github.com/alexdevep/Recursos/blob/master/p6.JPG)


## Glosario

### Conexion Host de Linux

+ First item
+ Second item
+ Third item
+ Fourth item 


:star: Gracias por visitarnos! Cienazo!! :star:
