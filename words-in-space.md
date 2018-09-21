# PyData LA Proposal

## Proposal Information

### Title

Words in Space: A Visual Exploration of Distance, Documents, and Distributions for Text Analysis

### Audience level

Novice

### Brief Description

Machine learning often requires us to think spatially and make choices about what it means for two instances to be close or far apart. So which is best - Euclidean? Manhattan? Cosine? It all depends! In this talk, we'll explore open source tools and visual diagnostic strategies for picking good distance metrics when doing machine learning on text.

#### Detailed Abstract

Whether we're modeling irises, houses in Boston, photos of dogs, or comments on Reddit, machine learning requires us to quantify "distance" between our instances. To do this, we must first imagine that our condos or corgis are points in space, where the relative closeness of any two tells us how similar they are. For text analysis tasks like document classification and topic modeling, our choice of distance metric is particularly important! Why? Because text produces a very high dimensional space, with some features that are much more important than others. Moreover, text is often sparsely distributed, with some feature variations that are much more significant.

Great! So what metric should we use - Euclidean? Manhattan? Minkowski? Jaccard? Cosine? Unfortunately, no two corpora are created equal. The number of documents, their lengths, and vocabulary all significantly impact the distribution and shape of a data set. But while there's no perfect one-size-fits-all distance measure, we can use *visual diagnostics* to begin developing an intuition around distance metrics best suited to a particular problem. Visual diagnostics leverage one of our most powerful analytic tools &mdash; the human visual cortex &mdash; to identify patterns and signals that would otherwise be opaque with purely numeric outputs. The open source visual diagnostics library [Yellowbrick](http://www.scikit-yb.org/en/latest/) is a tool for professional data scientists, engineers, and students to more easily visualize how data is fit and transformed throughout the machine learning process. Yellowbrick provides a visualization API modeled on [scikit-learn's](http://scikit-learn.org/stable/), providing `Visualizers` to support feature analysis, model selection, and hyperparameter tuning.

In this talk, we'll see how to use Yellowbrick to visualize our corpora at both a micro and macro level. We'll begin at a very high level, using stochastic neighbor embedding plots to look at two-dimensional projections of our documents. As we experiment with different [SciPy distance metrics](https://docs.scipy.org/doc/scipy/reference/spatial.distance.html), we can visualize their impact on the distribution of the data, for instance seeing how classes become more or less separable. Next, we can zoom in with token frequency distribution plots to explore feature importances (which in the context of text data will be n-grams). Once we've identified some of the n-grams we expect to be highly influential, we can filter for them using dispersion plots to see how they are distributed throughout the corpus and across documents of varying lengths. By the end of the talk, attendees will walk away with a visual intuition about how words can operate in space and with some new ideas about how to proceed with their own machine learning projects.

## Speaker Information

### First Time Speaking

No

### Affiliation

scikit-yb.org

### Under-represented population?

Yes

### Additional Notes

Rebecca is an active contributor to the open source community, and this talk is based on [Yellowbrick](scikit-yb.org), a project she began building with Benjamin Bengfort in late 2015. Yellowbrick would not be possible without the invaluable contributions of those in the Python and Data Science communities. Since the very first version, the project has accumulated 46 contributors, thanks in large part to the impact of traveling to different events across the country, delivering posters and talks, distributing stickers, and holding sprints.

Rebecca has been a speaker at PyCon, delivering a 2016 talk about [visual diagnostics for machine learning](https://www.youtube.com/watch?v=0MtOu_QlIMQ&feature=youtu.be) that mapped out the foundations of the Yellowbrick project, and in 2017 on [building a custom corpus for natural language processing](https://www.youtube.com/watch?v=j1DdGX2d9BE). She has also given talks at [O'Reilly Strata NYC](https://conferences.oreilly.com/strata/strata-ny-2017/public/schedule/detail/63459), [PyData Carolinas](https://pydata.org/carolinas2016/schedule/presentation/22/), [PyData London](https://pydata.org/london2017/schedule/presentation/42/), and [PyData San Luis](https://pydata.org/sanluis2017/). Rebecca and Benjamin were recently interviewed about their work on Yellowbrick on [Podcast.__init__](https://www.podcastinit.com/yellowbrick-with-bejnamin-bengfort-and-rebecca-bilbro-episode-166/).

In addition to her work on Yellowbrick, Rebecca is co-author of the O'Reilly book, [Applied Text Analysis with Python](http://shop.oreilly.com/product/0636920052555.do) and emeritus board member for Data Community DC - a not-for-profit organization of 13 meetups that organizes free monthly events and lectures for the local data community in Washington, DC.
