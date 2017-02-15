# Adbio Lincs App
The Linc Visualization Tool is web-based network visualization tool, which facilitate the visual exploration of the LINCS L1000 dataset as interactive space. Each node (circle) represents an experiment performed. Edges (lines) represent a similarity score, meaning they have a common signature based on the up and down regulated genes present in that expeiment. Nodes are clustered by cell line, and colored by perturbation (default).

# Usage
#### Main Page
The main page displays a list of perturbations and cell lines that can be dragged to the selection area. Selections can be added to a list of predefined selections by clicking the add button. The user added predefined selections are stored as a cookie and will be lost if the browser cookies are cleared. Clicking the accept button will use the selections to generate the network vizualization.
#### Network Page
If the selections have some simularity a clustered network will be generated. The network visual can be panned by clicking on the background and dragging. The node clusters can be moved around by clicking on a node and dragging. To zoom use the mouse wheel. The Nodes and Edges panel will display information about the nodes. Clicking a node or edge in the panel or on the network visual will select it. This in turn will generate a list of genes in the genes tab, and a list of pathways the pathways panel. The Pathways panel displays Kegg pathways that have over lapping genes present in them. Clicking on a pathway will open the pathway page. To select multiple nodes or edges hode shift while clicking the nodes. Two search fields are provided allowing the user to search and select a group of nodes or a single node. The left search field is limited to just the perturbation or cell line. Selecting one will select and highlight all nodes that are found with the search term. The right search field will search all node attributes, but only allows to select one node. Users can reopen the panels from the settings menu. Also users can change the coloring options in the settings menu. The coloring options are limited to a few predefined color schemes (color range), and predefined node attributes (color domain). Color settings are not saved and will be reset if the page is refreshed.
#### Pathway Page
The Pathway page will display a Kegg pathway image with colored overlay on the gene product. Blue means down regulated, red means up regulated, green means there is a conflict as there is up and down regulated genes located in the same gene product. Hovering over the colored area will display a table with the genes and the node/s and which genes are up or down. A green ! in the data cell means that that gene with that node is both up and down regulated.


# Installing and Running
- download jar
- download database
- install mongodb

Start database using mongodb. Create folder called db in location of the jar file.

Run
```sh
java -jar jarFileName
```
