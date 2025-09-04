# kircherlab.github.io

Kircher Lab Website: Computational Genome Biology at BIH and Regulatory Genomics group at UKSH

## Creating HTML files from "templates"

- Pretty much all pages were using the same header, banner and footer and it was difficult to keep them consistant
- Therefore, the actual page content was separated from these files in the templates folder
- Please edit files in templates and then create the html files

```
cat templates/header_404.tmp templates/banner.tmp templates/404.tmp templates/footer.tmp > 404.html

for i in impressum contact people research projects publications; do cat templates/header.tmp templates/banner.tmp templates/${i}.tmp templates/footer.tmp > ${i}.html; done

for i in templates/people/*.tmp; do 
    name=$(basename $i .tmp);
    cat templates/header.tmp templates/banner.tmp ${i} templates/footer.tmp > people/${name}.html; 
done

for i in templates/projects/*.tmp; do 
    name = $(basename $i .tmp);
    cat templates/header.tmp templates/banner.tmp ${i} templates/footer.tmp > projects/${name}.html; 
done

```
