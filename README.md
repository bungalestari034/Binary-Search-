# Binary-Search-
def binary_search(arr, target): 
    left = 0        #batas kiri
    right = len(arr) -1 #Batas Kanan 
    #Salam batas kiri dan kanan belum bersilang 
    while left <= right:
        #Cari indek tengah 
        mid = (left + right) //2
        if arr[mid] == target : 
            return mid #Ketemu! Kembalikan Indeksnya 
        elif target < arr[mid]: 
            right = mid  - 1
        else: 
            left = mid + 1

    return - 1
data = [ 10, 20, 30, 40, 50]
angka_dicari = 40 

hasil = binary_search(data,angka_dicari)
if hasil  !=-1: 
    print("angka", angka_dicari, "ada di indeks", hasil  )
else: 
    print("angka tidak ditemukan")
