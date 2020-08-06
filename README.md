# TwitterNodeAnalysisTesla

Item_Nodes <- read.csv("/Users/yeeiriser/Desktop/nodesTesla.csv",head=TRUE,sep=",")
Item_Edges <- read.csv("/Users/yeeiriser/Desktop/edgesTesla.csv",head=TRUE,sep=",")

library(visNetwork)
library(igraph)

visNetwork(Item_Nodes, Item_Edges, width = "100%", height="600px")  %>%
    # visIgraphLayout(layout = "layout_nicely") %>%
    visEdges(arrows = "middle", smooth = T) %>%
    visLegend() %>%
    visLayout(randomSeed = 12) 
