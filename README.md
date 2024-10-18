#استخدام class لمعرفه معلومات الشخص
#مثال على المعلومات الاسم الثلاثي و اللقب تاريخ الميلاد
class information_custmr:

    #اله الاسم الثلاثي مع اللقب و تاريخ الميلاد والجنس
    def __init__(self,Name,NAme,NAMe,Title,Age,Gnder):

        #عمليه اسناد القيم الى(self)
        self.name_custmr  = Name
        self.name_custmr_1 = NAme
        self.name_custmr_2 = NAMe
        self.titel_name = Title
        self.age_custmr = Age
        self.gnder_custmr = Gnder

    #داله لحساب عمر المستخدم
    def age_history(self,years):

        #داله تقوم بجعل العمر الذي ادخله المستخدم str لنقوم باخذ الاعداد الاربعه منها ونعمل عمليه طرح
        str_age = str(self.age_custmr[:4])
        self.years = years
        self.years-=int(str_age)

            #استخدام داله (def) طباعه الموديل مع باقي المعلومات
    def information(self):
        print("*****************************")

        #شرط لمعرفه الذكر من الانثى
        if self.gnder_custmr == "male":
            print("Welcome mr ",self.name_custmr,self.name_custmr_1,self.name_custmr_2,self.titel_name)
        else:
            print("Welcome ms ",self.name_custmr,self.name_custmr_1,self.name_custmr_2,self.titel_name)

        #نطبع (years) بدل ال(age)لكي لا نحصل على عدد سالب
        print("Your age is  ",self.years)

#**********************************************************************************************************************

"""class Bmw:
    
    def __init__(self,name_1,price_1,name_2,price_2,name_3,price_3,name_4,price_4,name_5,price_5,name_6,price_6):
        self.name_1 = name_1
        self.price_1 = price_1
        self.name_2 = name_2
        self.price_2 = price_2
        self.name_3 = name_3
        self.price_3 = price_3
        self.name_4 = name_4
        self.price_4 = price_4
        self.name_5 = name_5
        self.price_5 = price_5
        self.name_6 = name_6
        self.price_6 = price_6"""

