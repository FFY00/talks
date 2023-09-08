SRCFILES := $(wildcard *.mmd)
SVGFILES := $(SRCFILES:.mmd=.svg)
PNGFILES := $(SRCFILES:.mmd=.png)

.PHONY: all clean

all: $(SVGFILES) $(PNGFILES)

clean:
	rm -f $(SVGFILES)

%.svg: %.mmd
	mmdc -c config.json -i $< -o $@

%.png: %.mmd
	mmdc -c config.json -i $< -o $@
