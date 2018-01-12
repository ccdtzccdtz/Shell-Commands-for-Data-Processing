
## wc
#### count number of lines in a csv
`wc -l data.csv`
#### count number of words in a csv
`wc -w data.csv`
#### count number of files in a folder: feed `ls` result to`wc -l`
`ls -l <folder> | wc -l`

## head and tail
#### first n lines or last n lines of a csv
`head -n 2 data.csv`

`head -n 120 data.csv | tail -n 20 > 1.csv`

## cat
#### Concatenate multiple files
`cat 1.csv 2.csv > merge.csv`

## sed
#### replace "?" with empty string
`sed "s/, ?,/,,/g" 1.csv >  1.csv`

## uniq and sort
`uniq -c`: which adds the repetition count to each line;
`uniq -d`: which only outputs duplicate lines; And
`uniq -u`: which only outputs unique lines.
#### finding duplicate lines in a file
`sort 1.csv | uniq -d | wc -l`

## cut
#### select 2nd column of a csv
`cut -d "," -f 2 data.csv | head -3`
