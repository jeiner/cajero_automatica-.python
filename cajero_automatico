# Online Python compiler (interpreter) to run Python online.
# Write Python 3 code in this online editor and run it.

carga100 = 100
carga50 = 100
carga20 = 100
carga10 = 100
carga_moneda_5 = 100
carga_moneda_2 = 100
carga_moneda_1 = 100
carga_moneda_0_5 = 100
carga_moneda_0_2 = 100
carga_moneda_0_1 = 100


# se define una funcion  con un parametro de entrada el monto que se desea pagar
def sacar_dinero(cantidad):
    global carga50, carga20, carga10, carga100, carga_moneda_5, carga_moneda_2, carga_moneda_1, carga_moneda_0_5, carga_moneda_0_2, carga_moneda_0_1
    if cantidad <= 50 * carga50 + 20 * carga20 + 10 * carga10 + 100 * carga100 + 5 * carga_moneda_5 + 2 * carga_moneda_2 + 1 * carga_moneda_1:
        de100 = int(cantidad / 100)
        cantidad = cantidad % 100
        if de100 >= carga100:  # Si hay suficientes billetes de 50
            cantidad = cantidad + (de100 - carga100) * 50
            de100 = carga100

        de50 = int(cantidad / 50)
        cantidad = cantidad % 50
        if de50 >= carga50:  # Si hay suficientes billetes de 50
            cantidad = cantidad + (de50 - carga50) * 50
            de50 = carga50

        de20 = int(cantidad / 20)
        cantidad = cantidad % 20
        if de20 >= carga20:  # y hay suficientes billetes de 20
            cantidad = cantidad + (de20 - carga20) * 20
            de20 = carga20

        de10 = int(cantidad / 10)
        cantidad = cantidad % 10
        if de10 >= carga10:  # y hay suficientes billetes de 10
            cantidad = cantidad + (de10 - carga10) * 10
            de10 = carga10

        de_5 = int(cantidad / 5)
        cantidad = cantidad % 5
        if de_5 >= carga_moneda_5:  # y hay suficientes billetes de 5
            cantidad = cantidad + (de_5 - carga_moneda_5) * 10
            de_5 = carga_moneda_5

        de_2 = int(cantidad / 2)
        cantidad = cantidad % 2
        if de_2 >= carga_moneda_2:  # y hay suficientes billetes de 5
            cantidad = cantidad + (de_2 - carga_moneda_2) * 10
            de_2 = carga_moneda_2

        de_1 = int(cantidad / 1)
        cantidad = cantidad % 1
        if de_2 >= carga_moneda_1:  # y hay suficientes billetes de 5
            cantidad = cantidad + (de_1 - carga_moneda_1) * 10
            de_1 = carga_moneda_1

        de_0_5 = int(cantidad / 0.5)
        cantidad = cantidad % 0.5
        if de_0_5 >= carga_moneda_0_5:  # y hay suficientes billetes de 5
            cantidad = cantidad + (de_0_5 - carga_moneda_0_5) * 10
            de_0_5 = carga_moneda_0_5

        de_0_2 = int(cantidad / 0.5)
        cantidad = cantidad % 0.5
        if de_0_2 >= carga_moneda_0_2:  # y hay suficientes billetes de 5
            cantidad = cantidad + (de_0_2 - carga_moneda_0_2) * 10
            de_0_2 = carga_moneda_0_2

        de_0_1 = int(cantidad / 0.1)
        cantidad = cantidad % 0.1
        if de_0_1 >= carga_moneda_0_1:  # y hay suficientes billetes de 5
            cantidad = cantidad + (de_0_1 - carga_moneda_0_1) * 10
            de_0_1 = carga_moneda_0_1

        # Si todo ha ido bien, la cantidad que resta por entregar es nula:
        if cantidad == 0:
            # Así que hacemos efectiva la extracción
            carga100 = carga100 - de100
            carga50 = carga50 - de50
            carga20 = carga20 - de20
            carga10 = carga10 - de10
            carga_moneda_5 = carga_moneda_5 - de_5
            carga_moneda_2 = carga_moneda_2 - de_2
            carga_moneda_1 = carga_moneda_1 - de_1

            carga_moneda_0_5 = carga_moneda_0_5 - de_0_5
            carga_moneda_0_2 = carga_moneda_0_2 - de_0_2
            carga_moneda_0_1 = carga_moneda_0_1 - de_0_1

            return [de100, de50, de20, de10, de_5, de_2,de_1, de_0_5, de_0_2, de_0_1 ]
        else:  # Y si no, devolvemos la lista con tres ceros:
            return [0, 0, 0]
    else:
        return [-1, -1, -1, -1, -1, -1, -1, -1, -1 ,-1]


try:
    c = int(input('Ingrese Monto a pagar: '))
    resultado = sacar_dinero(c)
    if resultado == [0, 0, 0]:
        print('No hay desglose de billetes para su importe')
    elif resultado == [-1, -1, -1]:
        print('No hay suficientes billetes')
    else:
        print('Billetes de 100:', resultado[0])
        print('Billetes de 50:', resultado[1])
        print('Billetes de 20:', resultado[2])
        print('Billetes de 10:', resultado[3])
        print('Monedas de 5:', resultado[4])
        print('Monedas de 2:', resultado[5])
        print('Monedas de 1:', resultado[6])
        print('Monedas de 0.5:', resultado[7])
        print('Monedas de 0.2:', resultado[8])
        print('Monedas de 0.1:', resultado[9])
except:
    print('Importe incorrecto')
