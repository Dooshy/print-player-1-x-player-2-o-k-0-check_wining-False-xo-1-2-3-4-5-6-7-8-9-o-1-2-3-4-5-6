print ("player 1 (x) ,player 2 (o)")
k=0
check_wining = False
xo=[1,2,3,4,5,6,7,8,9 ]
o=[1,2,3,4,5,6,7,8,9 ]
counter = []
i=0
print ("     |       |    ")
print (xo[0] ,'      ', xo[1], '      ', xo[2])
print ("     |       |    ")
print ("--------------------")
print ("     |       |    ")
print (xo[3] ,'      ', xo[4], '      ', xo[5])
print ("     |       |    ")
print ("--------------------")
print ("     |       |    ")
print (xo[6] ,'      ', xo[7], '      ', xo[8])
print ("     |       |    ")

while True :
     
    
    print ("player 1(x) turn")
    x=int(input("enter the num of the place u wanna put the x\n"))
    
    while x in counter or x not in xo  :
        if x in counter:
            x=int(input("enter the num of the place u wanna put the x and not used before\n"))
        elif x not in xo:
            x=int(input("enter the right  num of the place u wanna put the x \n"))
    if x == 1 :
                xo[0]="x"
    elif x==2:
                xo[1]="x"
    elif x==3:
                xo[2]="x"
    elif x==4:
                xo[3]="x"
    elif x==5:
                xo[4]="x"
    elif x==6:
                xo[5]="x"
    elif x==7:
                xo[6]="x"
    elif x==8:
                xo[7]="x"
    elif x==9:
                xo[8]="x"
    else :
                print ("enter a exsist num and not used before")
    k=k+1
    counter.append(x)
        
    print ("     |       |    ")
    print (xo[0] ,'      ', xo[1], '      ', xo[2])
    print ("     |       |    ")
    print ("--------------------")
    print ("     |       |    ")
    print (xo[3] ,'      ', xo[4], '      ', xo[5])
    print ("     |       |    ")
    print ("--------------------")
    print ("     |       |    ")
    print (xo[6] ,'      ', xo[7], '      ', xo[8])
    print ("     |       |    ")
    print (counter, "those nums used before")
    
    if xo[0]==xo[3]==xo[6] or xo[1]==xo[4]==xo[7] or xo[2]==xo[5]==xo[8]:
        print ("player 1(x) the winner")
        check_wining = True
        break
    elif xo[0]==xo[1]==xo[2] or xo[3]==xo[4]==xo[5] or xo[6]==xo[7]==xo[8]:
        print ("player 1(x) the winner")
        check_wining = True
        break
    elif xo[0]==xo[4]==xo[8] or xo[2]==xo[4]==xo[6] :
        print ("player 1(x) the winner")
        check_wining = True
        break
    elif k == 9:
        break
    print ("player 2(O) turn")
    y=int(input("enter the num of the place u wanna put the O\n"))
    
    while y in counter or y not in xo:
        if y in counter  :
            y=int(input("enter the num of the place u wanna put the O and not used before\n"))
        elif y not in xo:
            y=int(input("enter the right  num of the place u wanna put the O \n"))
        
    if y == 1 :
            xo[0]="O"
    elif y==2:
            xo[1]="O"
    elif y==3:
            xo[2]="O"
    elif y==4:
            xo[3]="O"
    elif y==5:
            xo[4]="O"
    elif y==6:
            xo[5]="O"
    elif y==7:
            xo[6]="O"
    elif y==8:
            xo[7]="O"
    elif y==9:
            xo[8]="O"
    else :
            print ("enter a exsist num")
    k=k+1
    counter.append(y)
    
    print ("     |       |    ")
    print (xo[0] ,'      ', xo[1], '      ', xo[2])
    print ("     |       |    ")
    print ("--------------------")
    print ("     |       |    ")
    print (xo[3] ,'      ', xo[4], '      ', xo[5])
    print ("     |       |    ")
    print ("--------------------")
    print ("     |       |    ")
    print (xo[6] ,'      ', xo[7], '      ', xo[8])
    print ("     |       |    ")
    print (counter, "those nums used before")
    if xo[0]==xo[3]==xo[6] or xo[1]==xo[4]==xo[7] or xo[2]==xo[5]==xo[8]:
        print ("player 2(O) the winner")
        check_wining = True
        break
    elif xo[0]==xo[1]==xo[2] or xo[3]==xo[4]==xo[5] or xo[6]==xo[7]==xo[8]:
        print ("player 2(O) the winner")
        check_wining = True
        break
    elif xo[0]==xo[4]==xo[8] or xo[2]==xo[4]==xo[6] :
        print ("player 2(O) the winner")
        check_wining = True
        break
    
    elif k == 9:
        break
if check_wining == False:
    print ("no one win")

