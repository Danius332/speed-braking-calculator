def SpeedCalculator(Distance, Time):
    Speed = Distance/Time
    return Speed

def TimeCalculator(Distance, Speed):
    Time = Distance/Speed
    return Time

def BrakingDistanceCalculator(Speed, BrakingAccelaration):
    SpeedInMeterPerSecond = Speed/3.6
    BrakingDistance = Speed**2/(2*BrakingAccelaration)
    return BrakingDistance

def SavingInFile(answer):
    with open("Results.txt", "a", encoding="utf-8") as Results:
        Results.write(str(answer))

def inputs(choice):
    if choice == 1:
        Distance = float(input("Enter distance (in km): "))
        Time = float(input("Enter time (in hours): "))
        Speed = SpeedCalculator(Distance, Time)
        return Speed
    elif choice == 2:
        Distance = float(input("Enter distance (in km): "))
        Speed = float(input("Enter speed (in kmh): "))
        Time = TimeCalculator(Distance, Speed)
        return Time
    elif choice == 3:
        Speed = float(input("Enter speed (in kmh): "))
        BrakingAccaleration = float(input("Enter braking accelaration: "))
        BrakingDistance = BrakingDistanceCalculator(Speed, BrakingAccaleration)
        return BrakingDistance

def menu():
    choice = 0
    print("This program can calculate three things:")
    print("1. Speed")
    print("2. Time")
    print("3. Braking distance")
    
    while choice < 1 or choice > 3:
        choice = int(input("please choose one of these options: "))
        if choice >= 1 and choice <= 3:
            break
        else:
            print("Your input was invalid. Please try again.")
    return choice

def CheckIfPersonWantsToRepeat():
    Valid = False
    while Valid == False: 
        Check = input("Do you wish to calculate something else? (answer Yes or No): ")
        if Check == "Yes" or Check == "yes":
            Repeat = True
            return Repeat
        elif Check == "No" or Check == "no":
            Repeat = False
            return Repeat
            print("Okay bye! Thanks for using my program.")
        elif Check != "No" and Check != "Yes" and Check != "no" and Check != "yes":
            print("Your answer was invalid. Please try again and keep in mind that only valid answers is ""Yes""or ""No"".")

Repeat = True
while Repeat == True:
    choice = menu()
    answer = inputs(choice)
    print(answer)
    SavingInFile(answer)
    Repeat = CheckIfPersonWantsToRepeat()





