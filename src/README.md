## 📂 Project Structure

### Notebooks
* **`get_mole_ham_gs_local_MO.ipynb`**
    * **Purpose:** Generates the Hamiltonian for custom molecular systems.
    * **Functionality:** Constructs Hamiltonians using the **PySCF** package and exports a **sparse matrix file** for optimized storage and downstream computation.

* **`LUCJ_ansatz_N2.ipynb`**
    * **Purpose:** Generates electronic structure results for the $N_2$ molecule using the **LUCJ** (Local Unitary Cluster Jastrow) ansatz.
    * **Functionality:** Utilizes IBM's specialized packages to implement the ansatz and compute energy results. This notebook uses $N_2$ as a primary example but can be generalized to other molecular systems.

* **`chem_torch_ get_ci^+_cj_n_related_matrix.ipynb`**
    * **Purpose:** Generates hopping ($\hat{c}_i^\dagger \hat{c}_j$) and number ($\hat{n}_i$) operators in a sparse matrix format.
    * **Functionality:** Pre-computes these operators to enable efficient ansatz evaluation using **sparse matrix-vector multiplication**.
