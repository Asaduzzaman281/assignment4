import networkx as nx 
import matplotlib.pyplot as plt 
import seaborn as sns
%matplotlib inline
sns.set()
#--- put the values
G = nx.Graph()
g = nx.generators.krackhardt_kite_graph()

print("Notes of krackhardt_kite_graph: ","\n",g.nodes())

print("Notes of krackhardt_kite_graph","\n",g.edges())


plt.figure()

nx.draw_networkx(G)
people = {2:"Carlos" , 5:"Asad", 7:"Jane", 8:"Fernando", 9:"Kazi", 6:"Garth", 4:"Ed", 1:"Billal", 3:"Diane", 0:"Garth"}
people
GH=nx.Graph()
edg=([(0,1),(1,2),(2,3),(3,0),(0,4),(4,1),(4,5),(3,6),(0,6),(2,7),(1,7),(0,8),(1,8),(3,8),(2,8),(7,6),(5,9)])
edg=g.edges()
# ---print edges
GH.add_edges_from(edg)
 
print ("edge of networ","\n",GH.edges())
GL= nx.relabel_nodes(GH, people)
print("print the name in the networks\n")
print(" named network as note: ", "\n", GL.nodes())
print("----------------------\n")
print(" Edges of the  network: ", "\n", GL.edges())
nx.draw(GL,with_labels=1)
plt.show()

result:

