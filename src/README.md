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

* **`mole_optim_backprop.ipynb`**
    * **Purpose:** Executes the optimization routine for molecular ground state preparation using backpropagation.
    * **Functionality:** Optimizes ansatz parameters based on user-defined inputs.
    * **Key Parameters:**
        * `molecule_name`: Name of the target molecule.
        * `n_orbitals`: Number of orbitals in the active space.
        * `n_a`, `n_b`: Number of alpha (spin-up) and beta (spin-down) electrons.
        * `bond_length`: Interatomic distance.
        * `basis_choice`: Basis set selection (e.g., STO-3G, 6-31G).
        * `para_repeat_times`: The depth of the ansatz (number of layers).
