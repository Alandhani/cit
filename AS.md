# cit# pengkodean = utf-6
impor  os

dari  inti  impor  HackingTool
dari  core  import  HackingToolsCollection


kelas  TheFatRat ( HackingTool ):
    JUDUL  =  "Si FatRat"
    DESKRIPSI  =  "TheFatRat Menyediakan Cara Mudah Membuat Backdoor dan \n " \
                  "Payload yang dapat mem-bypass sebagian besar anti-virus"
    INSTALL_COMMANDS  = [
        "sudo git clone https://github.com/Screetsec/TheFatRat.git" ,
        "cd TheFatRat && sudo chmod +x setup.sh"
    ]
    RUN_COMMANDS  = [ "cd TheFatRat && sudo bash setup.sh" ]
    PROJECT_URL  =  "https://github.com/Screetsec/TheFatRat"

    def  __init__ ( mandiri ):
        super ( TheFatRat , mandiri ). __init__ ([
            ( ' Update' , self .update ),
            ( 'Troubleshoot' , self . troubleshoot )
        ])

     pembaruan def ( mandiri ):
        os . sistem (
            "cd TheFatRat && pembaruan bash && chmod +x setup.sh && bash setup.sh" )

    def  memecahkan masalah ( self ):
        os . sistem ( "cd TheFatRat && sudo chmod +x chk_tools && ./chk_tools" )


kelas  Brutal ( HackingTool ):
    JUDUL  =  "Brutal"
    DESKRIPSI  =  "Brutal adalah toolkit untuk membuat berbagai payload dengan cepat," \
                  "serangan powershell, \n serangan virus dan luncurkan pendengar untuk " \
                  "Perangkat Antarmuka Manusia"
    INSTALL_COMMANDS  = [
        "sudo git clone https://github.com/Screetsec/Brutal.git" ,
        "cd Brutal && sudo chmod +x Brutal.sh"
    ]
    RUN_COMMANDS  = [ "cd Brutal && sudo bash Brutal.sh" ]
    PROJECT_URL  =  "https://github.com/Screetsec/Brutal"

    def  show_info ( self ):
        super ( Brutal , diri sendiri ). tampilkan_info ()
        cetak ( """
        [!] Persyaratan
            >> Software Arduino (saya menggunakan v1.6.7)
            >> TeensyDuino
            >> Aturan udev Linux
            >> Salin dan tempel folder PaensyLib di dalam perpustakaan \ Arduino Anda
    
        [!] Silakan Kunjungi tautan di bawah ini untuk Instalasi Arduino
            >> https://github.com/Screetsec/Brutal/wiki/Install-Requirements
        """ )


kelas  Jahitan ( HackingTool ):
    JUDUL  =  "Menjahit"
    DESKRIPSI  =  "Stitch adalah Alat Administrator Jarak Jauh Python Lintas Platform \n \t " \
                  "[!] Rujuk Tautan Di Bawah Untuk Menang & MAc Os"
    INSTALL_COMMANDS  = [
        "sudo git clone https://github.com/nathanlopez/Stitch.git" ,
        "cd Stitch && sudo pip install -r lnx_requirements.txt"
    ]
    RUN_COMMANDS  = [ "cd Stitch && sudo python main.py" ]
    PROJECT_URL  =  "https://nathanlopez.github.io/Stitch"


kelas  MSFVenom ( HackingTool ):
    JUDUL  =  "Pembuat Muatan MSFvenom"
    DESKRIPSI  =  "MSFvenom Payload Creator (MSFPC) adalah pembungkus untuk menghasilkan \n " \
                  "beberapa jenis muatan, berdasarkan pilihan pengguna. \n " \
                  "Idenya adalah sesederhana mungkin (hanya membutuhkan " \
                  "satu masukan) \n untuk menghasilkan muatannya."
    INSTALL_COMMANDS  = [
        "sudo git clone https://github.com/g0tmi1k/msfpc.git" ,
        "cd msfpc;sudo chmod +x msfpc.sh"
    ]
    RUN_COMMANDS  = [ "cd msfpc; sudo bash msfpc.sh -h -v" ]
    PROYEK_URL  =  "https://github.com/g0tmi1k/msfpc"


kelas  Venom ( HackingTool ):
    JUDUL  =  "Generator Shellcode Venom"
    DESKRIPSI  =  "venom 1.0.11 (malicious_server) dibangun untuk mengambil" \
                  "keuntungan \n server web apache2 untuk mengirimkan muatan " \
                  "(LAN) menggunakan halaman web palsu yang ditulis dalam html"
    INSTALL_COMMANDS  = [
        "sudo git clone https://github.com/r00t-3xp10it/venom.git" ,
        "sudo chmod -R 775 venom*/ && cd venom*/ && cd aux && sudo bash setup.sh" ,
        "sudo ./venom.sh -u"
    ]
    RUN_COMMANDS  = [ "cd racun && sudo ./venom.sh" ]
    PROJECT_URL  =  "https://github.com/r00t-3xp10it/venom"


kelas  Spycam ( HackingTool ):
    JUDUL  =  "Kamera pengintai"
    DESKRIPSI  =  "Script untuk menghasilkan payload Win32 yang mengambil webcam" \
                  "gambar setiap 1 menit dan kirim ke penyerang"
    INSTALL_COMMANDS  = [
        "sudo git clone https://github.com/indexnotfound404/spycam.git" ,
        "cd spycam && bash install.sh && chmod +x spycam"
    ]
    RUN_COMMANDS  = [ "cd spycam && ./spycam" ]
    PROJECT_URL  =  "https://github.com/indexnotfound404/spycam"


kelas  MobDroid ( HackingTool ):
    JUDUL  =  "Mob-Droid"
    DESKRIPSI  =  "Mob-Droid membantu Anda menghasilkan payload metasploit di " \
                  "cara mudah \n tanpa mengetik perintah yang panjang dan menghemat waktu Anda"
    INSTALL_COMMANDS  = [
        "git clone https://github.com/kinghacker0/mob-droid.git" ]
    RUN_COMMANDS  = [ "cd mob-droid;sudo python mob-droid.py" ]
    PROJECT_URL  =  "https://github.com/kinghacker0/Mob-Droid"


kelas  Enigma ( HackingTool ):
    JUDUL  =  "Enigma"
    DESKRIPSI  =  "Enigma adalah dropper muatan Multiplatform"
    INSTALL_COMMANDS  = [
        "sudo git clone https://github.com/UndeadSec/Enigma.git" ]
    RUN_COMMANDS  = [ "cd Enigma;sudo python enigma.py" ]
    PROYEK_URL  =  "https://github.com/UndeadSec/Enigma"


kelas  PayloadCreatorTools ( HackingToolsCollection ):
    TITLE  =  "Alat pembuat muatan"
    ALAT  = [
        FatRat (),
        Brutal (),
        Jahitan (),
        MSFVenom (),
        Racun (),
        Kamera pengintai (),
        MobDroid (),
        Teka-teki ()
    ]
