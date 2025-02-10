# Kodluyoruz-Homework-
Minimum Öklid Mesafesinin Hesaplanması
import math

# Öklid mesafesini hesaplayan fonksiyon
def euclideanDistance(point1, point2):
    return math.sqrt((point2[0] - point1[0]) ** 2 + (point2[1] - point1[1]) ** 2)

# 2D uzaydaki noktalar
points = [(1, 2), (4, 6), (7, 8), (2, 1), (5, 3)]

# Mesafeleri saklayacak liste
distances = []

# Tüm nokta çiftleri arasındaki mesafeleri hesaplayıp distances listesine ekleme
for i in range(len(points)):
    for j in range(i + 1, len(points)):  # Her çifti sadece bir kez ele almak için
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)

# Minimum mesafeyi bulma ve yazdırma
if distances:
    min_distance = min(distances)
    print("Minimum Öklid mesafesi:", min_distance)
else:
    print("Yeterli nokta yok.")
