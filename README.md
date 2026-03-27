# Ταξινόμηση Σαφήνειας Πολιτικών Απαντήσεων

Υλοποίηση και σύγκριση κατηγοριοποιητών κειμένου για την ανίχνευση αποφυγής 
απαντήσεων σε πολιτικές συνεντεύξεις, στο πλαίσιο του SemEval 2026 Task 6 (CLARITY).
Το μοντέλο ταξινομεί κάθε απάντηση πολιτικού σε τρεις κατηγορίες: 
Clear Reply, Ambivalent και Clear Non-Reply.

## Μοντέλα
- TF-IDF + Logistic Regression με L1 regularization και bigram features
- Word2Vec + Logistic Regression με Skip-gram και averaged word vectors

## Πειράματα
11 πειραματικές εκτελέσεις με συστηματική βελτιστοποίηση υπερπαραμέτρων:
- Εξερεύνηση class weighting, ngram ranges, vocabulary restriction
- GridSearchCV με 5-fold cross-validation για C και solver
- Ανίχνευση και διερεύνηση overfitting μέσω learning curves
- Σύγκριση CBOW vs Skip-gram για Word2Vec

## Αποτελέσματα
- TF-IDF (Run 11): Validation F1 = 0.510
- Word2Vec (Run 9): Cross-validated F1 = 0.506

## Τεχνολογίες
Python · scikit-learn · gensim · Kaggle · LaTeX

## Αρχεία
- `PQAi.ipynb` — Notebook με όλες τις πειραματικές εκτελέσεις
- `report.pdf` — Αναφορά με ανάλυση αποτελεσμάτων και συμπεράσματα
