# pokemonPalette ![license](https://img.shields.io/github/license/MilanCalegari/pokePalette) ![version](https://img.shields.io/pypi/v/pokemonPalette) ![stars](https://img.shields.io/github/stars/MilanCalegari/pokePalette?style=social) ![Twittwer](https://img.shields.io/twitter/follow/rmcalegari?style=social)
The pokePalette is a python library generate a color palette based on the colors of a chosen pokemon.  


____
## Requeriments:  
 numpy  
 opencv  
 pokebase   
 sklearn
____
## Usage:

**get_pokemon_palette("pokemon name", numcolors=x)**

```python
>>> from pokemonPalette import pokePalette
>>> palette = pokePalette.get_pokemon_palette("charizard")
>>> print(palette)
['#bd4831', '#0f4F64', '#ef8826', '#edD079']
```
____
### Examples

> ```python
> import seaborn as sns
> import matplotlib.pyplot as plt
> from pokemonPalette import pokePalette
> 
> titanic = sns.load_dataset("titanic")
> palette = pokePalette.get_pokemon_palette('gengar',numcolors=2)
> g = sns.factorplot("class", "survived", "sex", data=titanic, kind="bar", palette=palette, legend=False)
> plt.show()
> ```
> <p align="center">
>    <img  width="175" height="175" src="https://user-images.githubusercontent.com/52531634/130979729-355d3f91-c8aa-4a3a-8082-fb7260c4e5a2.png" />
> </p>  
  
>```python
>import seaborn as sns
>import matplotlib.pyplot as plt
>from pokemonPalette import pokePalette
>
>sns.set_style('white')
>index = ['HP', 'Attack', 'Defense', 'Sp. Atk', 'Sp. Def', 'Speed']
>bulbasaur = [45, 49, 49, 65, 65, 45]
>charmander = [39, 52, 43, 60, 50, 65]
>squirtle = [44, 48, 65, 50, 64, 43]
>
>palette_b = pokePalette.get_pokemon_palette('bulbasaur')
>palette_c = pokePalette.get_pokemon_palette('charmander')
>palette_s = pokePalette.get_pokemon_palette('squirtle')
>
>fig, axes = plt.subplots(1,3)
>fig.suptitle('Initial Pokemons - 1st Generantion')
>sns.barplot(ax=axes[0], x=index, y=bulbasaur, palette=palette_b)
>axes[0].set_title("bulbasaur")
>sns.barplot(ax=axes[1], x=index, y=charmander, palette=palette_c)
>axes[0].set_title("charmander")
>sns.barplot(ax=axes[2], x=index, y=squirtle, palette=palette_s)
>axes[0].set_title("squirtle")
>```
> <p align="center">
>    <img  width="275" height="250" src="https://user-images.githubusercontent.com/52531634/130992215-d5ec9de4-fa29-4ae9-b4d6-37e3be1ddc3e.png" />
> </p>  
  
____
### Plans for next updates
- [ ] Add the option to get shiny Pokemon palette.  
- [ ] Remove repeated colors. 
