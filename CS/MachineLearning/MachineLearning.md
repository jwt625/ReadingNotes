# Machine Learning

From [coursera](https://www.coursera.org/learn/machine-learning)


Started on Jan 29, 2017.
```noteinfo
{
	"date": {
		"y": 2017,
		"m": 1,
		"d": 30
	},
	"tag": ["study", "other"]
}
```

[toc]

## Intro

[toc]

### Examples:
- Database mining
- Application can't program by hand
	- autonomous helicopter, handwriting recognition, most natural language processing, computer vision
- Self-customizing programs


### Supervised learning

Concepts:
- Feature/Attribute

Two types of problem:
- Classification
- Regression



```dot-parse
digraph G {
	graph [
	rankdir = "LR";
	bgcolor="black";
	];
	edge[color="white";fontcolor="white";];
	node[color="white";fontcolor="white";];

	TrSet[label="Training set";shape=rectangle;];
	LeAlgo[label="Learning algorithm";shape=rectangle;];
	h[label="h";];
	x[shape=circle;];
	y[shape=circle;];
	// connections
	TrSet->LeAlgo->h;
	x->h->y;
}
```

### Unsupervised learning

Not told the structure/feature/type. Automatically find the structure/pattern

E.g., clustering algorithm

Application:
- organize computer cluster
- social network analysis
- market segmentation
- astronomical data analysis

Cocktail party problem: two sound source, two microphone with different distances to the sound source, separate the two sound.

Quiz finished at 22:00, Jan 30, 2017.

## Model and Cost Function

Training set, notations: $m, x, y$

Hypothesis, Parameters, Cost function

Gradient descent

$\alpha$ is called the learning rate

## Linear Regression with Multiple Variables

[toc]

### Multiple features

### Gradient descent for multi var

$$
\theta_j := \theta_j - \alpha \frac{1}{m}\sum_{i=1}^{m}(h_{\theta}(x^{(i)})-y^{(i)})x_j^{(i)}
$$


### Feature scaling

Feature scaling: Get every feature into approximately a $-1\le x_i\le 1$ range.

For cost functions having squeezed oval contours, gradient descent might go back and forth many times until convergence. Hence it's useful to rescale the features.

Mean normalization: Replace $x_i$ with $ x_i - \mu_i$ to make features have approximately zero means (do not apply to $x_0 = 1$).


$\require{AMSsymbols}\therefore x_i := \frac{x_i- \mu_i }{S_i} $ where $S_i$ is the range and $ \mu_i $ is the mean value


### Learning rate

Too big: $J$ goes up vs number of iterations

Too small: converge too slow

$\therefore$ try the largest $\alpha$ then use value a little bit smaller than that

### Polynomial regression

- combine features
- change the behavior or curve of the hypothesis function to quadratic, cubic, square root, etc.



























<!-- ## Test Graphviz

Test LaTeX

```dot-parse
digraph G {

	graph [
	rankdir = "LR";
	bgcolor="black";
	];
	edge[color="white";fontcolor="white";];
	node[color="white";fontcolor="white";];

	h[label="$\\theta$";shape=rectangle;];
	h1[label="$\\frac{\\partial}{\\partial \\alpha}$";shape=circle;];
	h2[label="$\\int_{\\Omega} d \\omega = \\int_{\\partial \\Omega} \\omega$";shape=rectangle;];
	h1->h2[label="$\\sum_n^{\\infty} \\frac{1}{n^2}$";];
	h->h2[label="$e^{i\\theta}$"]
	a[URL="#intro";];
	a->{b->c}
}
``` -->







