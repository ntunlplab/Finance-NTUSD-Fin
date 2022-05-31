# NTUSD-Fin: A Market Sentiment Dictionary for Financial Social Media Data Applications
# Introduction
NTUSD-Fin provides various scoring methods including frequency, CFIDF, chi-squared value, market sentiment score and word vector for the tokens. Only the tokens appeared at least ten times and shown significantly difference between expected and observed frequency with chi-squared test are remained in our dictionary. The predetermined significance level is 0.05. The market sentiment score is calculated by substracting the bearish PMI from the bullish PMI. There are 8,331 words, 112 hashtags and 115 emojis in the constructed dictionary, NTUSD-Fin.

# Format
There are 8 parts for each token (word, hashtag, or emoji), and they are saved in json format.

“token”: word, hashtag, or emoji
“bull_freq”: frequency in bullish set.
“bear_freq”: frequency in bearish set
“bull_cfidf”: collection frequency in bullish set.
“bear_cfidf”: collection frequency in bearish set.
“chi_squared”: chi squared test result of the token.
“market_sentiment”: calculated by bullish PMI minus bearish PMI.
“word_vec”: 300-dimension word vector.
# Example
```yaml
{

'token': 'buy',

'bull_freq': 14489,

'bear_freq': 1592,

'bull_cfidf': 61.539806954702385,

'bear_cfidf': 52.32250663139482,

'chi_squared': 14711.705215251208,

'market_sentiment': 0.5961743093876137,

'word_vec': [0.0928284227848053, -0.10893399268388748, 0.12348346412181854, … , -0.01443735882639885]

}
```

# Download
Please go to [resources page](http://nlg.csie.ntu.edu.tw/nlpresource/NTUSD-Fin/) to access resources.

# How to Cite the Corpus
Please cite the following paper when referring to the NTUSD-Fin in academic publications and papers.

Chung-Chi Chen, Hen-Hsen Huang and Hsin-Hsi Chen. 2018. NTUSD-Fin: A Market Sentiment Dictionary for Financial Social Media Data Applications. In Proceedings of the 1st Financial Narrative Processing Workshop, 7 May 2018, Miyazaki, Japan.
# License
NTUSD-Fin is licensed under the [Creative Commons Attribution-Non-Commercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.
