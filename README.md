# Dimensionality Reduction

A hands-on introduction to dimensionality reduction for data science. The notebooks work through Principal Component Analysis (PCA) and t-SNE, then combine PCA with a classifier inside a scikit-learn pipeline. A final optional exercise brings PCA and t-SNE together with a first look at clustering. You will use datasets such as the wine dataset, Iris, the 20 Newsgroups text corpus, MNIST digits, face images, and real smartphone activity-sensor data.

## Learning Objectives

By the end of this repository, you should be able to:

- Apply PCA to a standardised dataset and calculate the explained variance ratio of each principal component.
- Reduce a dataset to its first principal components and compare classifier accuracy against the original features.
- Use t-SNE to project high-dimensional data (Iris, 20 Newsgroups, MNIST) into two dimensions for visualisation.
- Compare PCA and t-SNE, and select the technique that fits a given task.
- Build a scikit-learn pipeline that combines PCA with a logistic-regression classifier, and apply it to face recognition.

## Learning Path

Work through the notebooks in this order:

| File / Folder | Description |
|---|---|
| [**1 - Principal Component Analysis**](1_principal_component_analysis.ipynb) | Introduction to PCA on the wine dataset: scaling, explained variance, and class separation. |
| [**2 - t-SNE**](2_t_sne.ipynb) | t-Distributed Stochastic Neighbor Embedding applied to Iris, 20 Newsgroups, and MNIST. |
| [**3 - PCA in a Pipeline**](3_pca_in_pipeline.ipynb) | PCA combined with a logistic-regression classifier in a scikit-learn pipeline, applied to face recognition. |
| [**4 - PCA, t-SNE and Clustering (Exercise)**](4_pca_tsne_clustering_exercise.ipynb) | Optional applied exercise: reduce the 561-feature Human Activity Recognition dataset with PCA, cluster it (K-Means, hierarchical, DBSCAN), and visualise the activities with t-SNE. |

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**Data**](data/) | The wine dataset used in the first notebook. |
| [**Solutions**](solutions/) | Reference solutions. |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies. |
| [**uv.lock**](uv.lock) | Dependency lock file. |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it, including the `< >` brackets, with your own value. For example, `cd <repo-name>` becomes `cd ds-dimensionality-reduction`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in (`.venv/`).

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [**scikit-learn: PCA**](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html): Official API reference for `PCA`.
- [**scikit-learn: t-SNE**](https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html): Official API reference for `TSNE`.
- [**scikit-learn: Pipeline**](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html): Chaining preprocessing and a model into a single estimator.
- [**Principal Component Analysis Explained Visually**](https://setosa.io/ev/principal-component-analysis/): Interactive, geometry-first introduction to PCA.
- [**StatQuest: Principal Component Analysis (PCA), Step-by-Step**](https://www.youtube.com/watch?v=FgakZw6K1QQ): A clear video walkthrough of how PCA works.
- [**How to Use t-SNE Effectively**](https://distill.pub/2016/misread-tsne/): Interactive Distill article on reading t-SNE plots without over-interpreting them.
