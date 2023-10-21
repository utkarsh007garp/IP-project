import pandas as pd 
import numpy as np 
import time 
import sys 
import matplotlib.pyplot as plt


csv = pd.read_csv(r"C:\Users\vaans\Desktop\smartphone_cleaned_v5.csv")
ds = pd.DataFrame(csv)

print('''    |-------------------------------------------------------------|
    |                                                             |
    |             WELCOME TO MOBILE ANALYSIS MENU                 |
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

while True :

# THE MAIN MENU 
    print('\n [1] SHOW COMPLETE DATABASE ')
    print('\n [2] SHOW COLUMNS or SPECIFIC COLUMNS WITH DATASET ')
    print('\n [3] SHOW TOP ROWS ')
    print('\n [4] SHOW BOTTOM ROWS ')
    print('\n [5] DATA VISUALIZATION ')
    print('\n [6] CREDITS ABOUT PROJECT')
    print('\n [0] TO EXIT THE CODE')
    
    
    option = int(input('\n enter a option \n'))
    
    if option == 1 :
        print(ds)
        print('\n enter [1] to get back to the main menu')
        print('enter [2] to exit the code \n')
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
            print('[1] for brand_name')
            print('[2] for model')
            print('[3] for price')
            print('[4] for rating')
            print('[5] for processor_speed')
            print('[6] for battery_capacity')
            print('[7] for internal_memory')
            print('[8] for screen_size')
            print('[9] for primary_camera_rear')
            print('[10] for primary_camera_front')
            print('[0] for going back' )
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
            print('\nenter [1] to get back to the main menu')
            print('enter [2] to exit the code \n')
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
        print('enter a no. below 200 for the output to be defined ')
        print('the output will show you the no. of rows from the last ')
        pogba = int(input('\n >>> \n'))
        if pogba >= 200:
            print('invalid text')
            break
        else :
            print(ds[['brand_name', 'model', 'rating', 'processor_speed', 'battery_capacity', 'internal_memory']].tail(pogba))
            print('\nenter [1] to get back to the main menu')
            print('enter [2] to exit the code \n')
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
        print('''
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
        print('')
        
        
        
        
        
        
        
        
        
    elif option == 6:
        print('''\n
        project made by ~~ UTKARSH SHARMA AND PRANAV SHARMA 
        class ~~ 12 alpha 
        project about ~~ mobile analysis through ghraphs and database \n
        ''')
        
        
        
    elif option == 0:
        print('THANKS FOR USING OUR PROGRAM')
        time.sleep(0.5)
        print('🙏')
        break 
        
