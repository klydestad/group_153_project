### Run this cell before continuing.
library(tidyverse)
library(repr)
library(tidymodels)
options(repr.matrix.max.rows = 6)
#cleve_data <- read_csv("data/processed.cleveland.csv")
#hungary_data <- read_csv("data/processed.hungarian.csv")
#switz_data <- read_csv("data/processed.switzerland.csv")
van_data_csv <- read_csv("data/processed.van.csv", col_names =
               c("age", "sex", "chest_pain", "trestbps", "chol",
               "fbs",  "restecg", "thalach", "exang", "oldpeak", 
               "slope", "ca", "thal", "num")) %>%
                filter(!is.na(restecg)) %>%
                filter(!is.na(chol)) %>%
                filter(!is.na(trestbps))

van_data <- van_data_csv %>%
             select(age, restecg, trestbps, chol)

van_data
options(repr.plot.width = 20, repr.plot.height = 20) 

van_plot_chol <- ggplot(van_data, aes(x = age, y = chol)) + 
            geom_point() + 
            labs(x = "Age (years)", y = "Serum Cholesterol (mg/dL)", title = "Resting Blood Pressure vs. Cholesterol") + 
            theme( text = element_text(size = 20)) 
            
            
van_plot_chol       


options(repr.plot.width = 18, repr.plot.height = 18) 

van_plot_bps <- ggplot(van_data, aes(x = age, y = trestbps)) + 
            geom_point() + 
            labs(x = "Age (years)", y = "Resting Blood Pressure (mm Hg)", title = "Resting Blood Pressure vs. Age") + 
            theme( text = element_text(size = 20)) 
            
            
van_plot_bps 
