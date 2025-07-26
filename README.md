
count = 0
n = int(input("n: "))

for i in range(n):
    x = int(input("x: "))
    count = count + x

print("The Mean is:", count / n)