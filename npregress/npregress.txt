# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Local polynomials smoothing Use npregress With (In) R Software
install.packages("npregress")
library("npregress")
npregress = read.csv("https://raw.githubusercontent.com/timbulwidodostp/npregress/main/npregress/npregress.csv",sep = ";")
# Estimation Local polynomials smoothing Use npregress With (In) R Software
time <-npregress$time
accel <-npregress$accel
npregress <- npregress(time,accel,bandwidth=0.02)
summary(npregress)
ord <- order(time)
plot(time,accel)
lines(time[ord],predict(npregress)[ord])
# Local polynomials smoothing Use npregress With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished