### denoise-kit: Denoise amplicon sequencing data with USEARCH unoise


### 1. install

```sh
git clone https://github.com/jameslz/denoise-kit
wget https://drive5.com/downloads/usearch11.0.667_i86linux32.gz
gunzip usearch11.0.667_i86linux32.gz
mv usearch11.0.667_i86linux32 usearch
chmod -R 775 usearch
mv  usearch denoise-kit/binaries
```

### 2. usage

```sh
export PATH=$PWD/denoise-kit:$PATH
cp $PWD/denoise-kit/example/*  ./
```

: modifiy template files: metdata.txt and mapping_file.txt

For raw reads file format, support:

```text
ZB1_1.fastq.gz	ZB1_2.fastq.gz
ZB1_1.fastq	ZB1_2.fastq
```

run pipeline:

```sh
denoise-kit metdata.txt pipeline
```
