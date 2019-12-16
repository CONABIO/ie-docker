FROM rocker/geospatial:3.6.1

RUN sudo chmod gou+w /usr/local/lib/R/site-library && sudo chmod gou+w /usr/local/lib/R/library && \
    sudo R -e 'install.packages("BiocManager",repos="http://cran.us.r-project.org",lib="/usr/local/lib/R/site-library")' && \
    sudo R -e 'BiocManager::install()' && \
    sudo R -e 'BiocManager::install(c("bnlearn"))' && \
    sudo R -e 'BiocManager::install(c("graph", "Rgraphviz", "RBGL"));BiocManager::install("gRain");BiocManager::install("gRbase")'
