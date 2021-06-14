## script-for-translocation-detection
## Introduction
This script is based on the chromatin interaction clustering to detect inter-chromosomal translocations in cancer Hi-C data up to 1kb resolution. 
(Developed by Hao Jiang)            
### The script requires the following dependencies:
> 1) &nbsp; python (≥ 2.7) <br/>
> 2) &nbsp; matplotlib (≥ 2.3.1) <br/> 
> 3) &nbsp; scipy  (≥ 0.5.1)<br/>
> 4) &nbsp; numpy ( ≥ 1.18) <br/>
> 5) &nbsp; java ( ≥ 1.8.0_91) <br/> 
## Usage
    java -cp path/in-house_script.jar TLD.TransLocationDetection[-bd <int>] -f <string> [-l <int>] [-minc <int>] [-minl <int>] [-ml <int>] [-o <path>] [-p <string>] [-pv <float>] s <file> [-sort] [-t <int>] <br />   
    
     -bd <int>              min breakpoint distance, if two breakpoints distance less than this value, it will be merged (defalut 100k) <br />
     -f,--bedpe <string>    Interaction bedpe file <br />
     -l <int>               extend length (defalut 10k) <br />
     -minc <int>            min cluster count (default 70) <br />
     -minl <int>            min region distance (default 5k) <br />
     -ml <int>              cluster merge length (defalut 1M) <br />
     -o,--out <path>        output path <br />
     -p,--prefix <string>   output prefix <br />
     -pv <float>            P value (default 5e-5) <br />
     -s <file>              chr size file  <br />
     -sort                  if your input file don't sort before, add this argument <br />
     -t,--thread <int>      threads <br />   
    
## Example   
    java -jar in_house_script.jar -f input.bedpe -p test_out -s chr.size -t 1 -l 20000
    bedpe: Hi-C file 6 column
   
-----------------------------------------------------------------------------------------------------------------
#### &nbsp;CopyRight &#169; 2021 [Guoliang's Lab](http://glab.hzau.edu.cn/index.php), All Rights Reserved
