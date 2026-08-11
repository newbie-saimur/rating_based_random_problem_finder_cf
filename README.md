# Rating Based Random Problem Finder for Codeforces

This notebook finds **random Codeforces problems you have not solved yet**.
It checks your Codeforces submission history, looks at recent finished contests, filters problems by rating, and prints a few random practice links.

## What it does

1. Reads your Codeforces solved problems.
2. Gets finished contests from the last `last_n_days` days.
3. Collects problems from those contests.
4. Keeps only problems in the rating range you choose.
5. Removes problems you already solved.
6. Shows a small random list of unsolved problems with links.

## You need

- Python
- `requests`

Install `requests` if needed:

```python
pip install requests
```

## Main settings

Edit these values in the notebook:

- `handle` - your Codeforces username
- `min_difficulty` - lowest rating to include
- `max_difficulty` - highest rating to include
- `last_n_days` - how many days back to check for contests
- `num_problems_to_suggest` - how many random problems to show

Example:

```python
handle = "saimur"
min_difficulty = 800
max_difficulty = 1000
last_n_days = 100
num_problems_to_suggest = 3
```

## How to run

### Google Colab

1. Upload the notebook.
2. Install `requests` if it is not already available.
3. Update the settings in `main()`.
4. Run the cell.

### Jupyter Notebook

1. Open the notebook in Jupyter.
2. Install `requests` if needed.
3. Update the settings in `main()`.
4. Run the cell.

### Any IDE

1. Open the `.ipynb` file in an IDE that supports notebooks, or copy the code into a `.py` file.
2. Install `requests`.
3. Update the values in `main()`.
4. Run the script.

## Output

The notebook prints:

- how many problems you already solved
- how many recent contests were found
- how many problems match the rating range
- how many unsolved problems are left
- a few random problem names and links

## Demo output

Example output:

```text
Fetching solved problems for 'srrobin'...
Found 245 solved problems.

Fetching recent contests from the last 100 days...
Found 18 recent contests.

Fetching problems with difficulty 800-1000 from these contests...
Found 42 problems in that range.
Found 19 unsolved problems in that range.

Here are 3 random unsolved problems for you:
1. Problem Name One
	https://codeforces.com/problemset/problem/1234/A

2. Problem Name Two
	https://codeforces.com/problemset/problem/1250/B

3. Problem Name Three
	https://codeforces.com/problemset/problem/1300/C
```

## Notes

- The script uses the public Codeforces API.
- If Codeforces is slow or unavailable, the notebook may show an error.
- If you want easier or harder practice, just change the rating range.

## File

- `RatingBasedRandomProblemFinderCF.ipynb`
