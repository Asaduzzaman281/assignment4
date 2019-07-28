# ---assignment4
import networkx as nx 
import matplotlib.pyplot as plt 
%matplotlib inline 
#----------initialising the graph 
N = nx.Graph() 
 
n = nx.generators.small.krackhardt_kite_graph() 
 
print("Nodes krackhardt_kite_graph: ","\n",n.nodes(),"\n") 
print("Edges from krackhardt_kite_graph: ","\n",n.edges()) 
 
 
person = {2:"Md" ,0:"Soma", 7:"Jarif", 8:"Marzan", 9:"Adib", 6:"Ayan", 4:"Moshur", 1:"Asad", 3:"Hemayet", 5:"Uddin"} 
person 
 
#--------------Creating the graph object 
N1 =nx.Graph() 
#---------------Creating the Edges from the graph 
#---Option 1--- 
e1 = [(1,4), (2,4), (0,3), (2,7), (2,5), 
     (3,4), (3,5), (3,6), (4,6), (5,6), (5,7), (6,8), (8,6), (8,5),(8,6),(8,7),(8,6),(9,5)] 
 
#---Option 2--- 
e1 = n.edges() 
 
#---------------Add all the edges to the graph object 
N1.add_edges_from(e1) 
 
print("Edges for named network","\n" ,N1.edges()) 
 
H = nx.relabel_nodes(N1, person) 
print("----------------------\n") 
print(" Nodes for named network: ", "\n", H.nodes()) 
print("----------------------\n") 
print(" Edges for named network: ", "\n", H.edges()) 
 
nx.draw(H, with_labels =1) 
plt.show() 
