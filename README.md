
<br/>
<img width="850" height="272" alt="København" src="https://github.com/user-attachments/assets/14910d4e-5a1a-4257-9ea0-6b1d7ab054f7" />
<br/>

# SPOR
>[!IMPORTANT]
>Det følgende datasæt inkludere potentielt stødende materiale.
## Baggrund
<br/>
Mellem 1867 og 1920 udgav det danske politi et blad kaldet "Politiets Efterretninger", som, bredt forstået, indeholdt relevant information om kriminel aktivitet, der blev cirkuleret rundt politiafdelinger henover Danmarks areal. På sin vis er der tale om datidens døgnrapporter. I forbindelse med et kursus på kandidatuddannelsen i historie på Aalborg Universitet og i samarbejde med Københavns Stadsarkiv, er materialet fra 1867-1890 blevet digitaliseret og tilgængeliggjort. Denne side dokumenterer processens forskellige trin og deres bagvedliggende rationaler.
<br/>

## Usage & Requirements
* R Studio 3.0+
* Excel

```
library(readxl)
df <- readxl(insertnameofexceldocumenthere.xlsx)
```
<br/>

## Documentation
Følgende datasæt er baseret på overleveret indskanninger fra Københavns stadsarkiv. I alt sidder datasættet på cirka 16000 sider værd af information fra Politiets efterrettninger i perioden 1867-1890. <br/>
Primær informationsprocessering er fortaget igennem Transkribus. Dataen blev derefter valideret og checket af en gruppe af studerne hvorefter at datasættet er blevet linket til at starte med en ```Word2Vec``` <br/> model med følgende parameter

```
set.seed(1234)

w2v <- word2vec(toks,
                dim = 150,
                threads = 3,
                hs = TRUE,
                iter = 15,
                min_count = 5, 
                window = 5,
                verbose = TRUE)
```



