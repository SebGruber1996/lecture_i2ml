
SLOT1=slides-intro-performance
SLOT2=slides-overfitting
SLOT3=slides-measures
SLOT4=slides-roc-1
SLOT5=slides-roc-2
SLOT6=slides-train-test
SLOT7=slides-resampling


all: $(SLOT1).pdf $(SLOT2).pdf $(SLOT3).pdf $(SLOT4).pdf $(SLOT5).pdf $(SLOT6).pdf $(SLOT7).pdf 

all_sources: sources $(SLOT1).pdf $(SLOT2).pdf $(SLOT3).pdf $(SLOT4).pdf $(SLOT5).pd $(SLOT6).pdf $(SLOT7).pdf 


$(SLOT1).pdf: $(SLOT1).Rnw
	Rscript -e 'knitr::knit2pdf("$(SLOT1).Rnw")'

$(SLOT2).pdf: $(SLOT2).Rnw
	Rscript -e 'knitr::knit2pdf("$(SLOT2).Rnw")'

$(SLOT3).pdf: $(SLOT3).Rnw
	Rscript -e 'knitr::knit2pdf("$(SLOT3).Rnw")'

$(SLOT4).pdf: $(SLOT4).Rnw
	Rscript -e 'knitr::knit2pdf("$(SLOT4).Rnw")'

$(SLOT5).pdf: $(SLOT5).Rnw
	Rscript -e 'knitr::knit2pdf("$(SLOT5).Rnw")'

$(SLOT6).pdf: $(SLOT6).Rnw
	Rscript -e 'knitr::knit2pdf("$(SLOT6).Rnw")'

$(SLOT7).pdf: $(SLOT7).Rnw
	Rscript -e 'knitr::knit2pdf("$(SLOT7).Rnw")'

sources: 
	cd rsrc/; Rscript holdout-biasvar.R  # create holdout-bias-var.png (not used) and holdout-biasvar.RData (used in intro-performance and resampling)
	cd rsrc/; Rscript learning_curve.R  # create learning_curve.RData (used in resampling)


