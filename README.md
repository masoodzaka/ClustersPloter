# ClustersPloter
### Usage:<br>
```
%  git clone http://github.com/orangeSi/ClustersPloter.git
%  cd  ClustersPloter/example/
%  cat work.sh # output svg and html
# or go to https://clustersploter.readthedocs.io/en/latest/# 
```


### Dependence<br>
```
samtools >=1.7 # add this to linux PATH 
perl >=v5.10.1
sort
```

### Features:<br>
- plot gene clusters of many samples, one track means one sample, one track contain more than one fragments. one fragment contain gene cluster. you can defined every gene or feature(rotation,color,label,order depth,font size) in clusters. And add crossing link for any pair of genes.<br>
- every track mean one sample , one sample can has more than one fragments. you can defind the feature color/lable font size/label color/label rotaion in feature.color.label.conf <br>
- you can draw crosslink or sysnteny among features of different tracks<br>
- illunimate pair-end or mate-pair reads or pacbio/nanopore long reads mapping with varation(indel, sv) in bam, support snpindel in vcf file<br>

### Update:<br>
#### 2018-12-28:<br>
- add html format output, so you can pan or zoom the svg in html<br>
#### 2018-12-21:<br>
- add synteny between genomes, only support paf(like minimap2 ouput) format yet. test is example/out7.sh<br>
#### 2018-12-20:<br>
- support indel of cigar or indel in vcf now, but not support snp yet. test is example/out11.sh<br>
#### 2018-12-10:<br>
- add  plot depth and pabio read mapping of bam file, as example/out11.svg or out10.svg , inspired by  https://github.com/nspies/genomeview <br>
#### 2018-11-12:<br>
- rewrite feature.crossing.link.conf so that defined color and opactity or order or anchor position of every pair of links.<br>
- add tracks_reorder to plot tracks by new order, otherwise you must adjust --list file <br>
#### 2018-11-07:<br>
- feature_shaple now support <b>circle_point</b>/rect/arrow, add <b>feature_shift_y</b>, as example/out10.svg. combine with <b>feature_height_ratio</b> or <b>feature_shift_y</b>, try to plot <b>line</b> or <b>scatter</b> or <b>heatmap</b> or <b>histogram</b> is possible but hard for much data points, I will try do this by embed svg in svg, the embedded svg is producted by python or R tool(such as https://github.com/nspies/genomeview or https://github.com/svviz/svviz), and the linux convert not support embed svg, but cairosvg support it (should use the absoluted embedded svg path)!<br>
#### 2018-10-29:<br>
- redesign the the main.conf and feature.crossing.link.conf to make more freely to reset every feature, reset every link color and opacity one by one, and reset order depth of every feature or crosslink or track, reset feature height one by one as in out2.svg<br>
- add rect for feature shape, now have arrow and rect, you can use arrow and rect at the same time<br>
- remove the legend border line<br>
<br>

#### Note:<br>
```
```

#### ToDo:<br>
&nbsp;&nbsp;**2018-12-28**:<br>
&nbsp;&nbsp;&nbsp;&nbsp;1. add gtf fomrat, not only gff format<br>
&nbsp;&nbsp;&nbsp;&nbsp;2. add blat_spl and mummer4 fomrat, not only blast_m8 or paf format<br>
&nbsp;&nbsp;**2018-11-09**:<br>
&nbsp;&nbsp;&nbsp;&nbsp;1. sort by feature,so same feature of different tracks can align centre<br>
&nbsp;&nbsp;&nbsp;&nbsp;2. add ratio scale in the bottom to recognise the approximate length of every feature <br>
&nbsp;&nbsp;&nbsp;&nbsp;3. embed svg in svg to make heatmap or scatter or line or histogram more easy to product, like example/out.svg*svg or \<foreignObject\> <br> <br>



```
cat example/work.sh
```
![gene cluster image](example/out3.notitle.png)
<br><br><br>
![gene cluster image](example/out2.notitle.png)
<br><br><br>
![gene cluster image](example/out1.notitle.svg)
<br><br><br>
![gene cluster image](example_old/out7.notitle.svg)
<br><br><br>
![gene cluster image](example_old/out10.notitle.svg)
<br><br><br>
![gene cluster image](example_old/out.notitle.svg)
<br><br><br>
![gene cluster image](example_old/out2.notitle.svg)
<br><br><br>
![gene cluster image](example_old/out3.notitle.svg)
<br><br>
![gene cluster image](example_old/out3.2.notitle.svg)
<br><br>
![gene cluster image](example_old/out8.notitle.svg)
<br><br><br>

contact:<br>
&nbsp;&nbsp;&nbsp;&nbsp;QQ: 1522051171<br>
&nbsp;&nbsp;&nbsp;&nbsp;mail: ilikeorangeapple@gmail.com
