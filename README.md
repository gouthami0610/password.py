import random
letters=['a','b','c','d','e','f','g','h','i','j','k','l','m',
         'n','o','p','q','r','s','t','u','v','w','x','y','z',
         'A','B','C','D','E','F','G','H','I','J','K','L','M',
         'N','O','P','Q','R','S','T','U','V','W','X','Y','Z']
numbers=['0','1','2','3','4','5','6','7','8','9']
symbols=['!','%','#','@','$','^','&','*','+','_','-','(' , ')']
print("generate your password")
n_letters=int(input("enter how many letters you want in your password : "))
n_numbers=eval(input("enter how many numbers you want in your password : "))
n_symbols=eval(input("enter how many symbols you want in your password : "))
password_list=[]
password=""
for i in range(n_letters):
    char=random.choice(letters)
    password_list+=char
for i in range(n_numbers):
    num=random.choice(numbers)
    password_list+=num
for i in range(n_symbols):
    sym=random.choice(symbols)
    password_list+=sym
random.shuffle(password_list)
for i in password_list:
    password+=i
print("Your password is : ",password)
