#include <iostream>
#include <conio.h>
using namespace std;

int main ()
{
	int menu,totalHarga,diskon,jmlhHarga;
	int UangPembyran,kembalian,hasil;
	char jawab;
	do
		{
			cout<<"===================================="<<endl;
			cout<<"										"<<endl;
			cout<<"			BUBU PROGRAMMING		"<<endl;
			cout<<"		JL. GIRI DHARMA CAMPLIK NO.9 UNGASAN	"<<endl;
			cout<<"		pingkanpermata@gmail.com		"<<endl;
			cout<<"										"<<endl;
			cout<<"====================================="<<endl<<endl;
			
			cout<<"	MENU TRANSAKSI BARANG	\n\n";
			cout<<"	1. Member	\n";
			cout<<"	2. Bukan Member	\n";
			cout<<"silahkan pilih menu 1-2 ! : ";cin>>menu;
			cout<<"____________________________________________\n";
			cout<<"\n\n";
			
			if (menu==1)
			{
				cout<<"Selamat anda Mendapatkan Tambahan diskon 5%\n";
				cout<<"Masukkan Total Harga : Rp. ";cin>>totalHarga;
				if (totalHarga>100000 && totalHarga<=200000)
				{
					jmlhHarga=totalHarga-totalHarga*15/100;
					cout<<"Anda Mendapatkan Total Diskon 15% dari tambahan diskon 5%\n";
					cout<<"__________________________________________\n";
					cout<<"\n";
					cout<<"Jumlah Pembayaran	: Rp. "<<jmlhHarga;
				}
				else if (totalHarga >200000 && totalHarga<=300000)
				{
					jmlhHarga=totalHarga-totalHarga*20/100;
					cout<<"Anda Mendapatkan Total Diskon 15% dari tambahan diskon 5%\n";
					cout<<"_____________________________________________\n";
					cout<<"Jumlah Pembayaran	: Rp. "<<jmlhHarga;
				}
				else if (totalHarga > 300000)
				{
					jmlhHarga =totalHarga-totalHarga*25/100;
					cout<<"Anda Mendapatkan Total Diskon 15% dari tambahan diskon 5%\n";
					cout<<"_______________________________________________\n";
					cout<<"Jumlah Pembayaran	: Rp. "<<jmlhHarga;
				}
				else if (totalHarga<=100000)
				{
					cout<<"\n";
					cout<<"________________________________________________"<<endl;
					cout<<"|Maaf Anda Tidak Mendapatkan Diskon		|\n";
					cout<<"|Dikarenakan Total Belanja Tidak Lebih dari Rp. 100.000|\n";
					cout<<"________________________________________________\n"<<endl;
					cout<<"Total Harga		: Rp."<<totalHarga;
					jmlhHarga=totalHarga;
				}
			}
			else if(menu==2)
			{
				cout<<"Masukkan Total Harga	: Rp.";cin>>totalHarga;
				if (totalHarga >100000 && totalHarga<=200000)
				{
					jmlhHarga=totalHarga-totalHarga*10/100;
					cout<<"Anda Mendapatkan diskon 10%\n";
					cout<<"__________________________________\n";
					cout<<"\n";
					cout<<"Jumlah Pembayaran	: Rp. "<<jmlhHarga;
				}
				else if (totalHarga >200000 && totalHarga<=300000)
				{
					jmlhHarga =totalHarga-totalHarga*15/100;
					cout<<"Anda Mendapatkan diskon 15%\n";
					cout<<"__________________________________\n";
					cout<<"\n";
					cout<<"Jumlah Pemabyaran	: Rp."<<jmlhHarga;
				}
				else if (totalHarga > 300000)
				{
					jmlhHarga=totalHarga-totalHarga*20/100;
					cout<<"Anda Mendapatkan diskon 20%\n";
					cout<<"__________________________________\n";
					cout<<"\n";
					cout<<"Jumlah Pembayaran	: Rp."<<jmlhHarga;
				}
				else if (totalHarga<=100000)
				{
					jmlhHarga=totalHarga;
				}
			}
			else if (menu!=1 && menu!=2)
			{
				cout<<"Maaf Anda Diharuskan Memilih Antara Menu 1 atau Menu 2";
			}
			cout<<"\n";
			
			cout<<"Uang Pembayaran	: Rp.";cin>>UangPembyran;
			kembalian=UangPembyran-jmlhHarga;
			cout<<"___________________________________\n";
			cout<<"Uang Kembalian	: Rp."<<kembalian;
			cout<<"\n\n";
			
			if (UangPembyran<=jmlhHarga)
		{
			hasil=(kembalian)*-1;
			cout<<"Pembayaran Anda Kurang	: Rp."<<hasil;
		}
		
		cout<<"\n\n";
		cout<<"Apakah Anda Memilih Menu Transaksi Lagi ? (Y/T)";cin>>jawab;
		}
		while(jawab=='Y' || jawab=='Y');
		
		cout<<"Terimakasih Atas Kunjungannya\n\n"<<endl;
		cout<<"			by : Bubu Programming		";
		
		getch();
}
