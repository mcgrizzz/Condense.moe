**If you're using conda, switch to the koemoe conda environment**
``` { .bash .copy }
conda activate 'koemoe'
```
### Quick Start and Examples
#### Single File
Condense a **single file**, `Anime_S01E01.mkv`
``` { .bash .copy }
python './condense.py' 'X:/anime/Anime_S01E01.mkv'
```
#### Folder
Condense a every video file in a **folder**, `X:/anime/`
  
``` { .bash .copy }
python './condense.py' 'X:/anime/'
```

!!! note
    The rest of the examples are run for a **folder**, but work the same on **single files**

#### Include OP and ED
!!! terminal "**`-io`** _`--include-op`_ &nbsp;&nbsp;&nbsp;&nbsp; **`-ie`** _`--include-ed`_"
``` { .bash .copy }
#Include the opening
python './condense.py' -io 'X:/anime/'

#Include the ending
python './condense.py' -ie 'X:/anime/'

# Include both
python './condense.py' -io -ie 'X:/anime/'
```

#### Change the output directory
!!! terminal "`-o` _`--output-dir`_"

``` { .bash .copy }
python './condense.py' -o 'X:/condensed_anime/' 'X:/anime/'
python './condense.py' --output-dir 'X:/condensed_anime/' 'X:/anime/'
```

#### Change the output name or format
!!! terminal "`-f` _`--output-format`_"

``` { .bash .copy }
python './condense.py' -f "$name$_condensed.wav" 'X:/anime/'
python './condense.py' --output-format "$name$_condensed.wav" 'X:/anime/'
```

