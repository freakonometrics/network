    library(networkD3)
    library(network)

    ## network: Classes for Relational Data
    ## Version 1.13.0 created on 2015-08-31.
    ## copyright (c) 2005, Carter T. Butts, University of California-Irvine
    ##                     Mark S. Handcock, University of California -- Los Angeles
    ##                     David R. Hunter, Penn State University
    ##                     Martina Morris, University of Washington
    ##                     Skye Bender-deMoll, University of Washington
    ##  For citation information, type citation("network").
    ##  Type help("network-package") to get started.

    library(sna)

    ## Loading required package: statnet.common

    ## sna: Tools for Social Network Analysis
    ## Version 2.4 created on 2016-07-23.
    ## copyright (c) 2005, Carter T. Butts, University of California-Irvine
    ##  For citation information, type citation("sna").
    ##  Type help(package="sna") to get started.

    library(igraph)

    ## 
    ## Attaching package: 'igraph'

    ## The following objects are masked from 'package:sna':
    ## 
    ##     betweenness, bonpow, closeness, components, degree,
    ##     dyad.census, evcent, hierarchy, is.connected, neighborhood,
    ##     triad.census

    ## The following objects are masked from 'package:network':
    ## 
    ##     %c%, %s%, add.edges, add.vertices, delete.edges,
    ##     delete.vertices, get.edge.attribute, get.edges,
    ##     get.vertex.attribute, is.bipartite, is.directed,
    ##     list.edge.attributes, list.vertex.attributes,
    ##     set.edge.attribute, set.vertex.attribute

    ## The following objects are masked from 'package:stats':
    ## 
    ##     decompose, spectrum

    ## The following object is masked from 'package:base':
    ## 
    ##     union

    library(ggnet)

    library(network)
    data(flo)
    net = network(flo, directed = FALSE)
    plot(net,displaylabels=TRUE,boxed.labels=FALSE)

![](networks_files/figure-markdown_strict/unnamed-chunk-2-1.png)

    ggnet2(net,label=TRUE)

    ## Loading required package: scales

![](networks_files/figure-markdown_strict/unnamed-chunk-3-1.png)

    g=graph_from_adjacency_matrix(flo)
    e=E(g)
    v=V(g)
    plot(g)

![](networks_files/figure-markdown_strict/unnamed-chunk-4-1.png)

    df=as.data.frame(ends(g, E(g)))
    names(df)=c("src","target")
    simpleNetwork(df)

<!--html_preserve-->

<script type="application/json" data-for="htmlwidget-59d881ec94a6ee1d350a">{"x":{"links":{"source":[0,1,1,1,2,2,3,3,3,4,4,4,5,6,6,6,6,7,8,8,8,8,8,8,9,10,10,10,11,11,11,12,12,13,13,13,13,14,14,14],"target":[8,5,6,8,4,8,6,10,13,2,10,13,1,1,3,7,14,6,0,1,2,11,12,14,12,3,4,13,8,13,14,8,9,3,4,10,11,6,8,11],"value":[1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1],"colour":["#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666","#666"]},"nodes":{"name":["Acciaiuoli","Albizzi","Barbadori","Bischeri","Castellani","Ginori","Guadagni","Lamberteschi","Medici","Pazzi","Peruzzi","Ridolfi","Salviati","Strozzi","Tornabuoni"],"group":[1,1,1,1,1,1,1,1,1,1,1,1,1,1,1],"nodesize":[8,8,8,8,8,8,8,8,8,8,8,8,8,8,8]},"options":{"NodeID":"name","Group":"group","colourScale":"d3.scaleOrdinal(['#3182bd'])","fontSize":7,"fontFamily":"serif","clickTextSize":17.5,"linkDistance":50,"linkWidth":"'1.5px'.toString()","charge":-30,"opacity":0.6,"zoom":false,"legend":false,"arrows":false,"nodesize":true,"radiusCalculation":"d.nodesize","bounded":false,"opacityNoHover":1,"clickAction":null}},"evals":[],"jsHooks":[]}</script>
<!--/html_preserve-->
