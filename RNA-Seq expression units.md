RPKM, FPKM and TPM, Clearly Explained!!!
https://www.youtube.com/watch?v=TTUrtCY2k-w

What the FPKM? A review of RNA-Seq expression units
https://haroldpimentel.wordpress.com/2014/05/08/what-the-fpkm-a-review-rna-seq-expression-units/#:~:text=Therefore%2C%20let's%20clear%20one%20thing,simply%20a%20unit%20of%20expression.&text=fragments%20you've%20sequenced.,to%20make%20it%20more%20convenient.


#### RPKM - Reads Per Kilobase Million
    
  is for single end RNA-Seq
    
#### FPKM - Fragments Per Kilobase Million
    
  is for paired end RNA-Seq
    
  *FPKM keeps track of fragments so that one with two reads are not count twice 
    
These normalize reads counts for

<pre><code>
1 - The sequencing depth (that's the "million" part)
    - Sequencing runs with more depth will have more reads mapping to each gene

2 - The gene length (that's the "kilobase" part)
    - longer genes will have more reads mappingto them
</code></pre>

Primeiro, para cada amostra você calcula o "total reads" (de cada coluna) e divide por 1.000.000. Depois você divide os reads de cada gene por esse valor obtido. Dessa forma você calculou o RPM. O próximo passo é dividir os valores de RPM pelo "gene length", obtendo o RPKM. 

<pre><code>
Assim: 1 - Normalized for differences in sequencing depth and 2 - Normalized for gene size.
</code></pre>

#### TPM - Transcripts Per Million

  is like RPKM and FPKM, except for the order of operations, which are switched

Primeiro, você divide os valores de counts por "gene length", obtendo o RPK. Logo após você calcula o "total reads" (de cada coluna), divide por 1.000.000 e divide os RPK de cada gene por esse valor obtido. Dessa forma você calculou o TPM.

<pre><code>
Assim: 1 - Normalized for gene size and 2 - Normalized for differences in sequencing depth.
</code></pre>

Os dois (TPM e RPKM/FPKM) corrigem viéses em "gene length" e "sequencing depth", porém
  as somas de cada coluna (valores da amostra) são bem diferentes
  em RPKM/FPKM nós obtemos valores diferentes para cada amostra (tortas de diferentes tamanhos)
  em TPM nós obtemos os mesmos para cada amostra (tortas de tamanhos iguais)
  
  É possível comparar os tamanhos de fatias (expressões relativa de genes) de tortas entre tortas de mesmo tamanho.
  
  Com RPKM/FPKM, é mais difícil comparar as proporções de "total reads" porque cada coluna possui um valor total diferente (tortas de diferentes tamanhos, p.e. o valor 1, do gene, de 5, da torta, é diferente de 1, do gene, de 3, da torta. 1/5 = 0.20, 1/3 = 0.33).
  
  Uma vez que RNA-Seq é sobre a comparação de proporções de read, esta métrica parece estar mais apropriada. 
