#R in Create

data <- read.csv("~/R_Work(2017)/data/XXX.csv",header = 1)
spec <- spec.ar(data$heart_rate, plot = FALSE)

lf_data <- 0
hf_data <- 0

spec_lf <- spec$spec[50:150]    #0.05Hz to 0.15Hz ... LF 
spec_hf <- spec$spec[150:350]   #0.15Hz to 0.35Hz ...HF

spec_lf <- spec_lf * spec_lf
spec_hf <- spec_hf * spec_hf

lf_data <- sum(spec_lf)  #sum spectrum
hf_data <- sum(spec_hf)  #sum spectrum

lh <- lf_data / hf_data

rm(hf_data,lf_data,spec_hf,spec_lf,spec,data)

lh


