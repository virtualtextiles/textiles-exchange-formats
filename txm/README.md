# txm format
## Introduction
Txm (TeXtile Markup Language) is XML based format for saving textile structures at yarn and fiber level.
It was originally developed by company TexMind for saving of its simulated products. In the book "Warp knitted fabrics construction" https://www.routledge.com/Warp-Knitted-Fabrics-Construction/Kyosev/p/book/9781498780162 the txm format is use for providing the geometry of 100 samples to the book as 3D view, which can be visualised with the freeware Texmind Viewer. 
The format was developed in the time, where the 3D formats as GLB was not enough supported in the office procucts and the use of simple mesh files (Obj, x3D) was not convinient for exchange of TEXTILE related 3D data.  

## Data Structure Idea
The textile Structure is stored within the <TextileStructure> field and can have multiple Groups of yarns <YarnGroup>. One one YarnGroup can be for instance the set of warp or weft yarns in a woven structure,the yarns from one guide bar in the warp knitted structure, the yarns in one track in the braiding or any other way.
Each YarnGroup can contain multiple Yarns, but at least one.
Year Yarn contains multiple Fibers, but at least one.
The axis of each fiber is stored inside of the "Fiber" object as list of "Points".
Each upper hierarchical level has variable NumberOf... with the information regarding the nubmer of child objects in it, in order to simply the reading process.

## Example

```xml
<?xml version="1.0" encoding="iso-8859-1" ?>
<TextileStructure>
    <mName value="Simple Textile" />
    <numberOfYarnGroups value="1" />
    <YarnGroup>
        <mName value="Group_0" />
        <numberOfYarns value="1" />
        <Yarn>
            <mName value="Yarn_1" />
            <numberOfFibres value="1" />
            <Fibre>
                <mName value="Yarn1_F1" />
                <mDiameter value="1" />
                <mRed value="128" />
                <mGreen value="128" />
                <mBlue value="255" />
                <numberOfPoints value="4" />
                <Point>
                    <mX value="2.55" />
                    <mY value="0" />
                    <mZ value="0.785398" />
                </Point>
                <Point>
                    <mX value="2.35589" />
                    <mY value="0.975843" />
                    <mZ value="1.5708" />
                </Point>
                <Point>
                    <mX value="1.0253" />
                    <mY value="1.0253" />
                    <mZ value="2.35619" />
                </Point>
                <Point>
                    <mX value="0.554891" />
                    <mY value="1.33963" />
                    <mZ value="3.14159" />
                </Point>
            </Fibre>
        </Yarn>
</TextileStructure>
```