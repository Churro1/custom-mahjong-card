# Custom Mahjong Card Template
A LaTeX template for creating personalized, foldable Mahjong rule and scoring cards in the style of the National Mah Jongg League (NMJL). This template provides a standard 15.25" x 4" three-column layout, complete with color-coded suits, scoring columns, and category boxes, making it easy to design and print your own custom yearly hands.

## Features

Standard Sizing: Pre-configured to 15.25in x 4in to mimic the dimensions of a traditional foldable Mahjong card.
3-Column Layout: Automatically flows your categories across three columns.
Color-Coded Suits: Built-in macros for the traditional Blue, Red, Green, and Black color scheme.
Neat Formatting: Pre-built styling for descriptions,concealed/exposed markings, and point values.

## Prerequisites
To compile this template, you will need a working LaTeX distribution (such as TeX Live, MiKTeX, or MacTeX) or an online LaTeX editor like Overleaf.

## How to Use
The template uses simple custom LaTeX commands (macros) to make writing out Mahjong hands quick and readable.

### Suits and Colors
Use the following commands to wrap your tile text. The letters inside the curly braces will automatically be bolded and colored appropriately:

\cB{...} : Blue (Traditionally used for Dots) - e.g., \cB{111}
\cR{...} : Red (Traditionally used for Cracks) - e.g., \cR{2222}
\cG{...} : Green (Traditionally used for Bams) - e.g., \cG{33}
\cFW{...}: Black (Traditionally used for Flowers and Winds) - e.g., \cFW{FFF}

### Hand Descriptions and Scores
Descriptions: Use \desc{...} to add the gray, italicized instructional text next to a hand (e.g., \desc{Any 3 Suits}).
Scores: Use \score{Type}{Points} at the end of a line to display the score.
Type: Typically X (Exposed) or C (Concealed).
Points: The point value (e.g., 25, 30).
Example: \score{C}{30}

### Creating Categories
Group your hands using the \category and \categoryend tags. Every category acts as a stylized box.

Example of a complete category block:
\category{2024 Hands}
\begin{tabularx}{\linewidth}{@{} X r @{}}
\cFW{FF} \cR{20} \cG{24} \cB{2024} \dotfill \desc{Any 3 Suits} \dotfill & \score{X}{25} \\[2pt]
\cFW{NN} \cFW{EE} \cFW{WW} \cFW{SS} \dotfill \desc{Concealed} \dotfill & \score{C}{30} \\[2pt]
\end{tabularx}
\categoryend

(Note: \dotfill creates the dotted line connecting the hand to the score, and \\[2pt] adds a tiny bit of vertical padding between rows).

Reach out if you have questions
