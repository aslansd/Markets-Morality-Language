# Markets, morality and the complexity–efficiency trade-off of languages

A Jupyter notebook that combines

* **Enke (2023)**, *Market exposure and human morality*, Nature Human Behaviour 7:134–141, and
* **Koplenig, Wolfer, Rüdiger & Meyer (2025)**, *Human languages trade off complexity against efficiency*,
  PLOS Complex Systems 2(2): e0000032,

to answer:

1. **Q1** – Do languages of societies with more market exposure, or stronger moral values, differ in complexity
   (entropy rate) and efficiency (text length)?
2. **Q2** – Are moral phrases more or less complex/efficient than the rest of the text in each language, and is that
   related to market exposure?

Everything runs locally on a Mac; no Google Colab, no GPU.

---

## 1. One-time setup (macOS)

You need Python 3.10 or newer. Check in **Terminal**:

```bash
python3 --version
```

If it is missing or older than 3.10, install it from <https://www.python.org/downloads/macos/> (or `brew install python`
if you use Homebrew).

Then, in Terminal, go to this folder (drag the folder onto the Terminal window after typing `cd `) and run:

```bash
cd ~/Downloads/markets_morality_language      # adjust to where you unzipped it
python3 -m venv .venv                          # private Python environment for this project
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

If `pip install` is slow or blocked, try a mirror, e.g.
`pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple` (any PyPI mirror works).

All packages have ready-made wheels for both Apple-silicon (M1–M4) and Intel Macs.

## 2. Run the notebook

```bash
cd ~/Downloads/markets_morality_language
source .venv/bin/activate
jupyter lab combined_analysis.ipynb
```

In the browser window that opens choose **Kernel → Restart Kernel and Run All Cells**.

* **Run time:** about 15–40 minutes on a typical laptop the first time (most of it is compressing ~190 New Testaments
  in Section 4 and the moral-vs-rest comparison in Section 8). Results are cached in `results/`, so later runs take a
  few minutes. For a 2-minute smoke test set `MAX_LANGS = 20` in the settings cell.
* **Memory:** under 2 GB.
* **Internet:** not needed — all inputs are bundled in `data/`. If something is missing, the notebook downloads it and,
  if that fails, prints the exact URL and the folder to save the file in.

The notebook in this folder already contains the outputs of a full run, so you can read the results before running it.
A copy of the result tables and figures from that run is in `reference_results/`; your own run writes to `results/`.

## 3. Optional: add the original data of the two papers

The notebook works without them, using open proxies, but uses them automatically when present.

| Paper | Where | Put files in |
|---|---|---|
| Enke (2023) – market index and morality indices for 943 societies | Harvard Dataverse, doi:10.7910/DVN/EEGV7A (<https://doi.org/10.7910/DVN/EEGV7A>) | `data/enke/` (unzip; `.dta`/`.csv`/`.xlsx` files are detected) |
| Koplenig et al. (2025) – entropy estimates for 6,500 documents | OSF, <https://osf.io/xdwjc/> | `data/koplenig/` |

The notebook prints the columns it detected; if they are wrong, set `ENKE_COLUMNS` (Section 2.4) or `KOP_COLUMNS`
(Section 9). Enke's groups are linked to languages by ISO code, glottocode or name, and — if those are absent — to the
nearest language with a Bible translation within 150 km (`ENKE_LATLON_MATCH`).

## 4. What is in the folder

```
combined_analysis.ipynb   the analysis (executed, with outputs)
requirements.txt          Python packages
data/raw/                 cultural data (D-PLACE subset), Glottolog subset, eBible metadata, eMFD dictionary
data/bible/               New Testament text of 197 translations (NT only, xz-compressed)
data/enke/, data/koplenig/  empty — optional original data (see above)
reference_results/        tables (CSV), figures (PNG) and summary.md from the full run
ATTRIBUTION.md            sources and licences of the bundled data
```

## 5. Settings you may want to change (first code cell)

| Setting | Default | Meaning |
|---|---|---|
| `MODE` | `'full'` | `'core'` = only languages with market/child-value data (faster); `'full'` adds the Ethnographic Atlas high-gods sample |
| `MODELS` | `ppm2, ppm6, lzma` | language models (compressors) |
| `LEVELS` | `char, word, bpe` | symbol levels |
| `Q2_SPLITS` | 3 | random train/control splits in Q2 |
| `N_JOBS` | cores − 1 | parallel processes |
| `MAX_LANGS` | `None` | e.g. `20` for a quick test |
| `ALLOW_DOWNLOAD` | `True` | `False` = strictly offline |

The moral word lists for Q2 are in Section 8.1 (`LEX`) and can be edited; the cache is keyed to them, so Q2 is
recomputed automatically after a change.

## 6. Troubleshooting

* **`ModuleNotFoundError`** – the virtual environment is not active: run `source .venv/bin/activate` before
  `jupyter lab`, or choose the kernel of `.venv` in Jupyter.
* **Parallel processing errors** – the notebook falls back to a single process automatically; you can also set
  `N_JOBS = 1`.
* **The run was interrupted** – just run all cells again; finished languages are read from the cache in `results/`.
* **Start completely fresh** – delete the `results/` folder.
