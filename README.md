# TP Cuidándonos - Tarea de a pares
## Integrantes

* Jiun Ming Hsu
* Melisa Selene Perez

## Punto 1 
![Diagrama de clases](https://github.com/Melselep/dds-tp-pares/blob/main/img/res-p1.png)

Se utilizo Patron Strategy para configurar las opciones de reaccion ante un incidente. 
![Patron Strategy](https://github.com/Melselep/dds-tp-pares/blob/main/img/patron-strategy.png)

## Punto 2
![Diagrama de clases](https://github.com/Melselep/dds-tp-pares/blob/main/img/res-p2.png)

### Pseudo-codigo de Calculo de tiempo estimado

```
calcular tiempo estimado de Clase Viaje

calcularDemora() {
  tiempoEstimado = tramos
                      .map(tramo -> tramo.calcularDemora())
                      .sumarDuracion()
}
```

```
calcular tiempo estimado de Tramo Sin Espera

calcularDemora() {
  distancia = distanciaEntre(this.direccionPartida, this.direccionLlegada) // calculada por “Distance Matrix API” de Google
  return calcularTiempo(distancia)
}
```

```
calcular tiempo estimado de Tramo Con Espera 

calcularDemora() {
  distancia = distanciaEntre(this.direccionPartida, this.direccionLlegada) // calculada por “Distance Matrix API” de Google
  return calcularTiempo(distancia) + minutosDeEspera
}
```
