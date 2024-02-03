# Linux-assignment-4
1.
root@shubham-Latitude-7480:~# mkdir MyFile
root@shubham-Latitude-7480:~# ls
dir1  MyFile  snap
2.
root@shubham-Latitude-7480:~# touch document.txt
root@shubham-Latitude-7480:~# ls
dir1  document.txt  MyFile  snap
root@shubham-Latitude-7480:~# cp document.txt MyFile
root@shubham-Latitude-7480:~# cd MyFile
root@shubham-Latitude-7480:~/MyFile# ls
documents  document.txt
root@shubham-Latitude-7480:~/MyFile# cp document.txt documents
root@shubham-Latitude-7480:~/MyFile# cd documents
root@shubham-Latitude-7480:~/MyFile/documents# ls
document.txt
root@shubham-Latitude-7480:~/MyFile/documents# 
3.
root@shubham-Latitude-7480:~/MyFile# touch notes.txt
root@shubham-Latitude-7480:~/MyFile# ls
document  documents  document.txt  notes.txt
root@shubham-Latitude-7480:~/MyFile# rm notes.txt
root@shubham-Latitude-7480:~/MyFile# ls
document  documents  document.txt

