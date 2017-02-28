
```noteinfo
{
	"date": {
		"y": 23,
		"m": 2,
		"d": 2017
	},
	"tag": ["others"]
}
```

## Fancy Stuff

### Computer related

#### File convert/process
- [pandoc](http://pandoc.org/): convert among many file format
- [Xpdf](http://www.foolabs.com/xpdf/home.html): pdf Viewer, can extract text etc.

#### IDE, Platform, etc.
- [rocket.chat](https://rocket.chat/)

#### TeX
- [iTex2Img](http://www.sciweavers.org/free-online-latex-equation-editor): convert TeX to Img
- [Github with Mathjax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima/related): A very nice Chrome plugin to display TeX math in github .md file on web page


#### Mathematica

##### Matrix related
- guide/MatricesAndLinearAlgebra
- useful guide pages:
	- guide/MatrixOperations
	- guide/ConstructingMatrices
	- guide/RearrangingAndRestructuringLists
- Outer product example:
```matehmatica
tmp = Outer[Times, {{1, 0}, {0, 1}}, {{0, 1}, {1, 0}}]
ArrayFlatten[tmp]
```
- transpose irregular shaped matrix:
	- `PadRight` with some variable
	- transpose
	- replace the variable with `Sequence[]`

