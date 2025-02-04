# NumPy

import numpy as np
import pandas as pd

data = np.array([[5, 12, 18, 23, 45],
                 [7, 14, 22, 31, 50],
                 [10, 15, 25, 35, 55],
                 [13, 20, 30, 40, 60]])

print("Dizinin Boyutu:", data.shape)
print("Dizinin Veri Türü:", data.dtype)

column_means = np.mean(data, axis=0)
print("Her bir sütunun ortalamaları:", column_means)

row_max = np.max(data, axis=1)
print("Her bir satırdaki maksimum değerler:", row_max)

import kagglehub

# Download latest version
path = kagglehub.dataset_download("handanvural/verinumpy")

print("Path to dataset files:", path)

np.savetxt("veri.csv", data, delimiter=",", fmt="%d")

loaded_data = np.loadtxt("veri.csv", delimiter=",")
print("CSV'den okunan veri:\n", loaded_data)
