# MEGAHIT


MEGAHIT is de novo NGS assembler for assembling large and complex metagenomics data.MEGAHIT is used for Metagnomic assembly via succint de Bruijn graph.MEGAHIT can be installed via conda or Docker image

# Installation via Conda

conda install -c bioconda megahit

# Built a Docker image
Commands for builting Docker image in linux 

# First get the Docker installed on Ubuntu by following the commands

> sudo apt install docker.io

> sudo snap install docker

> docker --version

# For metagenomics megahit docker images ;

mkdir metagenomic

cd ~/metagenomic/

docker build -t megahit .

docker run -v ~/metagenomic:/data -i -t megahit /bin/bash

This command mount the metagenomic directory as /data within the image

The Docker file must be downloaded from the files of this repository

# Usuage

megahit -1 sample_R1.fastq -2 sample_R2.fastq -t 12 -o megahit.out # this command is for pair end fastq files to run megahit

-t 12 use 12 treads(number of parallel processors)







