# netflix-data-cleaning-excel
Data cleaning and preprocessing of Netflix Titles dataset using Excel 

# Netflix Data Cleaning in Excel

The dataset used was `netflix_titles.csv`, containing Netflix's shows and movies data, including columns such as:
- show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description


### Step 1: Handle Missing Values
- Replaced blank values in `director`, `cast`, and `country` columns with `"Unknown"`.
- Filled missing `date_added` values with `"Unknown"` after converting valid dates to `dd-mm-yyyy` format.

### Step 2: Remove Duplicates
- Removed duplicate rows across all columns to ensure each record is unique.

### Step 3: Standardize Text
- Applied `lower()` and `trim()` to textual columns like `title`, `director`, `cast`, `country`, `listed_in`, and `description`.
- Replaced all variations of "United States" with `"usa"` for country uniformity.

### Step 4: Convert Date Formats
- Standardized the `date_added` column to `dd-mm-yyyy` format using `pd.to_datetime()`.

### Step 5: Rename Columns
- Converted all column names to lowercase and replaced spaces with underscores.

### Step 6: Fix Data Types
- Ensured `release_year` is numeric.
- Created a new column `duration_num` to extract numeric values from the `duration` column (e.g., "90 min" → 90).

---
 Output
- Final dataset: `netflix_dataset'

## Technologies Used
- Excel (for formula reference)
