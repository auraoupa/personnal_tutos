# Manage environments with conda

- conda create --name snowflakes biopython
- source activate snowflakes
- conda env list

- export and share

 - here : conda env export > environment.yml
 - there : conda env create -f environment.yml + activate



- build identical env
   - conda list --explicit > spec-file.txt
   - conda create --name MyEnvironment --file spec-file.txt
   - conda install --name MyEnvironment --file spec-file.txt (different laptop but same platform)


