# orzel_czy_reszka
Gra - orzeł czy reszka

import time

import random

def start():
    print('Witamy w zabawie orzeł czy reszka')
    x = 1
    while x < 4:
        print(x)
        time.sleep(1)
        x += 1
    print('Zabawa rozpoczęta')

def wybor():

    start()

    user_result = 0
    pc_result = 0
    while pc_result < 5:
        user = input("""Proszę o wprowadzenie:
                    o = orzeł
                    r = reszka
                    """)
        if user == 'o':
            user = 1
        else:
            user = 2
        result = int(random.uniform(1,3))
        if user == result:
            print('Gratulacje użytkowniku trafiłeś!')
            user_result += 1
        else:
            print('Niestety nie udało się Tobie')
            pc_result += 1

    print(f'W grze obecnie wygrałeś {user_result}, pojedynków a komputer {pc_result}')



wybor()

