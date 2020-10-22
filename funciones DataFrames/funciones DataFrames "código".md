//we import the apache spark session

import org.apache.spark.sql.SparkSession

//we create the variable spark
val spark = SparkSession.builder().getOrCreate()

//We create the Data Frame and indicate the location of the data that we will use
val df = spark.read.option("header", "true").option("inferSchema","true")csv("C:/Users/DELL/Desktop/Unidad#1/funciones DataFrames-tiendita/tiendita_productos.csv")

//print the Schema
df.printSchema() 

//we import the spark variable implicitly
import spark.implicits._

//#1 Average in a data set (price)
df.select(avg("price")).show()

//#2 perform the sum over a data set
df.select(sum("price")).show()

//#3 identify the minimum value on a data set
df.select(min("price"),max ("price")).show()

//#4 Identify the maximum value in a data set
df.select(max("price")).show()

//#5 Shows an example that calculates the mean and maximum value of the subset of data grouped by last name
df.groupBy(df.col("amount")).agg(avg("price"), max("price")).show()

//#6 Shows an example that calculates the correlation over a data set
df.stat.corr("amount", "price")

//#7 Example that calculates covariance in a data set
df.stat.cov("amount", "price")

//#8 Show all Data Frame
df.show()

//#9 Show the names of the DataFrame columns
df.columns

//#10 Existing columns and information about them
df.printSchema()

//#11 select two specific columns
 df.select("amount","price").show()

 //#12 condition when price is less than 25 return boolean
val preciosmenor = df.select($"price" < 25)

// # 13 add a new column
val df2 = df.withColumn ("price*2", df ("price") * 2)
df2.show

// # 14 how many have the same price
df.groupBy ("price"). count (). show ()

// # 15 Show what type of data the Dataframe has
df2.printSchema ()
