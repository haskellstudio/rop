# ROP
Read Origin Protocol (ROP)

How to run job array on hoffman2:

1) ls *sh | awk '{i+=1;print "if [ $1 == "i" ];then ./"$1" ;fi"}' > myFunc.sh
2) wc -l myFunc.sh

3) qsub -cwd -V -N rop1 -l h_data=16G,time=06:00:00 -t 1-x:1 myFuncFastWrapper.sh



