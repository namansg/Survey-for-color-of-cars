Survey-for-color-of-cars
========================

#My first code in python

class myclass:
	sample=0
	w=0      #total no of white cars is zero initially
	b=0		 #black
	g=0		 #gray
	o=0		 #others
	color_list=['Black','White','Gray']
	def __init__(self,name):	#constructor function-is called automatically when an object of this class is created
								#all functions in classes in python takes the argument 'self'
		myclass.name=name 		#myclass.name is a local variable to this class
		print("What's the color of your car?")
		myclass.color=input()
		myclass.sample=myclass.sample+1 #every time the constructor function is called,the sample variable is updated
	def check_color(self):
		if myclass.color in myclass.color_list:
			if myclass.color==myclass.color_list[0]:
				myclass.b=myclass.b+1
			elif myclass.color==myclass.color_list[1]:
				myclass.w=myclass.w+1
			else:
				myclass.g=myclass.g+1
		else:
			myclass.o=myclass.o+1
	def display_result(self):
		print("Hello",myclass.name)
		print("Total number of black cars:",myclass.b)
		print("Total number of white cars:",myclass.w)
		print("Total number of grey cars:",myclass.g)
		print("Other:",myclass.o)
		print("Sample Size:",myclass.sample)

print("Number of samples:")
t=input()
for i in range(0,int(t)):
	print("Please Enter your name:")
	name=input()
	myobj=myclass(name)
	myobj.check_color()
	myobj.display_result()
