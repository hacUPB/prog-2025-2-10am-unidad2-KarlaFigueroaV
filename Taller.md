# TALLER

1.  **Verificación de peso de despegue**
    
    En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible.

    |Variables| Tipo|
    |---------|-----|
    |Peso_total| Salida| 
    |Peso_combustible|  Entrada|
    |peso_ carga| Entrada    
    |Peso_aeronave| Entrada|
    |Peso_máximo| Entrada|


    ```
    Inicio
    Leer Peso_combustible, Peso_Carga, Peso_ Aeronave
    Leer Peso_ máximo
    Peso Total = Peso_combustible + Peso_Carga + Peso_Aeronave
    Si Peso_Total < Peso_máximo
        Impirmir "LISTO PARA DESPEGAR"
    Si no 
        Imprimir "REDUCIR CARGA O COMBUSTIBLE"
        Fin si 
    FIN
    ```
3. **Registro de altitudes de vuelo**

    Un sistema debe registrar la altitud de vuelo cada 10 minutos durante una hora y mostrar todas las mediciones al final.
    |Variables| Tipo|
    |---------|----|
    |Tiempo|Entrada|
    |Altitud|Entrada|
    |Mediciones|Salida|
 
    ```
    Inicio
    Definir Altitud[7]
    Desde i=0 hasta i=6
        Escribir "Ingrese la altitud actual"
        Leer dato
        Altitud[i] = dato
    Fin desde
    Escribir "Las altitudes registradas son:"
    Desde i=0 hasta i=6
        Imprimir Altitud[i]
     Fin Desde
    Fin
    ```

7. **Simulación de conteo de pasajeros**
    
    Durante el abordaje, un sistema cuenta a los pasajeros que ingresan. Si el número total supera la capacidad máxima, el sistema debe detener el conteo y mostrar un mensaje de alerta.

    |Variables| Tipo|
    |---------|-----|
    |Cantidad_Pasajeros| Entrada|
    |Cantidad_máxima_Pasajeros| Entrada|
    |Cantidad_Pasajeros| Control|

    ```
    Inicio
    Cantidad_Pasajeros = 0
    Leer Cantidad_máxima_pasajeros
    Mientras Cantidad_pasajeros < Cantidad_máxima_pasajeros
        Cantidad_pasajeros = cantidad_pasajeros + 1
            Si Cantidad_pasajeros > cantidad_máxima_pasajeros
                Imprimir "HA SUPERADO LA CANTIDAD MÁXIMA"
            Si no 
            Imprimir Cantidad_pasajeros
        Fin si
    Fin mientras
    Cantidad_pasajeros <= Cantidad_máxima
    Fin      
