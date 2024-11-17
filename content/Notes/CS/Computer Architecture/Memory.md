## Caches
### Placement Schemes
#### Direct Map Cache
A cache structure that each memory location is exactly mapped to a fixed position in the cache.
$$
(Block\ address)\ modulo\ (Number\ of\ blocks\ in\ the\ cache)
$$
##### Fields
- Tag: A field in a table used for a memory hierarchy that contains the address information required to identify whether the associated block in the hierarchy corresponds to a requested word.
- Valid bit: A field in the tables of a memory hierarchy that indicates that the associated block in the hierarchy contains valid data.
#### Fully Associative Cache
A cache structure that each block can be put in any location in the cache.
#### Set Associative Cache
A cache structure that each block can be put in a fixed set of locations in the cache.
$$
(Block\ address)\ module\ (Number\ of\ sets\ in\ the\ cache)
$$
##### Fields
- Index: Used to select the set
- Tag: Used to choose the block by comparison with the blocks in the set
- Block offset: Address of desired data within the block
### Replacement Schemes
#### Least Recently Used(LRU)
A replacement scheme in which the block be replaced is the one that has been unused for the longest time.
#### Random
Candidate blocks are randomly selected, possibly using some hardware assistance.
### Write Schemes
#### Write-Through
A write scheme that writes always update the cache and the next lower level of the memory hierarchy to ensure the data consistency.
- write buffer: A queue that holds data while the data are waiting to be written to memory.
#### Write-Back
A scheme that updates values only to the block in the cache, then writes the modified block back to the lower level of the memory hierarchy when the modified block in the cache is replaced.
## Virtual Memory
### Definition
A technique that uses main memory as a "cache" for secondary storage.
### Page Table
The table containing the virtual to physical address translations in a virtual memory system. The table, which is stored in memory, is typically indexed by the virtual page number; each entry in the table contains the physical page number for that virtual page if the page is currently in memory.