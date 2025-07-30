
value = input("value:")

match value:
    case "individual":
        count = 0
        n = int(input("n: "))
        for i in range(n):
            x = int(input("x: "))
            count = count + x
        print("The Mean for individual is", count / n)

    case "discrete":
        n = int(input("n: "))
        M_fx = 0
        value = 0
        for i in range(n):
            f = int(input("f: "))
            x = int(input("x: "))
            M_fx = M_fx + f * x
            value = f + value
        print("The Mean for discrete is", M_fx / value)

    case "continuous":
        n = int(input("n:"))
        val = 0
        f =  [ ]
        x = [ ]
        for i in range(n):
           n1 = int(input(" "))
           n2 = int(input(" "))
           f1 = int(input(" "))
           f.append(f1)
           ci = (n1 + n2) / 2
           x.append(ci)
           val = val + f[i]
        if len(x) % 2 == 1:
           A = x[int(len(x)/2 - 0.5)]
        else:
           m = int(len(x)/2)
           A = (m + x[m+1]) / 2

        c = n2 - n1
        i = 0
        for i in range(n):
           d = (x[i] - A) / c
           Mfd = 0
           Mfd = Mfd + f[i] * d

        print("The Mean for continuous:", A + (Mfd / val) * c)