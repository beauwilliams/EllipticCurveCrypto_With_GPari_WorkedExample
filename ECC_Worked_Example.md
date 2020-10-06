parisize = 8000000, primelimit = 500000
? E= ellinit([1,1],113)
%1 = [Mod(0, 113), Mod(0, 113), Mod(0, 113), Mod(1, 113), Mod(1, 113), Mod(0, 113), Mod(2, 113), Mod(4, 113), Mod(112, 113), Mod(65, 113), Mod(40, 113), Mod(69, 113), Mod(48, 113), Vecsmall([3]), [113, [53, 100, [6, 0, 0, 0]]], [0, 0, 0, 0]]
? P=[3,12]
%2 = [3, 12]
? ellisoncurve(E,P)
%3 = 1
? Q=ellmul(E,P,23)
%4 = [Mod(55, 113), Mod(35, 113)]
? QA=[55,35]
%5 = [55, 35]
? ellisoncurve(E,QA)
%6 = 1
? Pm=[31,45]
%7 = [31, 45]
? k=19
%8 = 19
? C1= ellmul(E,QA,k) //made a boo boo here, should be on point P
%9 = [Mod(71, 113), Mod(98, 113)]
? C1= ellmul(E,P,k)
%10 = [Mod(13, 113), Mod(8, 113)]
? Cm= ellmul(E,QA,k)
%11 = [Mod(71, 113), Mod(98, 113)]
? C2= elladd(E,QA,Pm)
%12 = [Mod(108, 113), Mod(53, 113)]
? C1
%13 = [Mod(13, 113), Mod(8, 113)]
? C2
%14 = [Mod(108, 113), Mod(53, 113)]
? a=23
%15 = 23
? x= ellmul(E,C1,a)
%16 = [Mod(71, 113), Mod(98, 113)]
? ellsub(E,C2,x)
%17 = [Mod(19, 113), Mod(72, 113)]
? Pm
%18 = [31, 45]
? QA
%19 = [55, 35]
? P
%20 = [3, 12]
? k
%21 = 19
? C1=ellmul(E,P,k)
%22 = [Mod(13, 113), Mod(8, 113)]
? x= ellmul(E,QA,k)
%23 = [Mod(71, 113), Mod(98, 113)]
? C2= elladd(E,Pm,x)
%24 = [Mod(98, 113), Mod(112, 113)]
? y= ellmul(E,C1,a)
%25 = [Mod(71, 113), Mod(98, 113)]
? ellsub(E,C2,y)
%26 = [Mod(31, 113), Mod(45, 113)]
? Pm
%27 = [31, 45]
? //success

