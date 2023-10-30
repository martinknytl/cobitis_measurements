# cobitis_measurements
combination of Bash and R scripting

measurements of chromosomal arms created in Google Sheets. Each table of measurement downloaded as Tab Separated Values '.tsv' under the name cobitis_chr_length_and_p-q_arm_ratio-metafasename.tsv
in Bash: empty columns (p arms of Telocentric chromosomes) were substituted with 0. Code for the first cbi14 table:

Cobitis bilseli:
```
awk -F"\t" -v OFS="\t" '{ for(N=1; N<=NF; N++) if($N=="") $N="0" } 1' cobitis_chr_length_and_p-q_arm_ratio-cbi14.tsv  > cobitis_chr_length_and_p-q_arm_ratio-cbi14II.tsv
```

Cobitis fahireae:

```
awk -F"\t" -v OFS="\t" '{ for(N=1; N<=NF; N++) if($N=="") $N="0" } 1' cobitis_chr_length_and_p-q_arm_ratio-cfa1.tsv  > cobitis_chr_length_and_p-q_arm_ratio-cfa1II.tsv
```
