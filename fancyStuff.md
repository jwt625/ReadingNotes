
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

### Physics related

- Les Houches Summer School: [École de Physique des Houches](https://houches.univ-grenoble-alpes.fr/), [Lecture Notes of the Les Houches Summer School](https://global.oup.com/academic/content/series/l/lecture-notes-of-the-les-houches-summer-school-lnlh/?cc=us&lang=en&)
- on-chip MW circulator
	- [experiment](http://journals.aps.org/prx/abstract/10.1103/PhysRevX.7.011007)
	- Theory: [Hall Effect Gyrators and Circulators](http://journals.aps.org/prx/abstract/10.1103/PhysRevX.4.021019), [Self-Impedance-Matched Hall-Effect Gyrators and Circulators](http://journals.aps.org/prapplied/abstract/10.1103/PhysRevApplied.7.024030)



### Computer related

#### File convert/process
- [pandoc](http://pandoc.org/): convert among many file format
- [Xpdf](http://www.foolabs.com/xpdf/home.html): pdf Viewer, can extract text etc.

#### IDE, Platform, etc.
- [rocket.chat](https://rocket.chat/)

#### TeX
- [iTex2Img](http://www.sciweavers.org/free-online-latex-equation-editor): convert TeX to Img
- [Github with Mathjax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima/related): A very nice Chrome plugin to display TeX math in github .md file on web page

#### Tutorials

- [RF wireless world](http://www.rfwireless-world.com/)

#### Plotting & generating Figure

- [high charts](https://www.highcharts.com/)
- [graphviz](http://www.graphviz.org/)
- [Plotly](https://plot.ly/api/)

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

