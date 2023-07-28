# plotly_blast_tool

A specialised version of the generalised (plotly_tabular_tool)[https://github.com/fubar2/plotly_tabular_tool], but designed
for 25 column Galaxy blastn search outputs.
It uses the same code, but adds a default header and auto-transformation of the evalue column -log10(x) to make them more like the bitscore

Demonstration and some explanation at https://lazarus.name/demo/

Plotly.express makes a lot of clever design decisions.
Unfortunately, it gets totally confused with evalue columns because it thinks scientific notation like 5.00e-204 is a string or something.
Strange and probably uninformative axes and plots will probably result if you try to use data like the very small values in a blastn search result evalue column without transformation.
Note that all columns used for colour (legend) and the x/y axis tickmarks are truncated because they can squish up the plot.
*..* is added at the end to show truncation.


