# Desafios

##### Links para os repositórios dos desafios e descrição

* [Link com projeto do módulo](https://github.com/TalitaRamos/DigiOneBank)

* [Link com testes de arrays e coleções](https://github.com/TalitaRamos/api-collections)

* [Link com o app Simulador de partidas](https://github.com/TalitaRamos/simulator-matches-bootcamp)

* [Link com o simulador de API para o app de Simulação de Partidas](https://github.com/TalitaRamos/matches-simulater-api)

* [Link com o app Soccer News](https://github.com/TalitaRamos/SoccerNewsDio)

* [Link com o simulador de API para o app Soccer News](https://github.com/TalitaRamos/soccer-news-api)

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
   for(i in 1..3) {
    val l = readLine()!!.toInt()
    val v = readLine()!!.split(" ")
    
    var maior = 0
    for (a in 0..l-1){
      if (v[a].toInt() > maior) maior = v[a].toInt()
    }
    
    if(maior < 10) println("1")
    else if (maior > 10 && maior < 20) println("2")
    else println("3")
   }
}
```

## Desafio 6

```
fun main() {
   val n = readLine()!!.toInt()
    var a = 0
    var b = 1

    for (i in 1..(n -1)) {
        print("$a ")

        val sum = a + b;
        a = b;
        b = sum;
    }
    println("$a")
}
```
## Desafio 7

```
fun main() {
    val nTestes = readLine()!!.toInt()
    var i = 0

    while (i < nTestes){
        var cont = 0
        while (cont == 0) {
            var raios = readLine()
            var raiosArray: List<String> = raios!!.split(" ")
            var r1 = raiosArray[0]
            var r2 = raiosArray[1]
            println(String.format("%d",r1.toInt()+r2.toInt()))
            cont++
        }
        i++
    }
}
```

## Desafio 8

```
fun main() {
   val N = readLine()!!.toInt()
    for (i in 1..N) {
        var str = readLine()!!
        var N1 : Int = str.substring(0, 1).toInt()
        var N2 : Int = str.substring(2).toInt()
        var x : String = str.substring(1, 2)

        if (N1.equals(N2)) {
            println(String.format("%d",N1 * N2))
        } else {
            if (x.toUpperCase()==x) {
                println(String.format("%d",N2 - N1))
            } else {
                println(String.format("%d",N1 + N2))
            }
        }
    }
}
```


## Desafio 9

```
fun main() {
   val x = (readLine() ?: return).toInt()
    val y = (readLine() ?: return).toInt()
    var total = 0

    if (x < y) {
        for (i in x..y) {
            if (i % 13 != 0) {
                total += i
            }
        }
    } else {
        for (i in x downTo  y) {
            if (i % 13 != 0) {
                total += i
            }
        }
    }
    println(total)
}
```
