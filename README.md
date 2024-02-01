## Installation
```{r, eval = FALSE}
if(!require("devtools")) install.packages("devtools"); library(devtools)
if(!require("VICTORS")) install_github("Charlene717/VICTORS"); library(VICTORS)
```

## Operation method
```{r, eval = FALSE}
if(!require("tidyverse")) install.packages("tidyverse"); library(tidyverse)
if(!require("Seurat")) install.packages("Seurat"); library(Seurat)
```
```{r, eval = FALSE}
load("Path/to/Demo.RData")
```

```{r, eval = FALSE}
    VICTORS.lt <- VICTORS(seuratObject_Sample, seuratObject_Ref,
                          ActualCellTypeColumn = "Actual_Cell_Type",
                          AnnotCellTypeColumn = "Annotation")
    seuratObject_Sample <- VICTORS.lt$Sample
    seuratObject_Ref <- VICTORS.lt$Reference
```


