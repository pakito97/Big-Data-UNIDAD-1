### Correlation

```scala
import org.apache.spark.ml.linalg.{Matrix, Vectors}
import org.apache.spark.ml.stat.Correlation
import org.apache.spark.sql.Row
import org.apache.spark.sql.SparkSession
```

>importamos la session de spark

```scala
object CorrelationExample{

    def main(args: Array[String]): Unit = {
        val spark = SparkSession
        .builder
        .appName("CorrelationExample")
        .getOrCreate()
        import spark.implicits

        val data = Seq(
            Vectors.sparse(4, Seq((0, 1.0), (3, -2.0))),
            Vectors.dense(4.0, 5.0, 0.0, 3.0),
            Vectors.dense(6.0, 7.0, 0.0, 8.0),
            Vectors.sparse(4, Seq((0, 9.0), (3, 1.0)))
        )
```
>se crea un dataframe al cual se le asigna el valor de una tupla llamada tupla1
>el dataframe contiene una columna llamada features
        
        ```scala
        val df = data.map(Tuple1.apply).toDF("features")
        ```

>a un valor de tipo Fila llamado coeficiente1 de una matrix se le asigna el valor de la correlacion de pearson aplicada en el dataframe
>aplicado a la columna features

        ```scala
        val Row(coeff1: Matrix) = Correlation.corr(df, "features").head 
        ```
      
>a un valor de tipo Fila llamado coeficiente2 de una matrix se le asigna el valor de la correlacion de pearson aplicada en el dataframe
>aplicado a la columna features

       ```scala
        val Row(coeff2: Matrix) = Correlation.corr(df, "features", "spearman").head
        println(s"Spearman correlation matrix:\n $coeff2")// se imprime
        
       
        spark.stop()
    }
    }```
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
### ChiSquareTest

 ```scala
import org.apache.spark.ml.linalg.{Vector, Vectors}
import org.apache.spark.ml.stat.ChiSquareTest

import org.apache.spark.sql.SparkSession
 ```
>importamos la session de spark
```scala
object ChiSquareTestExample{

    def main(args: Array[String]): Unit = {
        val spark = SparkSession
        .builder
        .appName("ChiSquareTestExample")
        .getOrCreate()
        import spark.implicits

        val data = Seq(
            (0.0, Vectors.dense(0.5,10.0)),
            (0.0, Vectors.dense(1.5,20.0)),
            (1.0, Vectors.dense(1.5,30.0)),
            (0.0, Vectors.dense(3.5,30.0)),
            (0.0, Vectors.dense(3.5,40.0)),
            (1.0, Vectors.dense(3.5,40.0))
        )
```
>se crea un dataframe al cual se le asigna el valor date en las columnas label y features
 ```scala
        val df = data.toDF("label","features")
        //se crea un valor chi al que se le aplica chisquare mediantes las librerias al dataframe
        val chi = ChiSquareTest.test(df, "features", "label").head
        println(s"pValues = ${chi.getAs[Vector](0)}")
        println(s"degreesOfFreedom ${chi.getSeq[int](1).mkString("[", ",", "]")}")
        println(s"statistics ${chi.getAs[Vector](2)}")// se imprime
        
        spark.stop()
    }
} ```
