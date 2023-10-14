print('''|-------------------------------------------------------------|
|                                                             |
|             WELCOME TO MOBILE SALE ANALYSIS MENU            |
|                                                             |
|                                                             |
|       ▂▄▄▓▄▄▂                                             |
|     ◢◤█▀████▄▄▄▄▄▄◤                                       |
|     ██ IP  ████▀▀▀▀▀▀╬                                      |
|     ◥█████◤                                                |
|     ══╩══╩══                                                |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|-------------------------------------------------------------|
''')

import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

alpha=pd.read_csv(r"C:\Users\vaans\Desktop\TATA_IP.csv")
#beta=pd.read.csv()
#gamma=pd.read.csv()
#delta=pd.read.csv()
aa=pd.DataFrame(alpha)
#bb=pd.DataFrame()
#cc=pd.DataFrame()
#dd=pd.DataFrame()

# for ghraphs
alpha1 = alpha.loc[1:10]
alpha2 = alpha.loc[190:198]

def menu() :
    print("[1],for tata analysis")
    print("[2],for maruti analysis")
    print("[3],for toyota analysis")
    print("[4],for volkswagen analysis")
    print("[5]exit the program")
    

menu()
option = int(input("enter your option "))

while option != 0:
    if option == 1:
        print('''
             
             chose an option'''
             
             )
        print('[1] SHOW COLUMNS')
        print('[2] SHOW TOP ROWS')
        print('[3] SHOW BOTTOM ROWS')
        print('[4] SHOW SPECIFIC COLUMN')
        print('[5] FOR THE GRAPH BETWEEN LOW AND HIGH (for top rows)')
        print('[6] FOR THE GRAPH BETWEEN LAST AND CLOSE (for bottom rows)')
        choice = int(input('enter your choice'))
        if choice == 1:
            print(alpha)
        elif choice == 2:
            print(alpha.loc[1:10])
        elif choice == 3:
            print(alpha.loc[190:198])
        elif choice == 4:
            print('''
            
            chose an option
            
            ''')
            print('[1] FOR COLUMN DATE')
            print('[2] FOR COLUMN OPEN')
            print('[3] FOR COLUMN HIGH')
            print('[4] FOR COLUMN LOW') 
            print('[5] FOR COLUMN LAST') 
            print('[6] FOR COLUMN CLOSE') 
            qq = int(input('''enter your option 
                           
                           '''))
            if qq == 1:
                print(alpha.loc[:,'Date'])
            elif qq == 2:
                print(alpha.loc[:,'Open'])
            elif qq == 3:
                print(alpha.loc[:,'High'])
            elif qq == 4:
                print(alpha.loc[:,'Low'])
            elif 11 == 5:
                print(alpha.loc[:,'Last'])
            elif qq == 6:
                print(alpha.loc[:,'Close'])
            else :
                print(" invalid ")
        elif choice == 5:
            a1 = alpha1.High
            b1 = alpha1.Low
            plt.plot(b1,a1,)
            plt.show()
        elif choice == 6:
            a11 = alpha2.Last
            b11 = alpha2.Close
            plt.plot(a11,b11,)
            plt.show()
#alpha over

    elif option == 2:
        print('''
             
             chose an option'''
             
             )
        print('[1] SHOW COLUMNS')
        print('[2] SHOW TOP ROWS')
        print('[3] SHOW BOTTOM ROWS')
        print('[4] SHOW SPECIFIC COLUMN')
        print('[5] COMPLETE DATASET')
        choice = int(input('enter your choice'))
        if choice == 1:
            print(alpha)
        elif choice == 2:
            print(alpha.loc[1:10])
        elif choice == 3:
            print(alpha.loc[190:198])
        elif choice == 4:
            print('''
            
            chose an option
            
            ''')
            print('[1] FOR COLUMN DATE')
            print('[2] FOR COLUMN OPEN')
            print('[3] FOR COLUMN HIGH')
            print('[4] FOR COLUMN LOW') 
            print('[5] FOR COLUMN LAST') 
            print('[6] FOR COLUMN CLOSE') 
            qq = int(input('''enter your option 
                           
                           '''))
            if qq == 1:
                print(alpha.loc[:,'Date'])
            elif qq == 2:
                print(alpha.loc[:,'Open'])
            elif qq == 3:
                print(alpha.loc[:,'High'])
            elif qq == 4:
                print(alpha.loc[:,'Low'])
            elif 11 == 5:
                print(alpha.loc[:,'Last'])
            elif qq == 6:
                print(alpha.loc[:,'Close'])
            else :
                print(" invalid ")
        elif choice == 5:
            print(alpha)
    elif option == 3:
        print('''chose an option
        
        ''')
        print('[1] SHOW COLUMNS')
        print('[2] SHOW TOP ROWS')
        print('[3] SHOW BOTTOM ROWS')
        print('[4] SHOW SPECIFIC COLUMN')
        print('[5] ADD A NEW RECORD')
        print('[6] DELETE A RECORD')
        print('[7] COMPLETE DATASET')
        choice = int(input('enter your choice'))
        if choice == 1:
            #csv file nhi hai
            print('111')
        elif choice == 2:
            #csv file nhi hai
            print('222')
        elif choice == 3:
            #csv file nhi hai
            print('333')
        elif choice == 4:
            #csv file nhi hai
            print('444')
        elif choice == 5:
            # csv file nhi hai
            print('555')
        elif choice == 6:
            # csv file nhi hai
            print('666')
        elif choice == 7:
            #csv file nhi hai
            print('777')
    elif option == 4:
        print('''chose an option
        
        ''')
        print('[1] SHOW COLUMNS')
        print('[2] SHOW TOP ROWS')
        print('[3] SHOW BOTTOM ROWS')
        print('[4] SHOW SPECIFIC COLUMN')
        print('[5] ADD A NEW RECORD')
        print('[6] DELETE A RECORD')
        print('[7] COMPLETE DATASET')
        choice = int(input('enter your choice'))
        if choice == 1:
            #csv file nhi hai
            print('1111')
        elif choice == 2:
            #csv file nhi hai
            print('2222')
        elif choice == 3:
            #csv file nhi hai
            print('3333')
        elif choice == 4:
            #csv file nhi hai
            print('4444')
        elif choice == 5:
            # csv file nhi hai
            print('5555')
        elif choice == 6:
            # csv file nhi hai
            print('6666')
        elif choice == 7:
            #csv file nhi hai
            print('7777')
    else :
        print('''
              
              invalid option
              
              ''')

    print()
    menu()
    option = int(input("enter your option "))

print("thanks for using this program")
