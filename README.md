# Proyecto-01
# Andy Johel Valverde Ledezma
# C09291

## Cargamos los paquetes:
library(ggplot2)
library(dplyr)
library(hrbrthemes)
library(ggplot)

## Asigné un nombre al documento con el que voy a trabajar
data_clima <- read.csv("liberia_datos_climaticos.csv",
                       sep = ",",
                       na.strings = "",
                       dec = ",")
                       
## Revisé que no tuviera celdas vacías(NA)
View(data_clima)

## Realicé los histogramas

### Histograma de temperatura
ggplot(data_clima, aes(x = Temperatura..Celsius.)) +
  geom_histogram(binwidth = 2,
                 color = "red",
                 fill = "white") +
  ggtitle("Temperatura en Liberia") +
  xlab("Temperatura(Celsius)") +
  ylab("Días")+
  theme_ipsum()
  
### Histograma de Humedad Relativa
ggplot(data_clima, aes(x = HumedadRelativa....)) +
  geom_histogram(binwidth = 2,
                 color = "red",
                 fill = "white") +
  ggtitle("Humedad Relativa en Liberia") +
  xlab("Humedad Relativa") +
  ylab("Días")+
  theme_ipsum_es()
  
### Histograma de Velocidad de viento
ggplot(data_clima, aes(x = VelocidadViento..m.s.)) +
  geom_histogram(binwidth = 2,
                 color = "yellow",
                 fill = "dark green") +
  ggtitle("Velocidad de viento en Liberia") +
  xlab("Velocidad de viento") +
  ylab("Días")+
  theme_ft_rc()
  
### Histograma de Lluvias
ggplot(data_clima, aes(x = Lluvia..mm.)) +
  geom_histogram(binwidth = 2,
          color = "pink",
          fill = "purple") +
  ggtitle("Lluvias en Liberia") +
  xlab("Lluvias") +
  ylab("Frecuencia")+       
  theme_ipsum_es()
  
### Histograma de Irradiacion
ggplot(data_clima, aes(x = Irradiacion..W.m2.)) +
  geom_histogram(binwidth = 2,
                 color = "orange",
                 fill = "brown") +
  ggtitle("Irradiacion en Liberia") +
  xlab("Iradiacion") +
  ylab("Frecuencia")+       
  scale_color_ipsum()

### Histograma de EvapoTranspiracion
ggplot(data_clima, aes(x = EvapoTranspiracion..mm.)) +
  geom_histogram(binwidth = 2,
                 color = "light blue",
                 fill = "blue") +
  ggtitle("EvapoTranspiracion en Liberia") +
  xlab("EvapoTranspiración") +
  ylab("Frecuencia")+       
  theme_ft_rc()