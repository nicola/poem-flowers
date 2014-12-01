# POEM: 9*19 Flowers

A love poem that mix visualization art and code poetry. Probably the first poem written in git commits.

- [See the Visualization](https://nicola.github.io/flowers-poem) (and interact with it)
- [Read the Code](https://github.com/nicola/flowers-poem/blob/poem/poem/flowers.html) (in its readable poetic form)
- [Read the Poem](https://github.com/nicola/flowers-poem/commits/poem) (in the commit history)

![Visualization in black](documentation/cover.jpg?raw=true "Visualization in black")

## The Poem

The poem is about preparing a field to grow flowers and making sure that each flower has a beautiful color. These flowers  will shine when seen by the beloved and turn gray when touched. They keep asking to be touched again.

Since in a computer virtual world everything is possible and nothing is real, the lover will *handcraft* flowers from *maths and lines*.

It is possible to read the poem in the commit history in the [poem branch](https://github.com/nicola/flowers-poem/commits/poem).

```
$ git log --format="%C(yellow)%h%Creset %Cgreen%s%Creset%n%b"

ea814f4 POEM: 9*19 flowers
02d0dc0 Handcraft flowers from maths and lines,
aa14064 Choose the colors to make them shine,
ad4e12c Till the soil to plant the seeds.
700b967 .
7cea9e1 See me to make me glow
93c57f8 Touch me to give you more
e023bd0 Touch me you'll never stop
e146d2c Please touch me again.
```

Every commit has a meaningful code attached to it.

[`e023bd0 Touch me you'll never stop`](https://github.com/nicola/flowers-poem/commit/e023bd0b0006470fc2d1df47ace50c7cd0901161)
```diff
+ function stop_touching(d, i) {

+ }
```

## The Visualization

1. Colors are randomly generated. The function `beautiful_color()` makes sure that he lover handcrafts the most beautiful flowers.
2. When flowers are touched they get colourful. When a single one is touched, it changes shape.

![Flower story](documentation/flowerstory.png?raw=true "Flower story")


### The mathematics behind the flowers

The flowers are generated mathematically. The first grid that appears is a matrix, where flowers are generated using using the value of their column and row positions.

The mathematical formula is very simple. I define curves to be 

```
r = cos(kt)

where r = cos(kt)
```

As soon as we land in the visualisation there is a diagonal line towards the matrix. When the column and row number are the same, `k = 1` and therefore we get the identity flower, considered in the code to be *the ugly flower* that the lover deletes. It looks like this:

![Identity flower](documentation/identity.png?raw=true "Identity flower")

Where as soon as we play with `k`, for example `k = 2/1` we get the second flower.

![k2](documentation/k2.png?raw=true "k2")

## Want to contribute?

Clone the repo and install dependencies.

```bash
$ cd poem
$ bower install
```


### The End