#**********************************************************************************************************************
#استخدام خاصيه الوراثه في (class) لمعرفه نوع السياره
class car:

    #استخدام داله (str) في
    def __str__(self):
        return "welcome to BMW cars"

    #1
    #استخدام داله (classmethod)من اجل اختصار عمليه الطباعه
    @classmethod
    def input_car(cls):
        cls.enter = input("Enter model need:  ")
    #1
    #تعريف داله اسناد من اجل ادخال الموديل
    def cars(self,enter):
        self.enter=enter
        self.enter=car.input_car()

    #2
    #استخدام داله (classmethod)من اجل اختصار عمليه الطباعه
    @classmethod
    def input_chooes(cls):
        cls.chooess = input("Enter your choess: ")
    #2
    #تعريف داله اسناد من اجل ادخال الموديل
    def choees(self,chooess):
        self.chooess = chooess
        self.chooess = car.input_chooes()

    #
    @property
    def bank(self):



    #استخدام داله (def) من اجل موديل السيارات
    def car_type(self):
        #استخدام التكرار والشروط لمعرفه الموديل المراد
        print("We have this model in Bmw in 2024 ",["SUVs","Sedan","Coupes"])

         #استخدام (input) واختيار نوع المطلوب
        type=input("Enter the type of car :")

        # استخدام (if) و (while) الشرط والتكرار لاختيار نوع السياره المطلوبه
        if type == "SUVs":
            print("choses any model [BMW 330i ,BMW 540i xDrive]  ")
            while True:
                # استخدام خاصيه (classmethod)1
                car.input_car()

                #car_model = input("Enter the choes: ")
                if self.enter == "BMW 330i":
                    print("BMW 330i:")
                    print("price : starts at $65,700")
                    print("power : 375 horsepower")
                    print("Acceleration : 0 - 60 mph in 5.2 seconds")
                    print("colors : Avaliable in a variety of colors  including white ,black , and blue ")
                    print("do you need [Yes ,Not]")
                    # استخدام خاصيه (classmethod)2
                    car.input_chooes()
                    break

                elif self.enter == "BMW 540i xDrive" :
                    print("BMW 540i xDrive:")
                    print("price : starts at $81,900")
                    print("power : 375 horsepower")
                    print("Acceleration : 0 - 60 mph in 5.8 seconds")
                    print("colors : Avaliable in more than 165 colors  including sliver ,black , and red ")
                    print("do you need [Yes ,Not]")
                    # استخدام خاصيه (classmethod)2
                    car.input_chooes()
                    break

                else:
                    print("Truy agen")
                    break

        elif type == "Sedan":
            print("choses any model [BMW 3 ,BMW 5 ]")
            while True:
                # استخدام خاصيه (classmethod)1
                car.input_car()
                if self.enter == "BMW 3":
                    print("BMW 3 Series 2024:")
                    print("Price: Starts at approximately $43,000")
                    print("Speed: The M340i variant delivers 382 horsepower, with a 0-60 mph time of 4.1 seconds")
                    print("Features: Combines sporty performance with luxury, featuring the iDrive 8 infotainment system, a 12.3-inch display, and premium interior materials")
                    print("Colors: Available in a wide range of colors, including black, white, blue, and gray, along with other premium options")
                    print("do you need [Yes ,Not]")
                    # استخدام خاصيه (classmethod)2
                    car.input_chooes()
                    break

                elif self.enter == "BMW 5" :
                    print("2. BMW 5 Series 2024")
                    print("Price: Starts at around $70,500 for the 530i xDrive model")
                    print("Speed: The i5 M60 xDrive (fully electric) variant offers 593 horsepower, with a 0-60 mph time of 3.7 seconds")
                    print("Features: Includes a curved display, advanced infotainment with in-car gaming via AirConsole, and luxury interior options like a leather-free design")
                    print("Colors: Comes in up to 150 custom colors as part of BMW's Individual program.")
                    print("do you need [Yes ,Not]")
                    # استخدام خاصيه (classmethod)2
                    car.input_chooes()
                    break
                else:
                    print("Truy agen")
                    break

        elif type == "Coupes":
                print("choses any model [BMW M2,BMW 540i xDrive]  ")
                while True:
                    # استخدام خاصيه (classmethod)1
                    car.input_car()
                    if self.enter == "BMW M2":
                        print("BMW M2 Coupe 2024")
                        print("Price: Starts around $63,360")
                        print("Speed: Powered by a 480-hp inline-6 engine, with 0-60 mph in about 4.1 seconds")
                        print("Colors: Includes vibrant options like Fire Red, Voodoo Blue, and Frozen Portimao Blue")
                        print("do you need [Yes ,Not]")
                        # استخدام خاصيه (classmethod)2
                        car.input_chooes()
                        break

                    elif self.enter == "BMW 540i xDrive":
                        print("BMW M240i xDrive Coupe:")
                        print("Price: Starts at approximately $49,700")
                        print("Speed: Features a 382-hp engine and an 8-speed automatic transmission")
                        print(" Colors: Available in classic shades such as Alpine White, Black Sapphire, and Portimao Blue.")
                        print("do you need [Yes ,Not]")
                        # استخدام خاصيه (classmethod)2
                        car.input_chooes()
                        break
                    else:
                        print("Truy agen")
                        break
        else:
            print("sorry we dont have any model")

#***************************************************************************************************************************************************************************************************************************************
#custmr_1 = information_custmr(input("Enter your first name: "),input("Enter your second name: "),input("Enter your third name: "),input("Enter your Title: "),input("Enter your birthday: "),input("Enter your Gender: "))
custmr_1 = information_custmr("Muhammad","alaa","faleh","hasn","2004/3/1","famel")
custmr_1.age_history(2024)
custmr_1.information()
custmr_1=car()
print(custmr_1)
custmr_1.car_type()
