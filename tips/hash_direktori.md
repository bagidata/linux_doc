`$ find '/media/user/lokasi/direktori' -type f | md5sum`

Hasil :

`ac42e97226540a1266bad66ea878274c  -`

Spesifik file :

`find '/media/user/lokasi/direktori' -name "*.php" -exec md5sum {} \; > result.txt`
