# Digit-cancelling-fractions
This problem is too easy if I make int str data and use prime_number algorithm to value of the denominator. But I think my codes is too rought compared to matured developlers yet.So my next chapter is to make this codes matured by studying other codes that other developers has constructed.

list1=[]
list2=[]
a=1
b=1
for i in range(10,100):
    for j in range(i,100):
      i_str=str(i)
      j_str=str(j)
      if i_str[0]==j_str[1]:
          i_pin=int(i_str[1])
          j_pin=int(j_str[0])
          if j_pin!=0:
              if float(i/j)==float(i_pin/j_pin) and i_str[0]!=i_str[1]:
                  print(i,j)
                  a*=i
                  b*=j
      if i_str[1]==j_str[0]:
          i_pin=int(i_str[0])
          j_pin=int(j_str[1])
          if j_pin!=0:
              if float(i/j)==float(i_pin/j_pin) and i_str[0]!=i_str[1]:
                  print(i,j)
                  a*=i
                  b*=j
prime_list=[]
for i in range(2,100):
    t=0
    for j in range(2,i):
        if i%j==0:
            t+=1
    if t==0:
        prime_list.append(i)
print(a,b)
while True:
    t=0
    for i in prime_list:
        if a%i==0 and b%i==0:
            a=a/i
            b=b/i
            print(a,b)
            t=1
    if t==0:
       break
