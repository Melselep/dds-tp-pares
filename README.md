# TP Cuidándonos - Tarea de a pares

## Integrantes

* Jiun Ming Hsu
* Melisa Selene Perez

## Punto 1 
![Diagrama de clases](https://github.com/Melselep/dds-tp-pares/blob/main/img/p-1.png)

Se utilizo Patron Strategy para configurar las opciones de reaccion ante un incidente. 
![Patron Strategy](https://github.com/Melselep/dds-tp-pares/blob/main/img/patron-strategy.png)

## Punto 2
![Diagrama de clases](https://github.com/Melselep/dds-tp-pares/blob/main/img/p-2.png)

### Pseudo-codigo de Cálculo de tiempo estimado

calcular tiempo estimado de la clase `Viaje`

```
calcularDemora() {
  tiempoEstimado = tramos
                      .map(tramo -> tramo.calcularDemora())
                      .sumarDuracion()
}
```

calcular tiempo estimado de la clase `TramoSinEspera`

```
calcularDemora() {
  return DemoraPorDistancia.calcularTiempo(this.direccionPartida, this.direccionLlegada)
}
```

calcular tiempo estimado de la Clase `TramoConEspera` 

```
calcularDemora() {
  return DemoraPorDistancia.calcularTiempo(this.direccionPartida, this.direccionLlegada) + minutosDeEspera
}
```

### Aclaración

Tanto `TramoConEspera` como `TramoSinEspera` utilizan la funcción estática `calcularTiempo`, ya que dicha clase contiene lógica de conversión Distancia a Tiempo. Así también, es la clase que conoce y consume API “Distance Matrix”.
