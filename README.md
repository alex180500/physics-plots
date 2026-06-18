# physics-plots

Matplotlib style sheets for physics plots.

## Install

Copy and paste this into a terminal. Run it in the same Python environment where
you use Matplotlib.

In zsh/bash you can install it by running:
```bash
git clone https://github.com/alex180500/physics-plots.git
cp -Rf physics-plots/stylelib "$(python -c 'import matplotlib; print(matplotlib.get_configdir())')"
```

In powershell:
```powershell
git clone https://github.com/alex180500/physics-plots.git
Copy-Item -Recurse -Force physics-plots\stylelib (python -c "import matplotlib; print(matplotlib.get_configdir())")
```

This copies all files from this repository's `stylelib/` directory into
Matplotlib's user style directory, overwriting the styles define in this repository's `stylelib/` if already present. For the location of the directory refer to the [matplotlib documentation](https://matplotlib.org/stable/users/explain/customizing.html#distributing-styles).

## Use

After installing, use the styles by name:

```python
import matplotlib.pyplot as plt

plt.style.use("physics")
```

The `sans` style can be layered on top of `physics` if you want sans-serif
fonts:

```python
import matplotlib.pyplot as plt

plt.style.use(["physics", "sans"])
```
