## 1. Paths
```bash
export PATH=/etc/alternatives/java_sdk_11/bin/java:$PATH
export PATH=$PATH:/private/inp/.julia/juliaup/julia-1.10.0+0.x64.linux.gnu/bin
export PATH=$PATH:/private/inp/MYSRC
export PATH=$PATH:/private/inp/.localpython313/bin
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/prog/ow/R5000/oracle/lib
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/prog/oracle/11.2.0/lib
```

## 2. Variables used
```bash
export GEOLOG_CURRENT=/prog/pg/current/geolog/current/geolog_current
export LFP=/project/geolog/Epos/INT_SVG/LFP
export LOGLAN=/project/geolog/Epos/INT_SVG/LFP/loglan
export MYSRC=/private/inp/MYSRC
export ORACLE=/prog/oracle/11.2.0
export PACKAGES_LOCAL_PYTHON=/prog/pg/utils/Python38/lib/python3.8/site-packages
export WORKON_HOME=~/Envs
```

## 3. JavaScript functions based on Python
```bash
function calc() {    
    python -c "from math import *; from numpy import *; from scipy import *; print(eval('$1'))"
}
function salinity_from_log10rw_t() {   
    python -c "from .MYSRC.misc import salinity_from_log10rw_t; print(salinity_from_log10rw_t($1, $2))"
}
```

## 4. Read in my file of aliases
```bash
source ./.bash_aliases
```

## 5. >>> juliaup initialize >>>
```bash
case ":$PATH:" in
    *:/private/inp/.juliaup/bin:*)
        ;;

    *)
        export PATH=/private/inp/.juliaup/bin${PATH:+:${PATH}}
        ;;
esac
# <<< juliaup initialize <<<
```


