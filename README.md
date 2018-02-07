# series-de-tiempo
## 1 simulacion de series de tiempo
### vamos a simular el indicador
### para la simulacion en principio necesitamos algina informacion
## valor maximo, minimo, el numero de datos

## en este ejemplo vamos a proponer la poblacion en mexico
## que el valor minimo seran 100, max 120, 15 datos que inicie en 2000
prob<-sample(100:120,15, replace=F)
prob
## la convertimos en serie de tiempo 
pobts<- ts(prob,frequency = 1,start = (2000)) ## ts= lo conviertes en serie de tiempo frequency=las veces que se repite en el año
## start= año en que empieza
end(pobts)
start(pobts)
plot(pobts)## darle formato
plot(aggregate(pobts))

## bajar del inegi la ocupacion de personas
### importar csv
infor4<-read.csv("C://Users//USUARIO//Documents//inrgi.csv")
infor4
serie<-ts(infor4,frequency = 4, start=(2005))
end(serie)
plot(serie)## darle formato
plot(infts, ylim=c(0,100))
