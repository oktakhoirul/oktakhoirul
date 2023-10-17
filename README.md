#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>
#include "soal_common1.c"

int main(int argc, char *argv[]){
	
	char *garisbatasHorizontal = "---------";//bisa diubah, posisi tanggal menyesuaikan secara otomatis
	char *garisbatasVertikal = "|";//bisa diubah
	char *latarTanggal[] = {" ",".","*","#"};//index bisa dipilih dari 0-3 (untuk merubah tampilan kalender)
	char *spasiAwalKalender = "   ";//bisa diubah
	int kolomMulaiHari = 6;//bisa diubah
	int JumlahBarisKalender = 5;//bisa diubah
	dataPrint dataoutprint;
	
	char *Hari[] = {"sen","sl4sa","rabu","kam","jum'at","sabt*","min"};//bisa diubah, posisi string menyesuaikan panjang string secara otomatis
	
	dataoutprint = ProcessData(kolomMulaiHari,garisbatasHorizontal,garisbatasVertikal,spasiAwalKalender,latarTanggal[0],Hari,JumlahBarisKalender);
	
	for(int i=0;i<dataoutprint.ndata;i++){
		printf("%s\n",dataoutprint.dataOut[i]);
	}
	
	printf("\n\n  Jumlah hari = %d\n",dataoutprint.nDay);
	
	free(dataoutprint.dataOut),dataoutprint.dataOut=NULL;
	
	return 0;
} gabungkan ke dalam kalender
