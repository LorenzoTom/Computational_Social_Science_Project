# Analysis of Gender Asymmetries in Wikipedia
### Computational Social Science project

## Overview

This project analyzes reproduces and expands the research presented in the paper **“Women through the Glass Ceiling: Gender Asymmetries in Wikipedia.”**

---

## Main Findings of the analyzed paper

- **Wikipedia entry as a glass ceiling:**  
  For less notable individuals, women are 10–11% less likely to have a page than men.

- **Topical and linguistic bias:**
  Topical bias (mentioning family/gender) is present mainly in biographies of women born before 1900.  
  Linguistic bias follows the expected LIB pattern:  
  - Men’s biographies are 9% more likely to contain abstract positive terms.
  - Women’s biographies are 1.6% more likely to contain abstract negative terms.

- **Structural bias:**
  Meta-data show strong occupational skew (e.g., men in sports, women in arts).  
  “Spouse” appears significantly more often in women’s biographies.  
  The hyperlink network shows that women are **less central** than men by PageRank, even among top biographies.

The findings confirm the presence of a glass ceiling effect in Wikipedia, reinforcing that women face greater barriers to visibility.  
Moreover, topical and linguistic asymmetries indicate that editors may inadvertently reflect or reproduce external biases. 

For the authors two possible ways to mitigate this could be:
- Clearer editorial guidelines that could help reduce topical bias.  
- Redesigned Search and ranking algorithms to offset systemic visibility disadvantages.

---

## 🔎 Additional Studies and Extended Analysis

Beyond reproducing the original paper’s analyses, **additional studies** were conducted to explore gender asymmetries further, using new datasets and visual methods.

### Extended Analyses Conducted

1. **Network Homophily Analysis**  
   - Measured the number of links between same-gender and mixed-gender nodes
   - Compared proportions to detect homophily

2. **Notability and Inclusion Comparison**  
   - Comparison on the proportions of male and female *local heroes*
   - Calculation of the total and average number of Wikipedia language editions per gender

3. **Topical Bias Investigation**  
   - Investigation on gendered, personal-life, and professional terms in people summaries to quantify topical differences

4. **Network Visualization by Gender**  
   - Visualization of centrality of people of different genders with a gender-colored network structure
        - Both with and without “NA” gender nodes

5. **Centrality and Visibility Analysis**  
   - Identification and visualization of the **top 10 most central nodes**

---

## Datasets Used

| Dataset | Total | Female | Male | “NA” Gender | Notes |
|----------|--------|--------|------|--------------|--------|
| **Politicians** | 7293 | 386 | 2835 | 3221 | Used for all additional analyses |
| **Journalists** | 6996 | 1404 | 3661 | 1931 | Profession-specific dataset |
| **Italians (Born after 1970)** | 717 | 135 | 292 | 290 | General dataset; allows occupational comparison |
| **Italians (Born after 1950)** *(Italian Wikipedia)* | 1188 | 211 | 574 | 403 | Used to test Italian Wikipedia |

> For the last two datasets, since they did not concern specific occupations, it was possible to conduct a study regarding different occupations for different genders.  
> However, for the same reason it was not possible to look for specific professional words.
> A study of Italian writers was also attempted, but the available dataset was too small to give statistically satisfactory results.

---

## Results Summary

### **Politicians**
- **Links between genders:** 1516 / 8093 total → strong homophily (same-gender connections dominate)  
- **Local heroes:** 17.6% (males) vs. 15.0% (females)
- **Languages:**  
  - Total: 269 (males), 157 (females)
  - Average: 6.0 (males), 6.7 (females)  
> Despite fewer total female pages, women appear in slightly more language editions on average.  
> Visualization highlights a visible gender separation in the network and male-dominated top central nodes.

---

### **Journalists**
- **Links between genders:** 4114 / 15378 total → moderate homophily  
- **Local heroes:** 23% (males) vs. 25% (females)  
> Gender clusters remain visible; males dominate structural centrality, though top-ranked women appear comparably central.

---

### **Italians Born After 1970**
- **Links between genders:** 509 / 1958 total → consistent homophily  
- **Local heroes:** 8.9% (males) vs. 11.1% (females)  
> Suggests more limited visibility for women, though females often have slightly higher average centrality.

---

### **Italians Born After 1950 (Italian Wikipedia)**
- **Links between genders:** 180 / 903 total → similar gender-segregated connections  
- **Local heroes:** 5.9% (males) vs. 13.3% (females)
> Data suggest a gender gap, but Italian summaries were too short for reliable linguistic analysis.

---

## Conclusions

Across all datasets, the analyses reveal consistent though not always big **gender asymmetries** in Wikipedia data:

- **Topical bias:** Women’s biographies more often contain gendered or family-related words and fewer professional terms  
- **Structural bias:** Men are often more central in the network, although women’s average centrality ranks are slightly higher
- **Notability bias:** Inclusion thresholds differ between genders, but patterns vary by dataset  
- **Network homophily:** Same-gender links dominate, especially in political and professional domains

Overall, these findings reinforce the persistence of gender bias in online knowledge structures and suggest directions for future mitigation efforts — both algorithmic and editorial.

---

## Future Work

Possible future works on this topic:
- Incorporating **birth date and occupation correlations** to test whether inclusion difficulty varies by profession  
- Analyzing **editor demographics** to study gender in authorship patterns
- Extending studies to **other languages** and cultural contexts of Wikipedia
- Comparing with **external web sources** (e.g., top non-Wikipedia biography pages) to identify whether similar gender asymmetries exist elsewhere

---

## Repository Structure
<pre>
.
├── ComputationalSocialScienceProject.pdf
├── Images
│   ├── Ita1950
│   ├── Ita1970
│   ├── Journalists
│   ├── Politicians
├── Journalists.json
├── finns-1900-1940.json
├── politicians.json
├── project_wikipedia.ipynb
├── wiki.genders.txt
</pre>

## References 

- Wagner, C., Graells-Garrido, E., Garcia, D., & Menczer, F. (2016). *Women through the glass ceiling: gender asymmetries in Wikipedia.*  EPJ Data Science, 5(1). https://doi.org/10.1140/epjds/s13688-016-0066-4

- Dataset with gender for politicians and journalists from publicly available sources Dbpedia: https://wiki.dbpedia.org/