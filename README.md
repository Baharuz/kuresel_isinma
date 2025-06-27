Küresel Ortalama Sıcaklık Tahmini

Bu proje, Global Temperature Dataset verileri kullanılarak doğrusal regresyon modeli ile gelecekteki ortalama sıcaklık tahminini amaçlar. Python, Pandas, scikit-learn ve matplotlib gibi araçlarla yapılmıştır.

Veri Seti:
Veri: https://raw.githubusercontent.com/datasets/global-temp/master/data/monthly.csv

Kolonlar:

    Source: Veri kaynağı

    Year: Yıl ve ay bilgisi (ör. 1850-01)

    Mean: Ortalama sıcaklık farkı (referans döneme göre)

Kullanılan Kütüphaneler:

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error

Uygulanan Adımlar:

    Veri Yükleme ve Ön İşleme

        Tarih bilgisi datetime formatına dönüştürüldü.

        Tarihler sayısal (ordinal) hale getirildi.

    Model Eğitimi

        Veri %80 eğitim, %20 test olarak ayrıldı.

        LinearRegression modeli eğitildi.

    Tahmin Üretimi

        120 aylık (10 yıl) ileriye dönük tahmin üretildi.

        Ayrıca 2030 yılı için özel tahmin fonksiyonu eklendi.

    Görselleştirme

        Gerçek veriler ve tahminler aynı grafikte gösterildi.

        2030 yılına dikey çizgi ile işaret kondu.

Örnek Çıktı:

2030'daki ortalama sıcaklık: 0.2764

Nasıl Çalıştırılır?

    Jupyter Notebook ya da Google Colab üzerinde 
    Kodu doğrudan çalıştırmak için:

        Gerekli kütüphaneleri yükleyin (pip install pandas scikit-learn matplotlib seaborn)

        Yukarıdaki kodu bir .ipynb dosyası olarak açın.
