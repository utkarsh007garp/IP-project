import pandas as pd 
import numpy as np 
import time 
import sys 
import matplotlib.pyplot as plt


csv = pd.read_csv('smartphone_cleaned_v5.csv')
ds = pd.DataFrame(csv)
def delay_print(s):
    for c in s:
        sys.stdout.write(c)
        sys.stdout.flush()
        time.sleep(0.01)
delay_print('''    |-------------------------------------------------------------|
    |                                                             |
    |***********|WELCOME TO MOBILE SALES ANALYSIS MENU|***********|
    |=============================================================|                                                            
    |         Created by: Utkarsh Sharma | Pranav Sharma          |
    |                                                             |
    |                                                             |
    |                       ▂▄▄▓▄▄▂                             |
    |                      ◢◤█▀████▄▄▄▄▄▄◤                      |
    |                      ██ IP  ████▀▀▀▀▀▀╬                     |
    |                      ◥█████◤                               |
    |                      ══╩══╩══                               |
    |                                                             |
    |-------------------------------------------------------------|
    ''')



while True :
    print('\n [1] SHOW COMPLETE DATABASE ')
    print('\n [2] SHOW COLUMNS or SPECIFIC COLUMNS WITH DATASET ')
    print('\n [3] SHOW TOP ROWS ')
    print('\n [4] SHOW BOTTOM ROWS ')
    print('\n [5] DATA VISUALIZATION ')
    print('\n [6] CREDITS ABOUT PROJECT')
    print('\n [0] TO EXIT THE CODE')


    option = int(input('\n Enter a Option \n'))

    if option == 1 :
        print(ds)
        print('\n Enter [1] to get back to the main menu')
        print('Enter [2] to exit the code \n')
        breaker = int(input('\n >>> \n'))
        if breaker == 1:
            def delay_print(s):
                for c in s:
                    sys.stdout.write(c)
                    sys.stdout.flush()
                    time.sleep(0.069)
            delay_print("Loading... back ... to... the... menu... \n \n")


        elif breaker == 2: 
            print('\n Thank You for using \n')
            break


    elif option == 2 :
        print('  brand_name , model , price , rating , has_5g , has_nfc , has_ir_blaster , processor_brand , num_cores , processor_speed \n , battery_capacity , fast_charging_available , fast_charging , ram_capacity , internal_memory , screen_size, refresh_rate \n , resolution , num_rear_cameras , num_front_cameras , os , primary_camera_rear , primary_camera_front \n\n ')

        print('[1]  FOR SPECIFIC COLUMN')
        print('[2]  FOR GOING BACK TO MAIN MENU')
        print('[3]  FOR EXITING THE CODE')
        breaker = int(input('\n >>> \n'))
        if breaker == 1 :
            print('[1] For brand_name')
            print('[2] For model')
            print('[3] For price')
            print('[4] For rating')
            print('[5] For processor_speed')
            print('[6] For battery_capacity')
            print('[7] For internal_memory')
            print('[8] For screen_size')
            print('[9] For primary_camera_rear')
            print('[10] For primary_camera_front')
            print('[0] For going back' )
            option1 = int(input('\n ENTER YOUR CHOICE \n'))

            if option1 ==1 :
                print(ds.loc[:,'brand_name'])
            elif option1 == 2:
                print(ds.loc[:,'model'])
            elif option1 == 3:
                print(ds.loc[:,'price'])
            elif option1 == 4:
                print(ds.loc[:,'rating'])
            elif option1 == 5:
                print(ds.loc[:,'processor_speed'])
            elif option1 == 6:
                print(ds.loc[:,'battery_capacity'])
            elif option1 == 7:
                print(ds.loc[:,'internal_memory'])
            elif option1 == 8:
                print(ds.loc[:,'screen_size'])
            elif option1 == 9:
                print(ds.loc[:,'primary_camera_rear'])
            elif option1 == 10:
                print(ds.loc[:,'primary_camera_front'])
            elif option1 == 0:
                    break
            else :
                print('\n invalid \n')

        elif breaker == 2:
            def delay_print(s):
                for c in s:
                    sys.stdout.write(c)
                    sys.stdout.flush()
                    time.sleep(0.069)
            delay_print("Loading... back ... to... the... menu... \n \n")


        elif breaker == 3: 
            print('\n Thank You for using \n')
            break

        else :
            print('invalid option')
            break 


    elif option == 3:
        print('enter a no. above 1 for the output to be defined ')
        print('the output will show you the rows from the no. you entered till 1 ')
        pogba = int(input('\n >>> \n'))
        if pogba == 1:
            print('invalid text')
            break
        else :

            print(ds[['brand_name', 'model', 'rating', 'processor_speed', 'battery_capacity', 'internal_memory']].head(pogba))
            print('\nEnter [1] to get back to the main menu')
            print('Enter [2] to exit the code \n')
            breaker = int(input('\n >>> \n'))
            if breaker == 1:
                def delay_print(s):
                    for c in s:
                        sys.stdout.write(c)
                        sys.stdout.flush()
                        time.sleep(0.069)
                delay_print("Loading... back ... to... the... menu... \n \n")


            elif breaker == 2: 
                print('\n Thank You for using \n')
                break

    elif option == 4:
        print('Enter a no. below 200 for the output to be defined ')
        print('The output will show you the no. of rows from the last ')
        pogba = int(input('\n >>> \n'))
        if pogba >= 200:
            print('invalid text')
            break
        else :
            print(ds[['brand_name', 'model', 'rating', 'processor_speed', 'battery_capacity', 'internal_memory']].tail(pogba))
            print('\nEnter [1] to get back to the main menu')
            print('Enter [2] to exit the code \n')
            breaker = int(input('\n >>> \n'))
            if breaker == 1:
                def delay_print(s):
                    for c in s:
                        sys.stdout.write(c)
                        sys.stdout.flush()
                        time.sleep(0.069)
                delay_print("Loading... back ... to... the... menu... \n \n")


            elif breaker == 2: 
                print('\n Thank You for using \n')
                break

    elif option == 5:
        def delay_print(s):
            for c in s:
                sys.stdout.write(c)
                sys.stdout.flush()
                time.sleep(0.01)
        delay_print('''
        |--------------------------------------------|
        |                                            |  
        |        ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄           |                         
        |        █ 11:11     □    100◢◤ █           |      
        |        █                       █           |      
        |        █                       █           |
        |        █                       █           |      
        |        █                       █           |
        |        █                       █           |      
        |        █                       █           |
        |        █                       █           |     
        |        █                       █           |
        |        █         DATA          █           |      
        |        █     VISUALIZATION     █           |     
        |        █         MENU          █           |      
        |        █                       █           |     
        |        █                       █           |
        |        █                       █           | 
        |        █                       █           |
        |        █                       █           |      
        |        █                       █           |      
        |        █                       █           |     
        |        █                       █           |     
        |        █    ◀     ███     ⬤   █           |     
        |        █▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄█           |  
        |                                            |  
        |--------------------------------------------|
        ''')

        print('BAR GRAPH OF brand_name with respect to rating \n')
        print('[1] For Samsung')
        print('[2] For Vivo')
        print('[3] For Nokia')
        print('[4] For Apple')
        print('[5] For Xiaomi')
        print('[6] For Oppo')
        print('[7] For One Plus')
        print('[8] For Poco')
        print('[9] For Igoo')
        print('[10] For Realme')
        print('[11] For Motorola' )
        print('[12] For Tecno')
        print('[13] For Infinix')
        print('[14] For Google')
    
        opt2 = int(input('\n ENTER YOUR CHOICE \n'))
        if opt2==1:
            Price=[16499,114990,31239,23790,39999]
            Rating=[80,87,88,85,82]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==2:
            Price=[16990,9999,14499,35999,42990]
            Rating=[80,65,72,85,87]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==3:
            Price=[18000,13500,31000,22000,11999]
            Rating=[69,71,79,73,59]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==4:
            Price=[65999,129990,38999,74999,119900]
            Rating=[79,76,73,82,83]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==5:
            Price=[29999,24762,17859,32999,19999]
            Rating=[86,79,76,85,83]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==6:
            Price=[18999,45999,29990,28499,9499]
            Rating=[79,86,87,83,62]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==7:
            Price=[54999,19989,28999,32999,39999]
            Rating=[89,81,84,86,85]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==8:
            Price=[14999,20999,14999,16499,12999]
            Rating=[80,81,83,82,76]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==9:
            Price=[29999,13989,59999,21788,28999]
            Rating=[82,75,88,86,82]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==10:
            Price=[24999,18999,19999,27999,8950]
            Rating=[82,87,84,85,64]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==11:
            Price=[14999,18999,10499,15999,22999]
            Rating=[81,79,75,83,85]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==12:
            Price=[39999,6999,11999,6299,19999]
            Rating=[85,62,79,65,80]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==13:
            Price=[18999,19499,17999,36999,8999]
            Rating=[84,85,75,89,69]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
        elif opt2==14:
            Price=[29999,34990,42799,19290,17981]
            Rating=[71,69,75,72,65]
            plt.bar(Rating,Price,color=['r','g','b','y','m'])
            plt.xlabel('Rating',color='r')
            plt.ylabel('Price',color='g')
            plt.show()
    elif option == 6:
        print('''\n
        Project made by ~~ UTKARSH SHARMA AND PRANAV SHARMA 
        Class ~~ 12 alpha 
        Project about ~~ Mobile analysis through graphs and database \n
        ''')
    elif option == 0:
        print('THANKS FOR USING OUR PROGRAM')
        time.sleep(0.8)
        print('🙏')
    else:
        print('\n')
        def delay_print(s):
            for c in s:
                sys.stdout.write(c)
                sys.stdout.flush()
                time.sleep(0.05)
        delay_print("Please Choose a Valid Option. Redirecting to the Main Menu...")
