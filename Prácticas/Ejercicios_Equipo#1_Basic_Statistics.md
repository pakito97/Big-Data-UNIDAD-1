### Correlation

import org.apache.spark.ml.linalg.{Matrix, Vectors}
import org.apache.spark.ml.stat.Correlation
import org.apache.spark.sql.Row


import org.apache.spark.sql.SparkSession
//importamos la session de spark
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
// se crea un dataframe al cual se le asigna el valor de una tupla llamada tupla1
// el dataframe contiene una columna llamada features
        val df = data.map(Tuple1.apply).toDF("features")

//a un valor de tipo Fila llamado coeficiente1 de una matrix se le asigna el valor de la correlacion de pearson aplicada en el dataframe
//aplicado a la columna features
        val Row(coeff1: Matrix) = Correlation.corr(df, "features").head 
//a un valor de tipo Fila llamado coeficiente2 de una matrix se le asigna el valor de la correlacion de pearson aplicada en el dataframe
//aplicado a la columna features
        val Row(coeff2: Matrix) = Correlation.corr(df, "features", "spearman").head
        println(s"Spearman correlation matrix:\n $coeff2")// se imprime
        
        spark.stop()
    }
}
