# Desafios

##### Links para os repositórios dos desafios e descrição

* [Link com projeto do módulo] (https://github.com/TalitaRamos/DigiOneBank)

* [Link com testes de arrays e coleções] (https://github.com/TalitaRamos/api-collections)

* [Link com o app Simulador de partidas] (https://github.com/TalitaRamos/simulator-matches-bootcamp)

* [Link com o simulador de API para o app de Simulação de Partidas] (https://github.com/TalitaRamos/matches-simulater-api)

##### Desafios de código

# Desafios

## Desafio 1

```
fun main() {
    var reader = Scanner(System.`in`)

    var a = reader.nextDouble()
    var b = reader.nextDouble()
    
    var weightA = 3.5
    var weightB = 7.5
    var totalWeight = 11

    var m = (a * weightA + b * weightB) / totalWeight

    var r = "%.5f".format(m)

    println("MEDIA = ${r}")
}
```

## Desafio 2

```
fun main() {
   val v = readLine()!!.toInt()
   val a = IntArray(10).toMutableList()
    
    for (i in 0 until  a.size) {
        a[i] = if(i == 0) v
        else a[i-1] * 2
    }
    for (k in  0 until  a.size) { println("N[$k] = ${a[k]}") }
}
```
## Desafio 3

```
fun main() {
    val notas: IntArray = intArrayOf(100, 50, 20, 10, 5, 2, 1)
    var valor = readLine()!!.toInt()

    println(valor)

    for (i in 0..(notas.size - 1)) {
        if (valor >= notas[i]) {

            println("${valor / notas[i]} nota(s) de R$ " + notas[i] + ",00")
        } else {
            println("0 nota(s) de R$ " + notas[i] + ",00")
        }
        valor = valor % notas[i]
    }
}
```

## Desafio 4

```
fun main() {
   val input = readLine()!!
  
  val a = input.split(" ")[0].toFloat()
  val b = input.split(" ")[1].toFloat()
  val c = input.split(" ")[2].toFloat()
 
  val perimetro = a + b + c
  val area = ((a+b)*c)/2
  
  if (a < (b + c) &&  b < (a + c) &&  c < (a + b)){
      println(String.format("Perimetro = %.1f", perimetro))
  }else{
     println(String.format("Area = %.1f",area))
  } 
}
```

## Desafio 5

```
fun main() {
   
}
```

