# Introducere în analiza statistică {#cap3}

## Concepte de bază privind analiza statistică

text

## Mărimile relative

text

## Sistematizarea datelor

text

## Indicatorii de nivel

### Aplicații

#### 1. Media unei serii simple

Se cunosc date privind veniturile salariale lunare (în lei/lună) ale celor 80 de angajați din firma M.  Caracteristicile serie sunt prezentate în tabelul următor și ne propunem realizarea acestei analize descriptive prin cele 4 platforme software.  

::: {.content-visible when-format="html"}
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-c3ow"></th>
    <th class="tg-c3ow">grupe de venit<br>(lei)</th>
    <th class="tg-c3ow">$n_i$</th>
    <th class="tg-c3ow">$h_i$</th>
    <th class="tg-c3ow">$x_i$</th>
    <th class="tg-c3ow">$x_i n_i$</th>
    <th class="tg-c3ow">$N_i$\^</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow">0 – 1000</td>
    <td class="tg-c3ow">6</td>
    <td class="tg-c3ow">300</td>
    <td class="tg-c3ow">850</td>
    <td class="tg-c3ow">5100</td>
    <td class="tg-c3ow">6</td>
  </tr>
  <tr>
    <td class="tg-0pky">interval <br>quartila <br>inferioară</td>
    <td class="tg-c3ow">1001 – 1300</td>
    <td class="tg-c3ow">24</td>
    <td class="tg-c3ow">300</td>
    <td class="tg-c3ow">1150</td>
    <td class="tg-c3ow">27600</td>
    <td class="tg-c3ow">30</td>
  </tr>
  <tr>
    <td class="tg-0pky">interval <br>median</td>
    <td class="tg-c3ow">1301 – 1600</td>
    <td class="tg-c3ow">30</td>
    <td class="tg-c3ow">300</td>
    <td class="tg-c3ow">1450</td>
    <td class="tg-c3ow">43500</td>
    <td class="tg-c3ow">60</td>
  </tr>
  <tr>
    <td class="tg-0pky">interval <br>quartila <br>superioară</td>
    <td class="tg-c3ow">1601 – 1900</td>
    <td class="tg-c3ow">12</td>
    <td class="tg-c3ow">300</td>
    <td class="tg-c3ow">1750</td>
    <td class="tg-c3ow">21000</td>
    <td class="tg-c3ow">72</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow">1901 – 2200</td>
    <td class="tg-c3ow">5</td>
    <td class="tg-c3ow">300</td>
    <td class="tg-c3ow">2050</td>
    <td class="tg-c3ow">10250</td>
    <td class="tg-c3ow">77</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow">2201 – $\inf$</td>
    <td class="tg-c3ow">3</td>
    <td class="tg-c3ow">300</td>
    <td class="tg-c3ow">2350</td>
    <td class="tg-c3ow">7050</td>
    <td class="tg-c3ow">80</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow">total</td>
    <td class="tg-c3ow">80</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">114500</td>
    <td class="tg-c3ow"></td>
  </tr>
</tbody></table>
:::

::: {.content-visible when-format="pdf"}
\begin{table}[]
\begin{tabular}{lcccccc}
                             & grupe de venit (lei) & $n_i$ & $h_i$ & $x_i$ & $x_i n_i$ & $N_i$\^ \\                              & 0 – 1000             & 6     & 300   & 850   & 5100      & 6       \\
interval                     & 1001 - 1300          & 24    & 300   & 1150  & 27600     & 30      \\
interval median              & 1301 - 1600          & 30    & 300   & 1450  & 43500     & 60      \\
interval quartila superioară & 1601 - 1900          & 12    & 300   & 1750  & 21000     & 72      \\
                             & 1901 - 2200          & 5     & 300   & 2050  & 10250     & 77      \\
                             & 2201 - $\inf$        & 3     & 300   & 2350  & 7050      & 80      \\
                             & total                & 80    & -     & -     & 114500    &         \\ \end{tabular}
\end{table}
:::

Să se determine venitul salarial mediu lunar al angajaților firmei.  

##### Rezolvare prin R






::: {.cell}

```{.r .cell-code}
# incarcarea datelor "venit.csv"
venit <- read.csv("date/venit.csv", head = T)
# o vizualizare succinta a datelor
head(venit)
```

::: {.cell-output .cell-output-stdout}

```
  venit
1  1660
2  1410
3  1550
4  1820
5  1320
6  1340
```


