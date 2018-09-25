```
for sample in $(cat samples); \
do echo "On sample: $sample"; \
pandaseq -f "$sample"_16S_R1.fq -r "$sample"_16S_R2.fq -T 6 -w "$sample"_ps_aligned.fa; \
done;
```
```
for sample in $(cat samples); \
do echo "On sample: $sample"; \
header_rename.py -f "$sample"_ps_aligned.fa -s "$sample" >> ps_aligned_all.fa; \
done;
```