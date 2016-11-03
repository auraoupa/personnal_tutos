# Outil mkmov #

* purpose : produce movies from netcdf files or concatenate png files in a movies
* source :  https://github.com/chrisb13/mkmov

## Install ##

* git clone https://github.com/chrisb13/mkmov
* conda install -c menpo ffmpeg=3.1.3

## Successful example ##

* python mkmov.py 2d --bias  time_counter --bcmapcentre --cmap seismic --min -.4 --max .7  --lmask 0 zos examples/cordex24-ERAI01_1d_20040101_20040111_grid_T_2D.nc examples/cordex24-ERAI01_1d_20040101_20040111_grid_T_2D.nc
* result : https://youtu.be/J0xaRKMl5GQ

## My first attempt ##

* python mkmov.py 2d  --min 0 --max 1 -o /home/albert/Work/mkmov/movies/NATL60-CJM165-TRCsurf_y2013.mov TRC NATL60-TRC-2013/NATL60-CJM165_y2013.1d_ptrcT_surf.nc
* result : https://youtu.be/9EdpYhSjr7Y

## Other features ##

* same movie with date on it : python mkmov.py 2d  --min 0 --max 1 -o /home/albert/Work/mkmov/movies/NATL60-CJM165-TRCsurf_y2013.mov --tstart '2013-01-02' --tdelta '1_D' --x2d nav_lon --y2d nav_lat TRC NATL60-TRC-2013/NATL60-CJM165_y2013.1d_ptrcT_surf.nc

* result : https://youtu.be/piL4MsI8V4A

## The follwing successful attempts ##

* python mkmov.py 2d --min -5 --max 5 --x2d nav_lon --y2d nav_lat -o /home/albert/Work/mkmov/movies/NATL60QNE-CJM165_y2012.1d_curloverf.mov socurloverf ~/Data/NATL60/NATL60-CJM165-S/1d/2012/NATL60QNE-CJM165_y2012.1d_curloverf.nc

## Fails ##

* python mkmov.py 2d --min -1 --max 1 -o /home/albert/Work/mkmov/movies/NATL60-CJM165_y2012_curloverf.mov --tstart '2012-06-14' --tdelta '1_D' --x2d nav_lon --y2d nav_lat socurloverf NATL60/NATL60-CJM165_y2012.1d_curloverf.nc
  * after 45 frames => "Processus arrêté"
  * explication : fichier netcdf produit par le cdftool cdfcurl pas compatible, mettre l'option -nc4
  * de plus, fichier trop gros, faire les films avec les quartiers de NATL60 pas plus d'un an et sans oublier les options --x2d --y2d (projection sur la grille = moins de pixels)
