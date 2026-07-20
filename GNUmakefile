%.pdf: %.tex
	context $(<)

%.png: %.pdf
	magick -density 450 $(<) \
	       -background "#f6f8fa" \
	       -layers flatten \
	       -bordercolor "#f6f8fa" -border 15x15 \
	       $(@)

.PHONY: default clean veryclean
default:: master_field_equation.png
clean::
	-rm -f master_field_equation.{pdf,tuc,log}
veryclean::
	-rm -f master_field_equation.png
