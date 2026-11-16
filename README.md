# TallerEntregables

Python solutions to the exercises of a sorting and searching algorithms workshop. Each exercise is a standalone script that implements or applies a sorting, duplicate-removal, filtering or search routine and prints its result, and some scripts print intermediate steps of the algorithm. The repository appears to be a course assignment submission; the course itself is not named in the repository.

## Features

Scripts in `_Ordenamiento_202110151010/`, one folder per exercise (`Punto N`):

- **Punto 1**: removes duplicate values from a list while keeping first-occurrence order.
- **Punto 2**: removes duplicate values from a sorted list (the same approach as Punto 1 is used).
- **Punto 2 / Punto 7** (folder nested inside Punto 2): returns the non-positive values (`<= 0`) of a list.
- **Punto 4**: Shell sort, printing each element shift and the array after each gap pass.
- **Punto 5**: prints candidate identifiers from a vote array (see Known limitations).
- **Punto 6**: sorts lists of tuples and plain lists with Python's built-in `list.sort()`.
- **Punto 8**: recursive merge sort, printing the divide and merge steps.
- **Punto 10**: linear search over a matrix (see Known limitations).
- **Punto 11**: concatenates two lists and sorts the result with a recursive quicksort.
- **Punto 12**: bucket sort (`ejemplo_bin_sort.py`) with insertion sort inside each bucket, and LSD radix sort with counting sort (`ejemplo_radix_sort.py`).

The top-level `Untitled Diagram.drawio` and the `Untitled Diagram.drawio` inside `_Ordenamiento_202110151010/` are draw.io diagrams. The labels in the top-level one (in Spanish) describe a package-delivery domain (sender, receiver, driver, truck, package). The copy inside the workshop folder was not reviewed in detail.

## Tech stack

- Python 3 (only the standard library; no third-party packages are used).
- draw.io diagram files (`.drawio`, XML).

## Project structure

```
TallerEntregables/
├── Untitled Diagram.drawio
└── _Ordenamiento_202110151010/
    ├── taller_ordenacion.docx        # Workshop statement (not parsed in this README)
    ├── Untitled Diagram.drawio
    ├── Punto 1/elementos_repetidos_1.py
    ├── Punto 2/elementos_repetidos_vector_ordenado_2.py
    ├── Punto 2/Punto 7/ValoresNegativos_7.py
    ├── Punto 4/shell_sort_4.py
    ├── Punto 5/votos_candidatos_5.py
    ├── Punto 6/futbolistas_6.py
    ├── Punto 8/Ordenamiento_mezcla_8.py
    ├── Punto 10/matriz_busqueda_10.py
    ├── Punto 11/union_y_ordenamiento_de_listas_11.py
    └── Punto 12/
        ├── ejemplo_bin_sort.py
        └── ejemplo_radix_sort.py
```

Exercises Punto 3 and Punto 9 have no files in the repository.

## Getting started

There are no dependencies to install. Run any script with Python 3 from its folder, for example:

```bash
git clone https://github.com/jdvalencir/TallerEntregables.git
cd TallerEntregables/_Ordenamiento_202110151010/"Punto 4"
python3 shell_sort_4.py
```

Other examples:

```bash
cd "_Ordenamiento_202110151010/Punto 8" && python3 Ordenamiento_mezcla_8.py
cd "_Ordenamiento_202110151010/Punto 12" && python3 ejemplo_radix_sort.py
```

Each script contains its own sample input at the bottom of the file; edit that input to test other data.

## Known limitations

These scripts were written as workshop answers and are kept as submitted. Reading the code shows the following:

- `Punto 5/votos_candidatos_5.py` prints the list of candidate indices from the last one down to index 1. It does not count votes or determine a winner, and it skips index 0.
- `Punto 10/matriz_busqueda_10.py` iterates over the values of each row and returns `"Si"` or `"No"` from inside the first iteration, so it does not search the whole matrix.
- `Punto 2/elementos_repetidos_vector_ordenado_2.py` does not use the fact that its input is sorted; it is the same algorithm as Punto 1.
- `Punto 12/ejemplo_radix_sort.py` assumes non-negative integers.
- `Punto 12/ejemplo_bin_sort.py` computes bucket indices with floating-point division, so it is intended for the non-negative floats in its sample input.

The scripts have not been executed as part of writing this README.

## Language

Identifiers, comments and printed messages in the code are in Spanish. This README is in English.
