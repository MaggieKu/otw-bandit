bandit12@bandit:/tmp/work$ file hex
hex: cannot open `hex' (No such file or directory)
bandit12@bandit:/tmp/work$ xxd -r data.txt >>> hex
-bash: syntax error near unexpected token `>'
bandit12@bandit:/tmp/work$ xxd -r data.txt hex
bandit12@bandit:/tmp/work$ ls
data.txt  hex
bandit12@bandit:/tmp/work$ cat hex
@4Aڀh4C@hd2@hF4XdBGaB~6VAGf͌>G`wBx)B׭xk|IFDs>R4"^d!P^g!)O^1IF       7kFx,2=l [ĵF7YxXHF;ň<AVPIdJ-Se'yu3_1��Ft#^haX"l=]fwDZo,AB
4@weRI7}8v9H;uH%}$iKL12v)|Rib AN]BA>Y|.Ebandit12@bandit:/tmp/work$ file hex
hex: gzip compressed data, was "data2.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 581
bandit12@bandit:/tmp/work$ gzip -d hex
gzip: hex: unknown suffix -- ignored
bandit12@bandit:/tmp/work$ strings hex | gzip -d >>> out
-bash: syntax error near unexpected token `>'
bandit12@bandit:/tmp/work$ strings hex | gzip -d

gzip: stdin: not in gzip format
bandit12@bandit:/tmp/work$ mv hex data2.bin
bandit12@bandit:/tmp/work$ file data2.bin
data2.bin: gzip compressed data, was "data2.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 581
bandit12@bandit:/tmp/work$ gzip -d data2.bin
gzip: data2.bin: unknown suffix -- ignored
bandit12@bandit:/tmp/work$ mv data2.bin tmp.gz
bandit12@bandit:/tmp/work$ ls
data.txt  tmp.gz
bandit12@bandit:/tmp/work$ gzip -d tmp.gz
bandit12@bandit:/tmp/work$ ls
data.txt  tmp
bandit12@bandit:/tmp/work$ cat tmp
@4Aڀh4C@hd2@hF4XdBGaB~6VAGf͌>G`wBx)B׭xk|IFDs>R4"^d!P^g!)O^1IF       7kFx,2=l [ĵF7YxXHF;ň<AVPIdJ-Se'yu3_1��Ft#^haX"l=]fwDZo,AB
4@weRI7}8v9H;uH%}$iKL12v)|Rib AN]BA>Y|bandit12@bandit:/tmp/work$ file tmp
tmp: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/work$ mv tmp tmp.bz2
bandit12@bandit:/tmp/work$ bzip2 -d tmp.gz
bzip2: Can't open input file tmp.gz: No such file or directory.
bandit12@bandit:/tmp/work$ bzip2 -d tmp.bz2
bandit12@bandit:/tmp/work$ ls
data.txt  tmp
bandit12@bandit:/tmp/work$ cat temp
cat: temp: No such file or directory
bandit12@bandit:/tmp/work$ cat tmp
'sEddata4.binOHqs2|1y8ŞMJ$ؐbdDBNÃ5)]v([:&_7[b(oeKjƬ꺦jUVT      EU5-dE{wMDEn!e>ҷ_]z|eG=5l%kBH"f=`.,9£O1g&?T|9R37گexvy˱Rg7MDPbandit12@bandit:/tmp/work$ ls}
data.txt  tmp
bandit12@bandit:/tmp/work$ file tmp
tmp: gzip compressed data, was "data4.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/work$ mv tmp tmp.gz
bandit12@bandit:/tmp/work$ gzip -d tmp.gz
bandit12@bandit:/tmp/work$ ls
data.txt  tmp
bandit12@bandit:/tmp/work$ cat tmp
data5.bin0000644000000000000000000002400014421271447011246 0ustar  rootrootdata6.bin0000644000000000000000000000033414421271447011253 0ustar  rootrootBZh91AY&SYI
Jl@@4i2FAjbb1&FbO~ @f8AВ @{t"1<VfCYpwlKX,(fXM;U^hщr>q@)yǧ,!*\'vU}l?W\[  ܑNDBbandit12@bandit:/tmp/work file tmp
tmp: POSIX tar archive (GNU)
bandit12@bandit:/tmp/work$ mv tmp tmp.tar
bandit12@bandit:/tmp/work$ tar -xvf tmp.tar
data5.bin
bandit12@bandit:/tmp/work$ ls
data5.bin  data.txt  tmp.tar
bandit12@bandit:/tmp/work$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/work$ tar -xvf data5.bin
data6.bin
bandit12@bandit:/tmp/work$ ls
data5.bin  data6.bin  data.txt  tmp.tar
bandit12@bandit:/tmp/work$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/work$ bzip2 -d data6.bin
bzip2: Can't guess original name for data6.bin -- using data6.bin.out
bandit12@bandit:/tmp/work$ ls
data5.bin  data6.bin.out  data.txt  tmp.tar
bandit12@bandit:/tmp/work$ file data6.bin.out
data6.bin.out: POSIX tar archive (GNU)
bandit12@bandit:/tmp/work$ tar -xvf data5.bin.out
tar: data5.bin.out: Cannot open: No such file or directory
tar: Error is not recoverable: exiting now
bandit12@bandit:/tmp/work$ ls
data5.bin  data6.bin.out  data.txt  tmp.tar
bandit12@bandit:/tmp/work$ file data6.bin.out
data6.bin.out: POSIX tar archive (GNU)
bandit12@bandit:/tmp/work$ mv data6.bin.out data6.tar
bandit12@bandit:/tmp/work$ tar -xvf data6.tar
data8.bin
bandit12@bandit:/tmp/work$ ls
data5.bin  data6.tar  data8.bin  data.txt  tmp.tar
bandit12@bandit:/tmp/work$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/work$ mv data8.bin data9.gz
bandit12@bandit:/tmp/work$ gzip -d data9.gz data10
gzip: data10.gz: No such file or directory
bandit12@bandit:/tmp/work$ gzip -d data9.gz >>> data10
-bash: syntax error near unexpected token `>'
bandit12@bandit:/tmp/work$ gzip -d data9.gz
gzip: data9.gz: No such file or directory
bandit12@bandit:/tmp/work$ gzip -d data9.gz
gzip: data9.gz: No such file or directory
bandit12@bandit:/tmp/work$ ls
data5.bin  data6.tar  data9  data.txt  tmp.tar
bandit12@bandit:/tmp/work$ file data9
data9: ASCII text
bandit12@bandit:/tmp/work$ cat data9
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

Note: not a fan of this