:::

```{.r .cell-code}
# explorarea prelimiară a datelor
summary(venit)
```

::: {.cell-output .cell-output-stdout}

```
     venit     
 Min.   : 750  
 1st Qu.:1260  
 Median :1395  
 Mean   :1451  
 3rd Qu.:1605  
 Max.   :2360  
```


:::

```{.r .cell-code}
# intervalul datelor
range(venit$venit)
```

::: {.cell-output .cell-output-stdout}

```
[1]  750 2360
```


:::

```{.r .cell-code}
# calculul mediei seriei simple
mean(venit$venit)
```

::: {.cell-output .cell-output-stdout}

```
[1] 1450.875
```


:::
:::






Venitul salarial mediu lunar al celor 80 angajați ai firmei este de 1450.875 lei/lună.  


##### Rezolvare prin Python






::: {.cell}

```{.python .cell-code}
# importarea librariilor necesare
import pandas as pd

# incarcarea datelor "venit.csv"
venit = pd.read_csv("date/venit.csv")

# o vizualizare succinta a datelor
print(venit.head())
```

::: {.cell-output .cell-output-stdout}

```
   venit
0   1660
1   1410
2   1550
3   1820
4   1320
```


:::

```{.python .cell-code}
# explorarea preliminara a datelor
print(venit.describe())
```

::: {.cell-output .cell-output-stdout}

```
             venit
count    80.000000
mean   1450.875000
std     338.683952
min     750.000000
25%    1260.000000
50%    1395.000000
75%    1605.000000
max    2360.000000
```


:::

```{.python .cell-code}
# intervalul datelor
print(venit['venit'].min(), venit['venit'].max())
```

::: {.cell-output .cell-output-stdout}

```
750 2360
```


:::

```{.python .cell-code}
# calculul mediei seriei simple
print(venit['venit'].mean())
```

::: {.cell-output .cell-output-stdout}

```
1450.875
```


:::
:::






##### Rezolvare prin Excel

![](date/medie_simpla.PNG)  
[venit.xlsx](date/venit.xlsx)

##### Rezolvare prin Power BI

![](date/medie_simpla_Pbi.png)


#### 2. Gruparea datelor - construirea seriilor de distribuție

Exemplu: A fost efectuată o cercetare privind mărimea (măsurată pe baza numărului de salariați) a 80 de firme industriale din orașul M. Datele referitoare la numărul de salariați înregistrat în cursul observării sunt următoarele:

::: {.content-visible when-format="html"}
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-0pky">166</th>
    <th class="tg-0pky">162</th>
    <th class="tg-0pky">121</th>
    <th class="tg-0pky">126</th>
    <th class="tg-0pky">128</th>
    <th class="tg-0pky">85</th>
    <th class="tg-0pky">136</th>
    <th class="tg-0pky">158</th>
    <th class="tg-0pky">135</th>
    <th class="tg-0pky">127</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky">141</td>
    <td class="tg-0pky">142</td>
    <td class="tg-0pky">92</td>
    <td class="tg-0pky">148</td>
    <td class="tg-0pky">177</td>
    <td class="tg-0pky">80</td>
    <td class="tg-0pky">156</td>
    <td class="tg-0pky">188</td>
    <td class="tg-0pky">205</td>
    <td class="tg-0pky">144</td>
  </tr>
  <tr>
    <td class="tg-0pky">155</td>
    <td class="tg-0pky">230</td>
    <td class="tg-0pky">100</td>
    <td class="tg-0pky">129</td>
    <td class="tg-0pky">160</td>
    <td class="tg-0pky">159</td>
    <td class="tg-0pky">105</td>
    <td class="tg-0pky">150</td>
    <td class="tg-0pky">110</td>
    <td class="tg-0pky">98</td>
  </tr>
  <tr>
    <td class="tg-0pky">182</td>
    <td class="tg-0pky">102</td>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">198</td>
    <td class="tg-0pky">115</td>
    <td class="tg-0pky">122</td>
    <td class="tg-0pky">124</td>
    <td class="tg-0pky">163</td>
    <td class="tg-0pky">130</td>
    <td class="tg-0pky">133</td>
  </tr>
  <tr>
    <td class="tg-0pky">132</td>
    <td class="tg-0pky">150</td>
    <td class="tg-0pky">75</td>
    <td class="tg-0pky">206</td>
    <td class="tg-0pky">149</td>
    <td class="tg-0pky">170</td>
    <td class="tg-0pky">112</td>
    <td class="tg-0pky">142</td>
    <td class="tg-0pky">119</td>
    <td class="tg-0pky">151</td>
  </tr>
  <tr>
    <td class="tg-0pky">134</td>
    <td class="tg-0pky">224</td>
    <td class="tg-0pky">135</td>
    <td class="tg-0pky">236</td>
    <td class="tg-0pky">126</td>
    <td class="tg-0pky">175</td>
    <td class="tg-0pky">215</td>
    <td class="tg-0pky">130</td>
    <td class="tg-0pky">121</td>
    <td class="tg-0pky">128</td>
  </tr>
  <tr>
    <td class="tg-0pky">190</td>
    <td class="tg-0pky">156</td>
    <td class="tg-0pky">108</td>
    <td class="tg-0pky">143</td>
    <td class="tg-0pky">218</td>
    <td class="tg-0pky">172</td>
    <td class="tg-0pky">180</td>
    <td class="tg-0pky">120</td>
    <td class="tg-0pky">169</td>
    <td class="tg-0pky">129</td>
  </tr>
  <tr>
    <td class="tg-0pky">123</td>
    <td class="tg-0pky">156</td>
    <td class="tg-0pky">142</td>
    <td class="tg-0pky">127</td>
    <td class="tg-0pky">133</td>
    <td class="tg-0pky">146</td>
    <td class="tg-0pky">139</td>
    <td class="tg-0pky">140</td>
    <td class="tg-0pky">138</td>
    <td class="tg-0pky">138</td>
  </tr>
