	#include "Srexhsp.as"
	exec "stop_watch.exe"
	title "Super Text Editor(ÅMÅEÉ÷ÅEÅL)"
	pos 400,300:color 255,0,0
	gdbox 200,200,2
	pos 400,310:mcalmake 64,0
	chengecur "",4
*start1
	screen 0,640,600,0
	cls 1
	mes1=""
	mesbox mes1,620,300,1
	pos 0,320
	button "SAVE",*save
	pos 80,320
	button "LOAD",*load
	pos 160,320
	objsize 120
	combox c1,300,"äÁï∂éöÉäÉXÉg\n(ÅLÅEÉ÷ÅE`)\n(^É÷^)\n(ÅLÅGÉ÷ÅGÅM)\n(ÅLAÅM)"
	objsize 64
	pos 0,360:button "UNDO",*undo1
	pos 80,360:button "Stop",*stop1
	pos 160,400:button "Script",*script
	pos 240,400:button "ScriptGo",*scriptgo
	pos 0,420:mes "âÊëúÉrÉÖÅ[Éè"
	pos 0,440:button "View",*view1
	pos 80,440:button "Convert",*view2
	lb2=0
	objsize 120
	list="ï∂éöäG\nÑ¨\nÑ≠\nÑØ\nÑÆ\nÑ´\nÑ™"
	pos 160,360:combox lb2,64,list
	coloful 0,230|(230<<8)|(230<<16)
	objcolor 64|(64<<8)|(64<<16)
*main2
	randomize
	rnd a1,899
	a1+=100
	randomize
	rnd a2,499
	a2+=500
	pos 430,490:
	mes "î]ÉgÉå":mes ""+a1+"+"+a2
	input c2
	button "Answer",*kaitou

	goto *loop1
*script
	mes1+="art s.jpg\nmem Hello Jap\nmem Do you like susi\naro\nart s2.jpg\nsog tes1.wav\naaro\nart s2.jpg\nmem I like Hamburger\nmem Oh good\naro\nend"
	objprm 0,mes1
	wait 10
	goto *loop1
*view1
	dialog "",16
	if (stat==0){
	goto *loop1
	}
	screen 2
	picload refstr
	goto *loop1
*view2
	htm1="<html>\n"
	dirlist htm2,"*.jpg",0
	notesel htm2
	notemax max1
	repeat max1
		noteget z1,cnt
		htm1+="<a href=\""+z1+"\">"
		htm1+="<img src=\""+z1+"\">"
		htm1+="</a><BR><BR>\n"
		wait 1
	loop
	htm1+="</html>"
	strlen c6,htm1
	bsave "test.html",htm1,c6
	exec "test.html",16
	goto *loop1

*scriptgo
	notesel mes1
	line=0
	cls 1
	pos 440,300
	button "NEXT",*main3
	pos 0,0
	page1=0
	y2=360
*main
	repeat
	if(stop2==0){
	noteget bun,page1
	getstr com,bun,0,' '
	getstr fil,bun,4
	if(com=="art"){picload fil,1}
	if(com=="aro"){stop}
	if(com=="sog"){sndload fil}
	if(com=="mem"){pos 20,y2:mes fil:mes "\n":y2+=32}
	if(com=="end"){goto *start1}
	stop2=1
	}
	wait 10
	loop
*main3
	stop2=0
	page1+=1
	goto *main
*stop1
	a=0
	a2=-1
	if(flg2==0){
	objsend 0,$cf,-1,a,1	; èëÇ´çûÇ›ã÷é~ÉtÉâÉOÇÃê›íË
	objsend 1,$f4,$01,a2,1
	objsend 2,$f4,$02,a2,1
	objsend 3,$f4,$03,a2,1
	objsend 4,$f4,$04,a2,1
	objsend 5,$f4,$05,a2,1
	objsend 6,$f4,$01,a2,1
	flg2=1
	}else{
	objsend 0,$cf,o,a,1
	objsend 1,$f4,$00,a2,1
	objsend 2,$f4,$00,a2,1
	objsend 3,$f4,$00,a2,1
	objsend 4,$f4,$00,a2,1
	objsend 5,$f4,$00,a2,1
	objsend 6,$f4,$00,a2,1
	flg2=0
	}
	goto *loop1
*undo1
	a3=0
	objsend 0,$c7,0,a3,1
	goto *loop1
*kaitou
	if(c2==(a1+a2)){
	color 255,255,255
	boxf 430,490,600,600
	color 0,0,0
	pos 430,580
	mes "Good"
	}else{
	color 255,255,255
	boxf 430,490,600,600
	color 0,0,0
	pos 430,580
	mes "Bad"
	}
	goto *main2
*loop1
	if(c1==1){
	mes1+="(ÅLÅEÉ÷ÅE`)"
	objprm 0,mes1
	c1=0
	}
	if(c1==2){
	mes1+="(^É÷^)"
	objprm 0,mes1
	c1=0
	}
	if(c1==3){
	mes1+="(ÅLÅGÉ÷ÅGÅM)"
	objprm 0,mes1
	c1=0
	}
	if(c1==4){
	mes1+="(ÅLAÅM)"
	objprm 0,mes1
	c1=0
	}
	if(lb2==1){
	mes1+="Ñ¨"
	objprm 0,mes1
	lb2=0
	}
	if(lb2==2){
	mes1+="Ñ≠"
	objprm 0,mes1
	lb2=0
	}
	if(lb2==3){
	mes1+="ÑØ"
	objprm 0,mes1
	lb2=0
	}
	if(lb2==4){
	mes1+="ÑÆ"
	objprm 0,mes1
	lb2=0
	}
	if(lb2==5){
	mes1+="Ñ´"
	objprm 0,mes1
	lb2=0
	}
	if(lb2==6){
	mes1+="Ñ™"
	objprm 0,mes1
	lb2=0
	}
	lb2=0
	wait 10
	goto *loop1
*save
	dialog "txt",17
	if (stat==0){
	goto *loop1
	}
	strlen a1,mes1
	bsave refstr,mes1,a1
	goto *loop1
*load
	dialog "txt",16
	if (stat==0){
	goto *loop1
	}
	bload refstr,mes1
	objprm 0,mes1
	goto *loop1
	