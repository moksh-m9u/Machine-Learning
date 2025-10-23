# Robust Scaling

- it works best with outliers

- when data got outliers Roboust scaling got ur back

- Since MinMaxScaler does not perform good with data having outliers so we have robust scaling which is roboust to outliers

---
## Mathematical Formula

The robust scaling formula transforms features using the median and interquartile range (IQR):

$$X_{scaled} = \frac{X - \text{median}(X)}{\text{IQR}(X)}$$

Where:
- $X$ = original feature value
- $\text{median}(X)$ = median of the feature
- $\text{IQR}(X)$ = Interquartile Range = $Q_3 - Q_1$
- $Q_1$ = 25th percentile (first quartile)
- $Q_3$ = 75th percentile (third quartile)

**Alternative notation:**
$$X_{scaled} = \frac{X - Q_2}{Q_3 - Q_1}$$

Where $Q_2$ is the median (50th percentile).

### Key Properties:
- **Robust to outliers**: Uses median instead of mean
- **Scale invariant**: Uses IQR instead of standard deviation
- **Preserves the shape** of the original distribution
- **Typical range**: Most values fall between -1 and 1, but can extend beyond