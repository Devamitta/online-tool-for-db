output_filename_html=001_online_editing_basic.html
output_filename_pdf=001_online_editing_basic.pdf


${output_filename_html}: *.adoc 
	asciidoctor -o ${output_filename_html} -r asciidoctor-diagram 	$^

${output_filename_pdf}: *.adoc 
	asciidoctor-pdf -o ${output_filename_pdf} -r asciidoctor-diagram 	$^

.phony pdf: ${output_filename_pdf}

.phony html: ${output_filename_html}

.phony all: ${output_filename_pdf} ${output_filename_html}



.phony clean:
	rm ${output_filename_html}
	rm ${output_filename_pdf}
	rm uml_figures/*.png