</tbody></table>
:::

::: {.content-visible when-format="pdf"}
\begin{table}[]
\begin{tabular}{|l|l|l|l|l|l|l|l|l|l|}
\hline
166 & 162 & 121 & 126 & 128 & 85  & 136 & 158 & 135 & 127 \\ \hline
141 & 142 & 92  & 148 & 177 & 80  & 156 & 188 & 205 & 144 \\ \hline
155 & 230 & 100 & 129 & 160 & 159 & 105 & 150 & 110 & 98  \\ \hline
182 & 102 & 128 & 198 & 115 & 122 & 124 & 163 & 130 & 133 \\ \hline
132 & 150 & 75  & 206 & 149 & 170 & 112 & 142 & 119 & 151 \\ \hline
134 & 224 & 135 & 236 & 126 & 175 & 215 & 130 & 121 & 128 \\ \hline
190 & 156 & 108 & 143 & 218 & 172 & 180 & 120 & 169 & 129 \\ \hline
123 & 156 & 142 & 127 & 133 & 146 & 139 & 140 & 138 & 138 \\ \hline
\end{tabular}
\end{table}
:::

##### Rezolvare prin R






::: {.cell}

```{.r .cell-code}
# incarcarea datele
grupare <- read.csv("date/grupare.csv", head = F)
head(grupare)
```

::: {.cell-output .cell-output-stdout}

```
   V1
1 166
2 162
3 121
4 126
5 128
6  85
```


:::

```{.r .cell-code}
# numarul de observatii
nobs <- length(grupare$V1)
nobs
```

::: {.cell-output .cell-output-stdout}

```
[1] 80
```


:::

```{.r .cell-code}
# numărul de grupe
g <- ceiling((2*nobs)^(1/3))
g
```

::: {.cell-output .cell-output-stdout}

```
[1] 6
```


:::

```{.r .cell-code}
# valoarea maximă
xmax <- max(grupare$V1)
xmax
```

::: {.cell-output .cell-output-stdout}

```
[1] 236
```


:::

```{.r .cell-code}
# valoarea minimă
xmin <- min(grupare$V1)
xmin
```

::: {.cell-output .cell-output-stdout}

```
[1] 75
```


:::

```{.r .cell-code}
# determinarea înălțimii intervalelor
h <- (xmax - xmin) / g
h
```

::: {.cell-output .cell-output-stdout}

```
[1] 26.83333
```


:::

```{.r .cell-code}
# rotunjirea la o valoare superioară a intervalului
h <- ceiling(h/10) * 10
h
```

::: {.cell-output .cell-output-stdout}

```
[1] 30
```


:::

```{.r .cell-code}
# limitele intervalelor de grupare
x1_inf <- xmin - (g*h-(xmax-xmin))/2
x1_inf 
```

