# EmonFritzing
[Fritzing](http://fritzing.org/home/) parts for the various OpenEnergyMonitor boards.

## Creating new parts

These parts are mainly created using [eagle2fritzing](https://github.com/jeremypoulter/eagle2fritzing). For info on how to use this have a look at;
- https://learn.adafruit.com/make-beautiful-fritzing-parts-with-eagle2fritzing-brd2svg
- https://youtu.be/-84EdGnwP-Y

Here is a little bit of bash to report on all the missing parts;
```
./run.sh 2>&1 | tee log.txt && cat log.txt | grep "subpart not found" | sort
| uniq | tee missing_sub_parts.txt && echo `wc -l missing_sub_parts.txt | cut -
d\  -f 1` missing parts
```
