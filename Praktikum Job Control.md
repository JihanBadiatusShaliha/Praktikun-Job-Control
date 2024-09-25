# Praktikum Job Control
<h2>Nama			: Jihan Badiatus Shaliha <br/>
NIM	          : 09011282328098<br/>
Kelas			    : SK3B<br/>
Mata Kuliah		: Sistem Operasi<br/>
Dosen Pengampu: Adi Hermansyah, M.T.</h2>


<h3>Tugas Praktikum Job Control</h3>
1. Eksekusi seluruh profile yang ada : <br/> 
a.  Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :  <br/>
echo “Profile dari /etc/profile”  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/b2744d44-32c5-4391-bcc2-3270aa8dc031 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/6d4854d1-9943-45c5-ad31-df645bcaf7ec width=500 /> <br/>

b.  Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :  <br/>
/home/stD02001/.bash_profile  <br/>
/home/. stD02001/.bash_login  <br/>
/home/mahasiswa/.profile  <br/>
/home/mahasiswa/.bashrc  <br/>
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : <br/>
echo “Profile dari .bash_profile”  <br/>
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/45ef9e3e-5096-4573-9ea0-e0caf58ccd16 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/beded7c6-9cc4-4f5d-a007-5888cb244492 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/11654e84-bb89-4de5-a5b1-01f0c92f9e7c width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/f2a8cade-aa5c-4bef-a426-864f2b76aa76 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/f4c27584-0439-4b0f-8a81-ff4409d3efeb width=500 /> <br/>


c.  Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:  <br/>
$ su mahasiswa  <br/>
$ exit <br/>
kemudian gunakan opsi - sebagai berikut:<br/>
$ su – mahasiswa<br/>  
$ exit<br/>
Jelaskan perbedaan kedua utikitas tsb.<br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/ef7635c7-ec60-4ff9-89bd-60a9beecb116 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/2c7103aa-d643-4a4d-b4ae-966a2a56e200 width=500 /> <br/>
perbedaan:
su mahasiswa hanya mengganti pengguna tetapi tidak mengganti environment. <br/>
su - mahasiswa mengganti pengguna dan juga mengganti environment ke environment default pengguna baru tersebut. <br/>

2. Prompt String (PS)  <br/>
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan 
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell  <br/>
PS1='> '<br/>
export PS1  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/0a97db70-8255-4499-afd4-aa6aaf9eb332 width=500 /> <br/>

b.  Eksperimen hasil PS1 :<br/>
$ PS1=“\! > ”  <br/>
69 > PS1=“\d > ” <br/>
Mon Sep 23 > PS1=“\t > ”  <br/>
10:10:20 > PS1=“Saya=\u >” <br/>
Saya=mahasiswa > PS1=“\w >”  <br/>
~ > PS1=\h >”<br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/d4d058f4-1956-4c5f-bed3-78824470c17c width=500 /> <br/>

3. Logout  <br/>
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout  <br/>
Echo “Terima kasih atas sesi yang diberikan”  <br/>
Sleep 5  <br/>
clear<br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/cfb3263e-3e34-4d76-a001-c0aa08d507d7 width=500 /> <br/>


4. Bash script  <br/>
a.  Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :  <br/>
p1.sh  <br/>
#! /bin/bash  <br/>
echo “Program p1” <br/> 
ls –l  <br/>
p2.sh  <br/>
#! /bin/bash  
echo “Program p2”  <br/>
who  <br/>
p3.sh  <br/>
#! /bin/bash<br/>  
echo “Program p3”<br/>  
ps x<br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/63dafeef-980c-4963-86ad-6fb37003574c width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/e12d88e8-ca5a-44ad-816e-87fa61c5f150 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/3cd11d9f-d615-4638-8462-d6b3cb1417e8 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/6708a674-4bf5-44b8-a4e9-8fdf980c4f23 width=500 /> <br/>

b.  Jalankan script tersebut sebagai berikut :  <br/>
$  ./p1.sh ; ./p3.sh ; ./p2.sh  <br/>
$  ./p1.sh &  <br/>
$  ./p1.sh $ ./p2.sh & ./p3.sh &<br/>  
$  ( ./p1.sh ; ./p3.sh ) &<br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/c5a65424-a31a-487a-a026-91053a38e89c width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/0de1bebb-71c4-4e95-883e-b7fff7f943f3 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/64e09652-51d1-4c64-b4df-dfe85f4bf68c width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/499e6057-9e6f-4ab8-9742-6401cac73437 width=500 /> <br/>

5. Jobs  <br/>
a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh,  
setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.  <br/>
#!/bin/bash  <br/>
while [ true ]  <br/>
do  <br/>
date >> hasil  <br/>
sleep 10  <br/>
done  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/14476440-65b3-4114-806a-6dec6b59b254 width=500 /> <br/>


b.  Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background 
sebagai berikut :  <br/>
$ jobs  <br/>
$ find / -print > files 2>/dev/null &  <br/>
$ jobs  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/498e75a1-29f5-4283-b7bb-95751f5d7f0f width=500 /> <br/>

c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke 
background <br/> 
$ fg %1  <br/>
$ bg  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/fad43da6-90fa-4b5e-853a-a6a0a8dea4b0 width=500 /> <br/>

d.  Stop program background dengan utilitas kill  <br/>
$ ps x  <br/>
$ kill [Nomor PID] <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/4caef262-9989-42d7-8acc-5537a892817e width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/c7c2dd93-8f7c-4a9f-bf76-1233bd3d4e44 width=500 /> <br/>
<img src = https://github.com/user-attachments/assets/91e106d1-54f9-41be-8b5f-ceb69be64687 width=500 /> <br/>

6. History  <br/>
a. Ganti nilai HISTSIZE dari 1000 menjadi 20  <br/>
$ HISTSIZE=20  <br/>
$ h  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/f67a6670-6149-4bb7-bc18-413e012b6705 width=500 /> <br/>

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir 
dilakukan<br/><br/>  
$ !-5  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/cd5e0460-36ed-4150-bcba-7512916a6c80 width=500 /> <br/>

c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer  <br/>
$ !!  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/2c7a8cda-87be-460b-817e-7a7c005e29d9 width=500 /> <br/>

d.  Ulangi instruksi pada history bufer nomor 150  <br/>
$ !150  <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/4b8e7368-6b54-44bb-9d25-73e8d3542fa8 width=500 /> <br/>

e.  Ulangi instruksi dengan prefix “ls”  <br/>
$ !ls <br/>
jawab: <br/>
<img src = https://github.com/user-attachments/assets/35719c72-16c1-4488-aae4-b907682d22b4 width=500 /> <br/>
