# textiles-exchange-formats
Formats for description and 3D exchange of  textile structures (woven, knitted, braided, yarns, seams) 

## txm format
Txm is XML based format for saving textile structures at yarn and fiber level.
It was originally developed by company TexMind for saving of its simulated products. In the book "Warp knitted fabrics construction" https://www.routledge.com/Warp-Knitted-Fabrics-Construction/Kyosev/p/book/9781498780162 the txm format is use for providing the geometry of 100 samples to the book as 3D view, which can be visualised with the freeware Texmind Viewer. 
The format was developed in the time, where the 3D formats as GLB was not enough supported in the office procucts and the use of simple mesh files (Obj, x3D) was not convinient for exchange of TEXTILE related 3D data.  

## Reco-CSV
Reco-CSV is text based format for saving textile structures. It was originally developed during the cooperation between ALC Computertchnik and Y. Kyosev during the development of the first in the world industrial 3D system for warp knitting simulation (2006-2009). Because of it simplicity it becomes often used for exchange of textile data and especially in the education. Each yarn is placed in separated text file. A master text file contain the list of the yarn files.

## Hello CSV
Hello CSV textbased format where all data as XYZ coordinates is provided in ONE file. 