import matplotlib.pyplot as plt 
import random

def get_iter_randremoves(movie_name):
    iter = 0
    while len(movie_name) > 0 :
        iter +=1
        choice = random.randit(-1,35)
        if choice == -1:
            choice = " "
        elif choice > 25:
            choice = str(choice - 26)
        else:
            choice = chr(97 + choice)
        movie_name = movie_name.replace(choice,"")

movie_names = []
with open("movienames.txt", "r") as file:
    movie_names = file.readlines()
    file.close()

x = list(range(1,101))
y = []
average_iters = 0
average_len = 0 
for i in x:
    movie_name = random.choice(movie_names)
    movie_names.remove(movie_name)
    movie_name = movie_name.strip().lower()
    iters = get_iter_randremoves(movie_name)
    y.append(iters)
    average_iters = ((average_iters * (i-1)) +iters)/i
    average_len = ((average_len * (i-1)) + len(movie_name)) / i
    print("")
    print("Selcted Movie Name: ", movie_name)
    print("Length of movie name: ", len(movie_name))
    print("Iteration taken: ", iters)

print("")
print("Total plays: ", 100)
print("Average length of Movie Name: ",average_len)
print("Average Iterations: " ,average_iters)
print("Max Iterations: ", max(y))
print("Min Iterations:", min(y))  

plt.plot(x,y)
plt.plot(x , [average_iters]*100)
plt.xlabel("Run Index")
plt.ylabel("Iteration Taken")
plt.title("Iteration talen to empty movie names")
plt.legend(["Iterations", "Average Iteratioins"])
plt.grid()
plt.show()
