```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Daftar Barang</title>
  <link href="../../bootstrap-5.3.3-dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <style>
        .list-group-item.active {
          background-color: rgb(32, 32, 173);
          padding-left: 30px;
          background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="black" width="18px" height="18px"><path d="M0 0h24v24H0z" fill="none"/><path d="M9 16.2l-3.5-3.5c-.39-.39-.39-1.02 0-1.41s1.02-.39 1.41 0l2.09 2.09 5.59-5.59c.39-.39 1.02-.39 1.41 0s.39 1.02 0 1.41L10.41 16.6c-.39.39-1.02.39-1.41 0z"/></svg>');
          background-repeat: no-repeat;
          background-position: center left 5px;
        }
      </style>
   <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
        <a class="navbar-brand" href="#">Ada Kah</a>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="nav nav-pills">
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#">Home</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="#">About</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="#">Services</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="#">Contact</a>
                </li>
              </ul>
        </div>
        <button class="btn btn-primary mx-2"><a href="soal2.html" class="text-white">
          Sign Up</button>
        </a>
        <button class="btn btn-outline-primary">Sign In</button>
    </div>
</nav>
                      </div>
                    </span>
                  <div class="container">
                    </div>
                  </div>
                </div>
                </div>
        </div>
      </nav>
      
  <div class="container">
    <h1 class="text-center mt-5">Ada Ji Mau di Give Apa</h1>
    <div class="row mt-3">
      
      <div class="col-md-6">
        <select id="categoryFilter" class="form-select mb-2">
          <option value="elektronik">elektronik</option>
          <option value="fashion">Fashion</option>
          <option value="alat_rumah_tangga">alat_rumah_tangga</option>
          <option value="">Semua Kategori</option>

        </select>
      </div>
    </div>
    <table>
        <tr>
          <td>
            <ul class="list-group mt-3">
              <li class="item list-group-item" data-category="elektronik">Laptop</li>
              <li class="item list-group-item" data-category="elektronik">Smartphone</li>
              <li class="item list-group-item" data-category="fashion">Sepatu</li>
              <li class="item list-group-item" data-category="fashion">Baju</li>
              <li class="item list-group-item" data-category="alat_rumah_tangga">Panci</li>
              <li class="item list-group-item" data-category="alat_rumah_tangga">Piring</li>
            </ul>
          </td>
          </td>
          <td>
            <ul class="list-group mt-3">
                <li class="item list-group-item" data-category="elektronik">laptop</li>
                <li class="item list-group-item" data-category="elektronik">Smartphone</li>
                <li class="item list-group-item" data-category="fashion">Sepatu</li>
                <li class="item list-group-item" data-category="fashion">Baju</li>
                <li class="item list-group-item" data-category="alat_rumah_tangga">Panci</li>
                <li class="item list-group-item" data-category="alat_rumah_tangga">Piring</li>
              </ul>
          </td>
          </td>
          <td>
            <ul class="list-group mt-3">
              <li class="item list-group-item" data-category="elektronik">laptop</li>
              <li class="item list-group-item" data-category="elektronik">Smartphone</li>
              <li class="item list-group-item" data-category="fashion">Sepatu</li>
              <li class="item list-group-item" data-category="fashion">Baju</li>
              <li class="item list-group-item" data-category="alat_rumah_tangga">Panci</li>
              <li class="item list-group-item" data-category="alat_rumah_tangga">Piring</li>
            </ul>
          </td>
          </td>
          <td>
            <ul class="list-group mt-3">
              <li class="item list-group-item" data-category="elektronik">Laptop</li>
              <li class="item list-group-item" data-category="elektronik">Smartphone</li>
              <li class="item list-group-item" data-category="fashion">Sepatu</li>
              <li class="item list-group-item" data-category="fashion">Baju</li>
              <li class="item list-group-item" data-category="alat_rumah_tangga">Panci</li>
              <li class="item list-group-item" data-category="alat_rumah_tangga">Piring</li>
            </ul>
          </td>
        </tr>
      </table>
      
  </div>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
<script>
    $(document).ready(function(){
      $('.list-group-item').click(function(){
        $(this).toggleClass('active'); // Toggle class 'active' on the clicked item
      });
    });
    document.querySelectorAll('.item').forEach(item => {
        item.addEventListener('click', () => {
            const category = item.getAttribute('data-category');
            document.querySelectorAll('.item').forEach(otherItem => {
                if (otherItem !== item && otherItem.getAttribute('data-category') !== category) {
                    otherItem.classList.add('disabled');
                } else {
                    otherItem.classList.remove('disabled');
                }
            });
        });
    });
    const maxSelection = 1; // Maximum number of items that can be selected
    let selectedItems = 0;

    document.querySelectorAll('.item').forEach(item => {
        item.addEventListener('click', () => {
            if (item.classList.contains('disabled')) return; // Check if item is disabled

            if (item.classList.contains('active')) {
                item.classList.remove('active');
                selectedItems--;
            } else {
                if (selectedItems < maxSelection) {
                    item.classList.add('active');
                    selectedItems++;
                }
            }

            // Disable other items if maximum selection is reached
            document.querySelectorAll('.item').forEach(otherItem => {
                if (otherItem !== item && !otherItem.classList.contains('active')) {
                    if (selectedItems >= maxSelection) {
                        otherItem.classList.add('disabled');
                    } else {
                        otherItem.classList.remove('disabled');
                    }
                }
            });
        });
    });
    document.getElementById('nextButton').addEventListener('click', () => {
        // Remove 'active' class from all items
        document.querySelectorAll('.item').forEach(item => {
            item.classList.remove('active');
        });
        selectedItems = 0;

        // Enable all items
        document.querySelectorAll('.item').forEach(item => {
            item.classList.remove('disabled');
        });
    });
  </script>
</body>
</html>
```

1. **Container**: Mengatur lebar konten di dalamnya.
2. **Text Center**: Untuk membuat teks menjadi tengah.
3. **Margin Top**: Memberi jarak atas.
4. **Column**: Membuat layout kolom pada grid.
5. **Button**: Membuat tombol.
6. **Navbar**: Membuat navigasi bar.
7. **Nav Item**: Item dalam navigasi.
8. **Active**: Memberi penanda bahwa item ini aktif.
9. **List Group**: Membuat grup daftar.
10. **List Group Item**: Item dalam grup daftar.
11. **Form Select**: Membuat dropdown form.
12. **Background Color**: Memberi warna latar belakang.
13. **Padding Left**: Memberi padding sebelah kiri.
14. **Background Image**: Menambahkan gambar latar belakang.
15. **Background Repeat**: Mengatur ulang gambar latar belakang.
16. **Background Position**: Mengatur posisi gambar latar belakang.