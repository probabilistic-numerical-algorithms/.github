%.pdf: %.tex
	context $(<)

profile/assets/%.png: %.pdf
	magick -density 450 $(<) \
	       -background "#f6f8fa" \
	       -layers flatten \
	       -bordercolor "#f6f8fa" -border 15x15 \
	       $(@)

.PHONY: default clean veryclean
default:: profile/assets/master_field_equation.png
veryclean:: clean
clean::
	-rm -f master_field_equation.{pdf,tuc,log}
veryclean::
	-rm -f profile/assets/master_field_equation.png
