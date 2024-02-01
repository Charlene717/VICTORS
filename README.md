## Installation
```{r, eval = FALSE}
if(!require("devtools")) install.packages("devtools"); library(devtools)
if(!require("VICTORS")) install_github("Charlene717/VICTORS"); library(VICTORS)
```

## Operation method
load packages
```{r, eval = FALSE}
if(!require("tidyverse")) install.packages("tidyverse"); library(tidyverse)
if(!require("Seurat")) install.packages("Seurat"); library(Seurat)
```
load demo file
```{r, eval = FALSE}
load("Path/to/Demo.RData")
```

Set query, reference, column of Actual Cell Type, column of Annotation
```{r, eval = FALSE}
    VICTORS.lt <- VICTORS(seuratObject_Sample, seuratObject_Ref,
                          ActualCellTypeColumn = "Actual_Cell_Type",
                          AnnotCellTypeColumn = "Annotation")
```

Renew query and reference
(The diagnostic results of Query are stored in the updated seurat's meta.data.)
```{r, eval = FALSE}
    seuratObject_Sample <- VICTORS.lt$Sample
    seuratObject_Ref <- VICTORS.lt$Reference
```


