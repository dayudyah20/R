# R

#a Membuat plot deret waktu untuk Jumlah Curah Hujan Kota Pangkalan Bun

CurahHujan <-ts(CurahHujan,start=c(2015,1),frequency=12)
CurahHujan

plot.ts(CurahHujan.ts,type="l",col='blue4',col.main="red",xlab="Tahun",ylab="Curah Hujan(mm)",main=" Jumlah Curah Hujan Kota Pangkalan Bun")

#b Membuat plot deret waktu dengan menambahkan label nama bulan untuk Jumlah Curah Hujan di Kota Pangkalan Bun
library(TSA)
CurahHujan.ts <-ts(CurahHujan,start=c(2015,1),frequency=12)

CurahHujan.ts

plot.ts(CurahHujan.ts,type="l",col='blue3',col.main="red",xlab="Tahun",ylab="Curah Hujan(mm)",main="Jumlah Curah Hujan Kota Pangkalan Bun")
points(y=CurahHujan.ts,x=time(CurahHujan.ts),pch=as.vector(season(CurahHujan.ts)))
