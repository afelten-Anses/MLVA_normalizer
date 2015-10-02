Title: MLVA_normalizer README

Author: Paul Bachelerie

Affiliation: [Université PARIS-EST (France)](http://www.univ-paris-est.fr/), [Food Safety Laboratory – ANSES Maisons Alfort (France)](https://www.anses.fr/en/content/laboratory-food-safety-maisons-alfort-and-boulogne-sur-mer)

You can find the latest version of the tool at 
https://github.com/afelten-Anses/MLVA_normalizer

HTML and pdf user technical documentation are available in the 'doc/' directory.

A sample dataset to test the script is available in the 'dataset/' directory.


MLVA_normalizer
===============

MLVA_normalizer is a script conceived to normalize MLVA (Multiple Loci VNTR Analysis) results and allow data exchanges between laboratories. Indeed even if MLVA is a typing tool used at today to characterize several major pathogens as Brucella, Mycobacterium tuberculosis or Salmonella, the results obtained are instrument dependent and cannot be compared between laboratories without normalization. This script is conceived to be applied to any bacterial genera and is not depending from the MLVA protocol used.

MLVA_normalizer is composed of 1 scripts written in python :

 * MLVA_normalizer loads two input files: a file containing data of the reference strains and a file with data for the sample strains.


Quick Start
===========

## run it on Linux/Mac OS X system

Simply run the command in the 'src/' directory :

	 ./MLVA_normalizer


Dependencies
============

MLVA_normalizer needs python 2.7 (tested with 2.7.5), you can donwload it here :

* [python](https://www.python.org/ftp/python/2.7.5/Python-2.7.5.tar.xz)


MLVA_normalizer Parameters
==========================

##  MLVA_normalizer parameters

 * '-h': help, show instructions
 * '-r': input file, containing the data of the panel of the reference strain (example : 'references/ref_typhimurium.txt')
 * '-d': input file, containing data for the sample strain (example : 'capillary_electrophoresis.txt')
 * '-o': output prefix name ['output']

The input files must be in 'txt' or 'csv' format with a tabulation as column separator. The name of the VNTR (Variable Number of Tandem Repeats) loci from the '-d' input file must be  the same with those of the '-r' input file. 


Ouput
======

##  MLVA_normalizer output

MLVA_normalizer generates an output table which includes the corrected MLVA profiles and lengths of each tandem repeat.


MLVA_normalizer test
====================

The workflow can be tested with the dataset included in the 'dataset' directory.

Simply run the command in the 'src/' directory :

	./MLVA_normalizer -r ../references/ref_typhimurium.txt -d ../dataset/capillary_electrophoresis.txt -o results


Reference strains
=================

A Salmonella reference input file is provided as example with the workflow for the serovars Typhimurium, Enteritidis. 

