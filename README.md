# RFR
Relatório Final das Aulas de R em RMarkdown


> installed.packages(latex)
Error in installed.packages(latex) : object 'latex' not found
> installed.packages(LaTeX)
Error in installed.packages(LaTeX) : object 'LaTeX' not found
> install.packages(LaTeX)
Error in install.packages : object 'LaTeX' not found
> install.packages("latex2exp")
Installing package into ‘/home/rstudio-user/R/x86_64-pc-linux-gnu-library/4.0’
(as ‘lib’ is unspecified)
trying URL 'http://package-proxy/src/contrib/latex2exp_0.4.0.tar.gz'
Content type 'application/x-tar' length 319128 bytes (311 KB)
==================================================
downloaded 311 KB

* installing *binary* package ‘latex2exp’ ...
* DONE (latex2exp)

The downloaded source packages are in
	‘/tmp/RtmptvcsIq/downloaded_packages’
> 
> 
> 
> a <- 9
> b <- 4
> c <- -6
> delta <-  (b ** 2) − (4 ∗ a ∗ c)
Error: unexpected input in "delta <-  (b ** 2) −"
> a <- 9
> b <- 4
> c <- -6
> delta <-(b ** 2) − (4 ∗ a ∗ c)
Error: unexpected input in "delta <-(b ** 2) −"
> 
> a <- 9
> b <- 4
> c <- -6
> delta <-(b ** 2) - (4 * a * c)
> print(delta)
[1] 232
> 
> if (a == 0 & b == 0 & c == 0){
+     raizes = NA
+ } else if (a == 0 & b == 0){
+     raizes = NULL
+ } else if (a == 0){
+     raizes = - c / b
+ } else {
+ while (delta > 0){
+       raiz1 <- ((- b +  sqrt(delta)) / (2 * a))
+       raiz2 <- ((- b - sqrt(delta)) / (2 * a))
+ } else if (delta == 0) {
Error: unexpected 'else' in:
"      raiz2 <- ((- b - sqrt(delta)) / (2 * a))
} else"
> 
> a <- 9
> b <- 4
> c <- -6
> delta <-(b ** 2) - (4 * a * c)
> print(delta)
[1] 232
> 
> if (a == 0 & b == 0 & c == 0){
+     raizes = NA
+ } else if (a == 0 & b == 0){
+     raizes = NULL
+ } else if (a == 0){
+     raizes = - c / b
+ 
+ while (delta > 0){
+       raiz1 <- ((- b +  sqrt(delta)) / (2 * a))
+       raiz2 <- ((- b - sqrt(delta)) / (2 * a))
+ } else if (delta == 0) {
Error: unexpected 'else' in:
"      raiz2 <- ((- b - sqrt(delta)) / (2 * a))
} else"
> paulo <- 150
> joao <- 110
> ano <- 0
> 
> repeat{
+   paulo = paulo + 2
+   joao = joao + 3
+   ano = ano + 1
+ if(joao > paulo){break}
+   
+ }
> cat("joao passou paulo depois de ", ano, "anos.")
joao passou paulo depois de  41 anos.> cat("joao: ", joao, "cm")
joao:  233 cm> cat("paulo: ", paulo, "cm")
paulo:  232 cm> 
> x = 0
> repeat{
+   d = sample(1:6, size = 2)
+   print(d)
+   print(sum(d))
+   x = x + 1
+   if(sum(d)==7|sum(d)==11){
+     (break)
+   }}
[1] 3 4
[1] 7
> format(x)
[1] "1"
> 
> 
> b <- 20
> a <- 10
> area <- (b * a) / 2
> triangulo <- function(b, a) {
+   return(area)
+ }
> cat("a area do triangulo é: ", area, "\n")
a area do triangulo é:  100 
> 
> 
> 
> 
> t <-  (1:10)
> x = trunc(sqrt(t))
> y = trunc(2 * pi *t)
> z = rbind(x, y)
> f = function(x, y){
+   return(z)
+ }
> show(z)
  [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8] [,9] [,10]
x    1    1    1    2    2    2    2    2    3     3
y    6   12   18   25   31   37   43   50   56    62
> 
> 
> 
> x = c(1, 16, 144, -4)
> z = table(as.vector(x))
> y = ifelse(x<=0, (-x^3), ifelse(x>0&x<=0, x^2, ifelse(x>1, sqrt(x), TRUE)))
> teste = function (x){
+   return(y)
+ }
> print(y)
[1]  1  4 12 64
> 
> 
> 
> vetor <- function(x){
+   x <- c(1:20)
+   print(x)
+   y <- median(x)
+ }
> show(y)
[1]  1  4 12 64
> 
> 
> m <- matrix(1:20, nrow = 4, ncol = 5)
> print(m)
     [,1] [,2] [,3] [,4] [,5]
[1,]    1    5    9   13   17
[2,]    2    6   10   14   18
[3,]    3    7   11   15   19
[4,]    4    8   12   16   20
> apply(m,1,median)
[1]  9 10 11 12
> apply(m,2,median)
[1]  2.5  6.5 10.5 14.5 18.5
> 
> 
> moda = function(x) {
+   z = table(as.vector(x))
+   names(z)[z == max(z)]
+ }
> 
> teste1 = moda(c(1,2,3,4,5,5,5))
> print(teste1)
[1] "5"
> 
> moda = function(x) {
+   z = table(as.matrix(x))
+   names(z)[z == max(z)]
+ }
> 
> teste2 = matrix(c(1, 2, 2, 3, 4, 2, 5, 5, 5), nrow = 3, ncol = 3)
> apply(teste2, 1, moda)
[[1]]
[1] "1" "3" "5"

[[2]]
[1] "2" "4" "5"

[[3]]
[1] "2"

> apply(teste2, 2, moda)
[[1]]
[1] "2"

[[2]]
[1] "2" "3" "4"

[[3]]
[1] "5"

> 
> print(teste2)
     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    5
[3,]    2    2    5
> 
> 
> 
> a <- c(1:20)
> x <- function(a){
+   resp = (a%%2 == 0)
+   return(resp)
+ }
> sapply(a,x)
 [1] FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE  TRUE
[15] FALSE  TRUE FALSE  TRUE FALSE  TRUE
> 
> 
> 
> 
> a <- c(1:20)
> x <- function(a){
+   resp = (a%%2 != 0)
+   return(resp)
+ }
> sapply(a,x)
 [1]  TRUE FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE  TRUE FALSE
[15]  TRUE FALSE  TRUE FALSE  TRUE FALSE
> 
> 
> 
> 
> dados1 <- read.table(file = "age.txt", header = T, sep = "", dec = ",")
Error in file(file, "rt") : cannot open the connection
> dados1 <- read.table(file = "age.txt", header = T, sep = "", dec = ",")
Error in file(file, "rt") : cannot open the connection
> 
> 
> dados1 <- read.table(file = "age.txt", header = T, sep = "", dec = ",")
> show(dados1)
> dados2 <- read.table(file = "teeth.txt", header = T, sep = "", dec = ",")
> show(dados2)
> dados3 <- cbind.data.frame(dados1, dados2)
> dados3 <- subset(dados3, select = -c(3))
> show(dados3)
> dados4 <- dados3[order(dados3[, 3])]
> show(dados4)
> 
> dados1 <- read.table(file = "age.txt", header = T, sep = "", dec = ",")
> show(dados1)
> dados2 <- read.table(file = "teeth.txt", header = T, sep = "", dec = ",")
> show(dados2)
> dados3 <- cbind.data.frame(dados1, dados2)
> dados3 <- subset(dados3, select = -c(3))
> show(dados3)
> dados4 <- dados3[order(dados3[, 3])]
> show(dados4)
> 
> 
> n <- 1:10
> for (i in 11) {
+   n
+   n * n
+   n * n * n
+ }
> tabela <- cbind.data.frame(n, n * n, n * n *n)
> show(tabela)
> 
> x = matrix(rep(1:100), nrow = 10, ncol = 10, byrow = T)
> dump("x", file = "dump.txt")
> rm(x)
> source("dump.txt")
> show(x)
      [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8] [,9] [,10]
 [1,]    1    2    3    4    5    6    7    8    9    10
 [2,]   11   12   13   14   15   16   17   18   19    20
 [3,]   21   22   23   24   25   26   27   28   29    30
 [4,]   31   32   33   34   35   36   37   38   39    40
 [5,]   41   42   43   44   45   46   47   48   49    50
 [6,]   51   52   53   54   55   56   57   58   59    60
 [7,]   61   62   63   64   65   66   67   68   69    70
 [8,]   71   72   73   74   75   76   77   78   79    80
 [9,]   81   82   83   84   85   86   87   88   89    90
[10,]   91   92   93   94   95   96   97   98   99   100
> 
> 
> x <- seq(-5, 5, by = 0.01)
> x <- x[(3*(x^2 - 1)) >= 0]
> 
> y.upper <- sqrt(3*(x^2 - 1))
> y.lower <- -sqrt(3*(x^2 - 1))
> y.max <- max(y.upper)
> y.min <- min(y.lower)
> d1 <- sqrt(3)*x
> d2 <- -sqrt(3)*x
> 
> plot(c(-5, 5), c(y.min, y.max), type = "n", xlab = "x", ylab = "y")
> lines(x, y.upper)
> lines(x, y.lower)
> lines(c(-.99, .99), c(0, 0), col = "blue")  
> lines(x,d1)
> lines(x,d2)
> points(2, 0)
> points(-2,0)
> text(2, 0, "focus (2, 0)", pos = 4)
> text(5, y.max, "asymptote y = sqrt(3)*x", pos = 2)
> title("Hiperbole x^2 - y^2/3 = 1")
> 
> 
> 
> library(spuRs)
Error in library(spuRs) : there is no package called ‘spuRs’
> install.packages(spuRs)
Error in install.packages : object 'spuRs' not found
> install.packages("spuRs")
Installing package into ‘/home/rstudio-user/R/x86_64-pc-linux-gnu-library/4.0’
(as ‘lib’ is unspecified)
trying URL 'http://package-proxy/src/contrib/spuRs_2.0.2.tar.gz'
Content type 'application/x-tar' length 203206 bytes (198 KB)
==================================================
downloaded 198 KB

* installing *binary* package ‘spuRs’ ...
* DONE (spuRs)

The downloaded source packages are in
	‘/tmp/RtmprJEjYc/downloaded_packages’
> library(spuRs)
> 
> data(ufc)
> head(ufc)
> str(ufc)
'data.frame':	336 obs. of  5 variables:
 $ plot    : int  2 2 3 3 3 4 4 5 5 6 ...
 $ tree    : int  1 2 2 5 8 1 2 2 4 1 ...
 $ species : Factor w/ 4 levels "DF","GF","WC",..: 1 4 2 3 3 3 1 1 2 1 ...
 $ dbh.cm  : num  39 48 52 36 38 46 25 54.9 51.8 40.9 ...
 $ height.m: num  20.5 33 30 20.7 22.5 18 17 29.3 29 26 ...
> 
> a <- ufc[order(ufc$height.m),]
> head(a)
> show(a)
> 
> h <- ufc[order(ufc$species),]
> head(h)
> 
> b <- aggregate(ufc$dbh.cm, by=list(ufc$species), FUN = mean)
> show(b)
> 
> 
> c <- summary(ufc$dbh.cm)
> show(c)
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
  10.10   24.80   35.00   37.41   47.15  101.50 
> 
> 
> 
> e <- aggregate(ufc$dbh.cm, by=list(ufc$species), FUN = max)
> head(e)
> x <- aggregate(ufc$height.m, by=list(ufc$species), FUN = max)
> head(x)
> 
> e <- aggregate(ufc$dbh.cm, by=list(ufc$species), FUN = max)
> head(e)
> x <- aggregate(ufc$height.m, by=list(ufc$species), FUN = max)
> head(x)
> max(x[,2])
[1] 47
> 
> 
> b <- aggregate(ufc$dbh.cm, by=list(ufc$species), FUN = mean)
> head(b)
> max(b[, 2])
[1] 39.90526
> 
> 
> atv4 <- data.frame(
+   nome = as.factor(c("Joao Silva", "Pedro Silva", "Amanda Silva", "Fabio Silva", "Fernanda Silva", 
+                      "Gustavo Silva", "Larissa Silva", "Jonas Silva", "Ada Silva", "Angela Silva")),
+   idade = c(22, 21, 18, 20, 23, 19, 23, 30, 29, 25),
+   sexo = as.factor(c("masculino", "masculino", "feminino", "masculino", "feminino", 
+                      "masculino", "feminino", "masculino", "feminino", "feminino")),
+   escolaridade = as.factor(c("ensino medio", "ensino medio", "ensino medio", "ensino medio",
+                              "ensino medio", "ensino medio", "ensino medio", "ensino medio",
+                              "ensino medio", "ensino medio")),
+   renda = c(800, 750, 900, 500, 1000, 1500, 800, 3000, 900, 900))
> show(atv4)
> write.table(atv4, file = "atv4.txt", sep="", row.names = FALSE,
+             col.names = FALSE)
> #a
> subset(atv4, sexo == "feminino", c("nome", "idade", "sexo", "escolaridade", "renda"))
> subset(atv4, sexo == "masculino", c("nome", "idade", "sexo", "escolaridade", "renda"))
> #b
> sapply(Filter(is.numeric, atv4), mean)
idade renda 
   23  1105 
> #c
> atv4[with(atv4, order(sexo)),]
> atv4[with(atv4, order(escolaridade)),]
> #d
> atv4$nivelsocioeconomico <- c("C2", "C2", "D", "C2", "C2", "C2", "C2", "C1", "C2", "C2")
> show(atv4)
> #e
> atv4 <- ftable(atv4[c(3,6)])
> atv4
          nivelsocioeconomico C1 C2 D
sexo                                 
feminino                       0  4 1
masculino                      1  4 0
> 
> 
> 
> install.packages("rmdformats")
Installing package into ‘/home/rstudio-user/R/x86_64-pc-linux-gnu-library/4.0’
(as ‘lib’ is unspecified)
also installing the dependency ‘bookdown’

trying URL 'http://package-proxy/src/contrib/bookdown_0.21.tar.gz'
Content type 'application/x-tar' length 960703 bytes (938 KB)
==================================================
downloaded 938 KB

trying URL 'http://package-proxy/src/contrib/rmdformats_1.0.0.tar.gz'
Content type 'application/x-tar' length 1901269 bytes (1.8 MB)
==================================================
downloaded 1.8 MB

* installing *binary* package ‘bookdown’ ...
* DONE (bookdown)
* installing *binary* package ‘rmdformats’ ...
* DONE (rmdformats)

The downloaded source packages are in
	‘/tmp/RtmprJEjYc/downloaded_packages’
Error in yaml::yaml.load(..., eval.expr = TRUE) : 
  Scanner error: mapping values are not allowed in this context at line 8, column 16
We have detected that your installed R packages need to be re-installed to work with the new OS version.
See https://community.rstudio.com/t/rstudio-cloud-ubuntu-16-04-eol-on-sept-13-2021/113409 for more details.
Please wait while we re-install your R packages.
You can look in the jobs pane to check progress...
> 
