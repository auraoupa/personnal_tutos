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

## Fails ##

* 
