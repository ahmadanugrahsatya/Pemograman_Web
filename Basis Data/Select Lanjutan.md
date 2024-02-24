# AND 
## Struktur
```mysql
select kolom1,kolom2 from nama_table where kolom1='nilai_kolom1' and kolom2='nilai_kolom2';
```

## Contoh
```mysql
select warna,pemilik from mobil where warna='hitam' and pemilik='ibrahim'
```

## Hasil
![](aset/ss48.png)



# OR
## Struktur
```mysql
select kolom1,kolom2 from nama_table where kolom1='nilai_kolom1' or kolom2='nilai_kolom2';
```

## Contoh
```mysql
select warna,pemilik from mobil where warna='Hitam' or pemilik='Ibrahim';
```

## Hasil
![](aset/ss49.png)

# Between
## Struktur
```mysql
select * from nama_table where nama_kolom between nilai1 and nilai2;
```

## Contoh
```mysql
select * from mobil where harga_rental between 100000 and 150000;
```

## Hasil
![](aset/ss50.png)

# Not Between
## Struktur
```mysql
select * from nama_table where nama_kolom not between nilai1 and nilai2;
```

## Contoh
```mysql
select * from mobil where harga_rental not between 100000 and 150000;
```

## Hasil
![](aset/ss50.png)

# <=
## Struktur
```mysql
select * from nama_table where nama_kolom<=nilai;
```

## Contoh
```mysql
select * from mobil where harga_rental<=50000;
```

# >=
## Struktur
```mysql
select * from nama_table where nama_kolom>=nilai;
```

## Contoh
```mysql
select * from mobil where harga_rental>=50000
```

## Hasil
![](aset/ss52.png)

# <> atau !=
## Struktur1
```mysql
select * from nama_table where nama_kolom<>nilai;
```

## Struktur2
```mysql
select * from nama_table where nama_kolom!=nilai;
```

## Contoh1
```mysql
select * from mobil where harga_rental<>50000; 
```

## Contoh2
```mysql
select * from mobil where harga_rental!=50000; 
```

## Hasil1
![](aset/ss53.png)

## Hasil2
![](aset/ss54.png)

# Tantangan Login
## Struktur
```mysql
select nama_kolom from nama_table where nama_kolom=nilai;
```

## Contoh
```mysql
select pemilik from mobil where no_plat="DD 2560 XY";
```

## Hasil
![](aset/ss55.png)

    

