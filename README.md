# Program C++ List Total Piutang
Shofi Annisa Fitri Swasono

      #include <iostream>
      #include <string>
      #include <iomanip>
      using namespace std;
      int main() 
      {
      int jum_orang, bayar, bunga, jumlah[50];
      string nama_penghutang[50];
      float tot;

      cout<<"List Hutang"<<endl;
      cout<<"--------------------------"<<endl;
      cout<<endl;
      cout<<"Jumlah Orang yang Hutang : ";
      cin>>jum_orang;

      for (int i=0; i<jum_orang;i++){
        cout<<endl;
        cout<<"Penghutang Ke-"<<i+1<<endl;
        cout<<endl;

        cout<<"Nama Penghutang : ";
        cin>>nama_penghutang[i];

        cout<<"Jumlah      : ";
        cin>>jumlah[i];

        tot+=jumlah[i];

      }

      cout<<endl;
      cout<<"List Hutang"<<endl;
      cout<<"-------------------------------------"<<endl;
      cout<<"No      Nama    Jumlah     "<<endl;
      for (int i=0;i<jum_orang;i++){
        cout<<i+1<<setw(10)<<nama_penghutang[i]<<setw(10)<<jumlah[i]<<endl; //Menampilkan semua nilai array
      }
      cout<<"-------------------------------------"<<endl;

      //Menampilkan Keterangan
      cout<<"Jumlah Piutang : Rp."<<tot<<endl;//Menampilkan jumlah piutang

      //Kondisi untuk menentukan tindakan yang dilakukan
      if (tot>=100000){
        cout<<"Cepat Tagih Hutang Teman-temanmu!";
      }else {
        cout<<"Sabar ya, tunggu mereka membayar";
      }

      }
