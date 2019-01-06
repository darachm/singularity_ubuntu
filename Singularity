Bootstrap: docker
From: ubuntu:18.04

%labels
MAINTAINER darachm
DATE 190104

%help

    This is a base for debugging Singularity builds.
    
%post

    apt-get -y update
    apt-get -y install gnupg2 software-properties-common
    apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
    add-apt-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/' 

    apt-get -y update
    apt-get -y upgrade
    apt-get -y install git wget g++ gcc-4.8 r-base r-base-dev curl libcurl4-openssl-dev

    Rscript -e 'install.packages("BiocManager"); BiocManager::install()'
    Rscript -e 'BiocManager::install(c("Rcpp","RCurl","Biostrings", "ggplot2", "data.table", "reshape2", "ShortRead", "RcppParallel", "IRanges", "XVector", "BiocGenerics"))'

%test

    # ?
