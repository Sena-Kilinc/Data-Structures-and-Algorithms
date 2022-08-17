# Merge Sort

## [16,21,11,8,12,22]

## 1. Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.

**_*Diziyi ortadan ikiye bölüyoruz. Bölünen dizileri tekrar bölüyoruz. Tek eleman kalana kadar bu işleme devam ediyoruz*_**.

```
|     |     |     |     |     |     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|     |     |     | 16  | 21  | 11  | 8   | 12  | 22  |     |     |     |
|     |     |     |     |     |     |     |     |     |     |     |     |
|     |     | 16  | 21  | 11  |     |     | 8   | 12  | 22  |     |     |
|     |     |     |     |     |     |     |     |     |     |     |     |
|     | 16  |     |     | 21  | 11  |     | 8   |     | 12  | 22  |     |
|     |     |     |     |     |     |     |     |     |     |     |     |
| 16  |     | 21  |     | 11  |     |     | 8   |     | 12  |     | 22  |
```

**_Ardından birleştirme ve sıralama yapıyoruz._**

```
|     |     |     |     |     |     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 16  |     | 21  |     | 11  |     |     | 8   |     | 12  |     | 22  |
|     |     |     |     |     |     |     |     |     |     |     |     |
|     | 16  |   |     | 11  |  21   |     | 8   |     | 12  | 22  |     |
|     |     |     |     |     |     |     |     |     |     |     |     |
|     |     | 11  | 16  | 21  |     |     | 8   | 12  | 22  |     |     |
|     |     |     |     |     |     |     |     |     |     |     |     |
|     |     |     | 8   | 11  | 12  | 16  | 21  | 22  |     |     |     |
```

## 2. Big-O gösterimini yazınız.

**Merge sort metodunda dizi ikiye bölünerek işlemler yapılır ve bu her satır başına n kez gerçekleştiği için 2^x = n olarak düşünürsek Big-O gösterimi O(nlogn) olacaktır.**
