## Script-for-Translocation-detection
## Introduction
This script is based on the chromatin interaction clustering to detect inter-chromosomal translocations in cancer Hi-C data up to 1kb resolution. 
(co-developer Hao Jiang)
For complete information please read (https://www.frontiersin.org/articles/10.3389/fcell.2021.706375/full) 
### The script requires the following dependencies:
> 1) &nbsp; python (≥ 2.7) <br/>
> 2) &nbsp; matplotlib (≥ 2.3.1) <br/> 
> 3) &nbsp; scipy  (≥ 0.5.1)<br/>
> 4) &nbsp; numpy ( ≥ 1.18) <br/>
> 5) &nbsp; java ( ≥ 1.8.0_91) <br/> 
## Usage
    java in-house_script.jar [-bd <int>] -f <string> [-l <int>] [-minc <int>] [-minl <int>] [-ml <int>] [-o <path>] [-p <string>] [-pv <float>] s <file> [-sort] [-t <int>] 
    
     -bd <int>              min breakpoint distance, if two breakpoints distance less than this value, it will be merged (defalut 100k) 
     -f,--bedpe <string>    Interaction bedpe file 
     -l <int>               extend length (defalut 10k) 
     -minc <int>            min cluster count (default 70)
     -minl <int>            min region distance (default 5k) 
     -ml <int>              cluster merge length (defalut 1M) 
     -o,--out <path>        output path 
     -p,--prefix <string>   output prefix 
     -pv <float>            P value (default 5e-5) 
     -s <file>              chr size file  
     -sort                  if your input file don't sort before, add this argument 
     -t,--thread <int>      threads  
    
## Example   
    java -jar in_house_script.jar -f input.bedpe -p test_out -s chr.size -t 1 -l 20000
    bedpe: Hi-C file 6 column
   
-----------------------------------------------------------------------------------------------------------------
#### &nbsp;CopyRight &#169; 2021 [Guoliang's Lab](http://glab.hzau.edu.cn/index.php), All Rights Reserved
