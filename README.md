# Link-para-baixar-dados-para-o-CPT verja abaixo

SOURCES .NOAA .NCEP .CPC .FEWS .Africa .DAILY .ARC2 .monthly .est_prcp
  X 10 26 RANGEEDGES
  Y -19 -3 RANGEEDGES
  
TRIMESTRAL

T (Apr 1983) (Jun 2021) RANGEEDGES
  T 3 boxAverage
  91 mul
  T 12 STEP

FOR ANML
 
SOURCES .NOAA .NCEP .CPC .FEWS .Africa .DAILY .ARC2 .daily .est_prcp
  Y -3 -19 RANGEEDGES
  X 10 26 RANGEEDGES
  T (1 Sep 2019) (31 Nov 2019) RANGEEDGES
  T SUM

MENSAL

  T (Jan 1983) (Jan 2019) RANGEEDGES
  T 1 boxAverage
  31 mul
  T 12 STEP

Obervados (Reanalises)
SOURCES .NOAA .NCEP .CPC .FEWS .Africa .DAILY .ARC2 .daily .est_prcp

T (1 Feb 2020) (29 Feb 2020) RANGEEDGES
Y -19 0.1 -3 GRID
X 10 0.1 25 GRID
T SUM

Anomalias (Reanalises)
 SOURCES .NOAA .NCEP .CPC .CAMS_OPI .v0208 .anomaly .prcp

T (days since 1980-01-01) streamgridunitconvert
T differential_mul
T (Feb 2020) (Feb 2020) RANGEEDGES
Y (19S) (3S) RANGEEDGES
X (10E) (25E) RANGEEDGES