::: {.cell-output .cell-output-stdout}

```
[1] 65.5
```


:::

```{.r .cell-code}
# rotunjirea la o valoare superioară a limitei inferioare
x1_inf <- ceiling(x1_inf/10) * 10
x1_inf
```

::: {.cell-output .cell-output-stdout}

```
[1] 70
```


:::

```{.r .cell-code}
# dacă limita inferioară nu cuprinde valoarea minimă se reajustează limita inferioară
if (x1_inf > xmin) {x1_inf <- (floor(x1_inf/10) - 1) * 10}

# determinarea intervalelor de frecvente
limite_intervale <- seq(from = x1_inf, to = 250, by = h)
grupare$interval <- cut(grupare$V1, breaks = limite_intervale)

library(dplyr)
```

::: {.cell-output .cell-output-stderr}

```

Attaching package: 'dplyr'
```


:::

::: {.cell-output .cell-output-stderr}

```
The following objects are masked from 'package:stats':

    filter, lag
```


:::

::: {.cell-output .cell-output-stderr}

```
The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union
```


:::

```{.r .cell-code}
grupare %>% 
  group_by(interval) %>%
  summarise(frecvente = n())
```

::: {.cell-output .cell-output-stdout}

```
# A tibble: 6 x 2
  interval  frecvente
  <fct>         <int>
1 (70,100]          6
2 (100,130]        24
3 (130,160]        30
4 (160,190]        12
5 (190,220]         5
6 (220,250]         3
```


:::
:::






##### Rezolvare prin Python






::: {.cell}

```{.python .cell-code}
import pandas as pd
import numpy as np
import math

# încărcarea datelor
grupare = pd.read_csv("date/grupare.csv", header=None, names=["V1"])
print(grupare.head())
```

::: {.cell-output .cell-output-stdout}

```
    V1
0  166
1  162
2  121
3  126
4  128
```


:::

```{.python .cell-code}
# numărul de observații
nobs = len(grupare["V1"])
print(nobs)
```

::: {.cell-output .cell-output-stdout}

```
80
```


:::

```{.python .cell-code}
# numărul de grupe
g = math.ceil((2 * nobs) ** (1/3))
print(g)
```

::: {.cell-output .cell-output-stdout}

```
6
```


:::

```{.python .cell-code}
# valoarea maximă
xmax = grupare["V1"].max()
print(xmax)
```

::: {.cell-output .cell-output-stdout}

```
236
```


:::

```{.python .cell-code}
# valoarea minimă
xmin = grupare["V1"].min()
print(xmin)
```

::: {.cell-output .cell-output-stdout}

```
75
```


:::

```{.python .cell-code}
# determinarea înălțimii intervalelor
h = (xmax - xmin) / g
h = math.ceil(h / 10) * 10  # rotunjire la cel mai apropiat multiplu de 10
print(h)
```

::: {.cell-output .cell-output-stdout}

```
30
```


:::

```{.python .cell-code}
# limitele intervalelor de grupare
x1_inf = xmin - (g * h - (xmax - xmin)) / 2
x1_inf = math.ceil(x1_inf / 10) * 10  # rotunjire la cel mai apropiat multiplu de 10

# ajustarea limitei inferioare dacă este necesar
if x1_inf > xmin:
    x1_inf = (math.floor(x1_inf / 10) - 1) * 10
print(x1_inf)
```

::: {.cell-output .cell-output-stdout}

```
70
```


:::

```{.python .cell-code}
# determinarea intervalelor de frecvențe
limite_intervale = np.arange(x1_inf, 250 + h, h)
grupare['interval'] = pd.cut(grupare['V1'], bins=limite_intervale)

# calculul frecvențelor pe intervale
frecvente = grupare.groupby('interval').size().reset_index(name='frecvente')
print(frecvente)
```

::: {.cell-output .cell-output-stdout}

```
     interval  frecvente
0   (70, 100]          6
1  (100, 130]         24
2  (130, 160]         30
3  (160, 190]         12
4  (190, 220]          5
5  (220, 250]          3
```


:::
:::






##### Rezolvare prin Excel

![](date/grupare.PNG)
[grupare.xlsx](date/grupare.xlsx)

##### Rezolvare prin Power BI

![](date/medie_simpla_Pbi.png)



## Indicatorii variației

• abateri, dispersie, abatere standard, repartiție, asimetrie, concentrare

## Vizualizarea datelor

text

