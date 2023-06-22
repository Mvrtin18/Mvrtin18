Op=0
OpDoc=0
SiNo=0
DatosVehiculos=[]
Multa=[]
Doc=[]
OpEmi=0
mult=0
print("-----------------------------------------")
print("Bienvenido a Auto Seguro ")
print("----------------------------------------")
while Op<1 or Op>=5:
 print("Ingrese lo que desea realizar:")
print("1) Grabar un vehiculo")
print("2) Buscar un vehiculo")
print("3) Imprimir certificado")
print("4) Salir del sistema")
Op=int(input("Ingrese una opcion: "))
if Op==1:
 print("----------------------------------------")
print("Bienvenido al sistema de grabado de Vehiculos")
print("----------------------------------------")
Tipo=str(input("Ingrese el tipo de vehiculo: "))
Patente=str(input("Ingrese la patente del vehiculo sin guiones ni puntos: "))
Marca=""
while len(Marca)<2 or len(Marca)>15:
Marca=str(input("Ingrese la marca del vehiculo: "))
Precio=0
while Precio<=5000000:
Precio=int(input("Ingrese el precio del vehiculo: "))
FechaRegVeh=int(input("Ingrese la fecha de registro de su vehiculo (Utilize el siguiente formato /dia/mes/año): "))
NomDueño=int(input("Ingrese el nombre del dueño del vehiculo: "))
while SiNo<1: or SiNo>2:
SiNo=int(input("¿Usted tiene alguna multa? \n1)Si\n2)No\n"))
if SiNo==1:
 MontoM=(input("Ingrese el monto de su multa: "))
FechaM=(input("Ingresa la fecha de la multa: (dia/mes/año) "))
Multa=[FechaM,MontoM]
 Multa.append(Multa)
 OtraM=int(input("¿Usted tiene otra multa? \n1)Si\n2)No\n"))
if OtraM==1:
MontoM=""
FechaM=""
SiNo=0
elif Otram==2:
          print("multas ingresadas")
elif SiNo==2:
print(".")
Vehiculo=[Tipo,Patente,Marca,Precio,FechaRegVeh,NomDueño,Multas]
DatosVehiculos.append(Vehiculo)
Op=0
elif Op==2:
print("----------------------------------------")
print("Bienvenido al buscador de vehiculos")
print("----------------------------------------")
BusquedaPatente=input("Ingrese la patente del vehiculo a buscar(Debe ser sin guionesni puntos): ")
VehEncontrado=None
for Vehiculo in DatosVehiculos:
if Vehiculo[1]==BusquedaPatente:
VehEncontrado=Vehiculo 
break
if VehEncontrado is not None:
print("Vehiculo encontrado: ")
print("Tipo: {VehEncontrado[0]}")
print("Patente: {VehEncontrado[1]}")
print("Marca: {VehEncontrado[2]}")
print("Precio: {VehEncontrado[3]}")
print("Fecha de Registro: {VehEncontrado[4]}")
print("Nombre del dueño: {VehEncontrado[5]}")
print("Multas: {VehEncontrado[6]}")
else:
print("Vehiculo no encontrado")
elif Op==3:
print("----------------------------------------")
print("Bienvenido al visor y imprimidor de certificados de vehiculos")
print("----------------------------------------")
BusquedaPatente=input("Ingrese la patente del vehiculo del cual desea tener los certificados:")
VehEncontrado=None
for Vehiculo in DatosVehiculos:
if Vehiculo[1]==BusquedaPatente:
VehEncontrado=Vehiculo
break
  if VehEncontrado is not None:
while OpDoc<1 or OpDoc>=5:
print("Que archivo desea imprimir:")
print("1)Emision de contaminantes $1500")
 print("2)Anotaciones vigentes $2000")
print("3)Multas $3500")
Opdoc=int(input("Ingrese el documento que desea impirmir: "))
if Opdoc==1:
EmiDoc=(f"Emision de contaminantes:\nFechaReg: {VehEncontrado[4]}\nDueño:
{VehEncontrado[5]}\nTipo: {VehEncontrado[0]}\nPatente: {VehEncontrado[1]}\nMarca:
{VehEncontrado[2]}\n Sello verde:APROBADO\n")
Doc.append(EmiDoc)
 while OpEmi<1 or OpEmi>=3:
 print("¿Desea sumar otro documento o imprimir el ya seleccionado?
\n1)Si\n2)No")
 OpEmi=int(input())
 if OpEmi==1:
OpDoc=0
 if OpEmi==2:
print("Gracias por utilizar este sistema")
 if OpDoc==2:
AnoVig=(f"Anotaciones Vigentes:\nFechaReg: {VehEncontrado[4]}\nDueño:
{VehEncontrado[5]}\nTipo: {VehEncontrado[0]}\nPatente: {VehEncontrado[1]}\nMarca:
{VehEncontrado[2]}\n")

Doc.append(AnoVig)
104 while OpEmi<1 or OpEmi>=3:
105 print("¿Desea sumar otro documento o imprimir el ya seleccionado?
\n1)Si\n2)No")
 OpEmi=int(input())
 if OpEmi==1:
 OpDoc=0
 if OpEmi==2:
 print("Gracias por utilizar este sistema")
 if Opdoc==3:
 print("Multas:\n")
 mult=1
 while OpEmi<1 or OpEmi>=3:
 print("¿Desea sumar otro documento o imprimir el ya seleccionado?
\n1)Si\n2)No")
 OpEmi=int(input())
 if OpEmi==1:
 OpDoc=0
  if OpEmi==2:
 print("Gracias por utilizar este sistema")
 print(Doc)
 if mult==1:
 print(VehEncontrado[6])
 else:
 print("Vehiculo no encontrado")
 Op=3
 Op=0
 elif Op==4:
     print("Muchas gracias por utilizar este sistema!!")
