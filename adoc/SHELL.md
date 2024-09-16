```bash
cd AFCS\ Book; [ ! -d ../build ] && mkdir ../build
```

```bash
[ ! -d ../build ] && mkdir ../build ; asciidoctor-pdf \
-r asciidoctor-bibtex \
-r asciidoctor-diagram \
--theme prepress.yml \
-a commitnumber=`git describe --tags --long --dirty` \
-a source-highlighter=rouge \
--destination-dir=../build \
AFCS\ Book.adoc
```

```bash
[ ! -d build ] && mkdir build ; \
asciidoctor-pdf \
-r asciidoctor-bibtex \
-r asciidoctor-diagram \
--theme Blog/prepress.yml \
-a commitnumber=`git describe --tags --long --dirty` \
-a source-highlighter=rouge \
--destination-dir=build \
Blog/QRPHPart2.adoc
```

```bash
[ ! -d build ] && mkdir build ; \
asciidoctor \
-r asciidoctor-bibtex \
-r asciidoctor-diagram \
-a commitnumber=`git describe --tags --long --dirty` \
-a source-highlighter=rouge \
--destination-dir=build \
QRPHPart1.adoc
```

````bash
asciidoctor -r asciidoctor-bibtex -r asciidoctor-diagram -a commitnumber=`git describe --tags --long --dirty` -a source-highlighter=rouge --destination-dir=../_posts/includes -e QRPHPart2.adoc```


````
