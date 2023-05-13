# udpipe model

Included are scripts for training a model (and, for releases, pretrained
models) for [udpipe1](https://github.com/ufal/udpipe). The model performs
sentence segmentation, tokenization, lemmatization, and part-of-speech tagging.
It does not analyze for morphological features or syntax.

## How to get udpipe

`udpipe` can be installed with `pip` (for python usage) or by cloning and
compiling (for cli usage). We'll outline the latter, assuming a Linux system:

1. Clone the repository:

```
git clone https://github.com/ufal/udpipe $HOME/udpipe
```

2. Enter the repository:

```
cd $HOME/udpipe/src
```

3. Compile!
```
make
```

You can test to see that it works by running:
```
./udpipe --version
```

## How to train

From the `models` directory, run:

```
$HOME/udpipe/src/udpipe --train --tokenizer=dimension=64\;segment_size=200 --parser=none ar_iahlt-ud.udpipe ../*.conllu
```

Training may take some time!

## How to analyze

For raw text (filling in the placeholders):

```
$HOME/udpipe/src/udpipe --tokenize --tag ar_iahlt-ud.udpipe TEXTFILE > CONLLUFILE
```

For presegmented sentences (one sentence per line):
```
$HOME/udpipe/src/udpipe --tokenizer=presegmented --tag ar_iahlt-ud.udpipe SENTENCEFILE > CONLLUFILE
```

