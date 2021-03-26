#Johnny Rondon (2019-8291)


#Instalamos LOS paquetes necesario para leer y filtrar el archivo
install.packages("readr")
install.packages("dplyr")
install.packages("ggplot2")

#llamamos los paquetes
library(readr)
library(dplyr)
library(ggplot2)

#Le pasamos los datos a la variable datos
Datos <- read_csv2("EstadisticasCultivo2019.csv")
View(Datos)

#Dividimos los datos de los cultivos segun el trimestre
#Cada uno actuara como una tabla distinta
ListaCultivos <- filter(Datos, TRIMESTRE=="enero-marzo")
View(ListaCultivos)

ListaCultivos2 <- filter(Datos, TRIMESTRE=="abril-junio")
View(ListaCultivos2)

ListaCultivos3 <- filter(Datos, TRIMESTRE=="octubre-diciembre")
View(ListaCultivos3)


#-----Eliminamos las filas que no esten completas-----
#-----Tambien renombramos las columnas-----
ListaC = ListaCultivos[complete.cases(ListaCultivos),]
names(ListaC)=c("FAMILIA", "CULTIVOS", "SUPERFICIE_SEMBRADA", "SUPERFICIE_COSECHADAS", "VOLUMEN_OBTENIDO", "UNIDAD_DE_MEDIDA", "VALOR_PRODUCCION", "TRIMESTRE", "ANUALIDAD")

ListaC2 = ListaCultivos2[complete.cases(ListaCultivos2),]
names(ListaC2)=c("FAMILIA", "CULTIVOS", "SUPERFICIE_SEMBRADA", "SUPERFICIE_COSECHADAS", "VOLUMEN_OBTENIDO", "UNIDAD_DE_MEDIDA", "VALOR_PRODUCCION", "TRIMESTRE", "ANUALIDAD")

ListaC3 = ListaCultivos3[complete.cases(ListaCultivos3),]
names(ListaC3)=c("FAMILIA", "CULTIVOS", "SUPERFICIE_SEMBRADA", "SUPERFICIE_COSECHADAS", "VOLUMEN_OBTENIDO", "UNIDAD_DE_MEDIDA", "VALOR_PRODUCCION", "TRIMESTRE", "ANUALIDAD")



#---------------Analizemos la ListaC---------------
attach(ListaC)  #cambiemos predeterminado a nuevo dataset

#La media de superficie de cultivos cosechados es 5122.417
mean(SUPERFICIE_COSECHADAS) 

hist(SUPERFICIE_COSECHADAS) #El histograma me lo deja ver graficaente

# varia la superficie sembrada de la cosechada de los cultivos? 
plot(SUPERFICIE_SEMBRADA ~ SUPERFICIE_COSECHADAS, main = "Superficie sembrada de cosechada LC",
        xlab = "Cosechada",
        ylab = "Sembrada",
        col="blue"
)

boxplot(VOLUMEN_OBTENIDO ~ FAMILIA, main = "Volumen obtenido por familia de cultivo LC",
        xlab = "Familia",
        ylab = "Volumen",
        col="blue"
)



#---------------Analizemos la ListaC2---------------
attach(ListaC2)  #cambiemos predeterminado a nuevo dataset

#La media de superficie de cultivos cosechados es 9852.36
mean(SUPERFICIE_COSECHADAS) 

hist(SUPERFICIE_COSECHADAS) #El histograma me lo deja ver graficaente

# varia la superficie sembrada de la cosechada de los cultivos?
plot(SUPERFICIE_SEMBRADA ~ SUPERFICIE_COSECHADAS, main = "Superficie sembrada de cosechada LC2",
        xlab = "Cosechada",
        ylab = "Sembrada",
        col="blue"
)

boxplot(VOLUMEN_OBTENIDO ~ FAMILIA, main = "Volumen obtenido por familia de cultivo LC2",
        xlab = "Familia",
        ylab = "Volumen",
        col="blue"
)



#---------------Analizemos la ListaC3---------------
attach(ListaC3)  #cambiemos predeterminado a nuevo dataset

#La media de superficie de cultivos cosechados es 4854.26
mean(SUPERFICIE_COSECHADAS) 

hist(SUPERFICIE_COSECHADAS) #El histograma me lo deja ver graficaente

# varia la superficie sembrada de la cosechada de los cultivos?
plot(SUPERFICIE_SEMBRADA ~ SUPERFICIE_COSECHADAS, main = "Superficie sembrada de cosechada LC3",
        xlab = "Cosechada",
        ylab = "Sembrada",
        col="blue"
)

boxplot(VOLUMEN_OBTENIDO ~ FAMILIA, main = "Volumen obtenido por familia de cultivo LC3",
        xlab = "Familia",
        ylab = "Volumen",
        col="blue"
)


