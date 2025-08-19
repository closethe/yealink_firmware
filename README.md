## version 


 arm程序，用于安装yealink固件。
 
 可以用于逆向固件加密算法(cypher1-cypher4、aes_an、aes_li)、密钥，或进行相关研究。
 打印固件信息。
## 程序执行 help信息
```
t1-armbian:yealink:# ./version.bin
	no rom block file setting!
	romtool 2.0.6.2 [none]
	[Oct 27 2021 19:29:04]
		  --help            display this help and exit
		  --version         output version information and exit
	-e    --execute         execute action on the rom or block
	-i    --all-info        show all info of the rom or block
	-I    --info            show info of the rom or block
	-f    --flags           flags for rom or block,for example :[force|tool|checksum|crc]
	-t    --type            type for rom or block,for example :[none|bin|tool|file|nand-raw|nand-oob|nor]
	-p    --cypher-type     cypher type    for rom or block,for example :[none|cypher1|cypher2]
	-F    --fifo            romtool support data from fifo
	-d    --data-type       source data type for rom or block,for example :[raw|file]
	-o    --option          option block to take action
	-a    --align           align option,[block-align|page-align|pad=0x??],pad data default as 0xFF
	-t    --retry           flash  write retry,default as 3
	-v    --verify          verify write retry,default as yes
	-V    --verbose         verbosely list files processed
	-s    --skipbad         skip that block can NOT found in rom
	-r    --reboot          do reboot after processed,and handle watchdog while processing
	-h    --background      run in background
	-k    --kill            kill all process
	-q    --standalone      installing rom as standalone,handle 'kill','reboot',etc
	-c    --current path    setup the current or output path
```
## 示例1：
```
t1-armbian:yealink:# ./version.bin -i T53W_96.86.0.164.rom
============ROM<T53W_96.86.0.164.rom>=============
rom magic       :0xad24ec0b
rom hsize       :128
rom hcrc        :0x133653b3
rom format      :0x00000002
rom flags       :0x0000002a
rom lenght      :45310208
rom verify      :0xffffffff
rom blocks      :3
rom dev vid     :0
rom dev pid     :96
rom dev name    :T54W
rom oem name    :NULL
rom version     :96.86.0.164
rom hw id       :2
rom sw id       :1
rom hw  cid     :0=97
rom hw  cid     :1=95
rom hw  cid     :2=142
============block 0================
blk offset      :128
blk header      :128
blk magic       :0xeb9f56c9
blk hsize       :128
blk good hcrc   :0xbabe346a
blk flags       :0x00000100
blk lenght      :641872
blk total       :642000
blk none verify :0xe9c2a0da
blk type        :2
blk id          :0
blk name        :version
blk version     :96.0.0.7
blk cypher      :none
blk data        :raw
============block 1================
blk offset      :642128
blk header      :128
blk magic       :0xeb9f56c9
blk hsize       :128
blk good hcrc   :0x3d4144a7
blk flags       :0x00000100
blk lenght      :44274736
blk total       :44274864
blk none verify :0xb99e9d67
blk type        :4
blk id          :8
blk name        :rfs
blk version     :96.86.0.164
blk cypher      :cypher1
blk data        :raw
============block 2================
blk offset      :44916992
blk header      :128
blk magic       :0xeb9f56c9
blk hsize       :128
blk good hcrc   :0xe2918464
blk flags       :0x00000100
blk lenght      :393216
blk total       :393344
blk none verify :0x3d2e4ff5
blk type        :4
blk id          :1
blk name        :bootloader
blk version     :96.0.1.8
blk cypher      :cypher3
blk data        :raw
```
