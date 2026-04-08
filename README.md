# vlim-economic-dispatch
High-performance implementation of the Vectorized Lambda Iteration Method (VLIM) for solving economic dispatch problems in power systems using NumPy

⚡ Vectorized Lambda Iteration Method (VLIM) for Economic Dispatch

A Python implementation of the **Vectorized Lambda Iteration Method (VLIM)** for solving the Economic Dispatch problem in power systems.

This project demonstrates how vectorized numerical computation can significantly accelerate classical optimization methods for generator scheduling.

📄 Related publication:  
Ikhsan et al. (2024), [Vectorized Lambda Iteration Method for Swift Economic Dispatch Analysis](https://doi.org/10.5109/7172306)

⸻

🚀 Features
	•	⚡ Fast computation using vectorization (NumPy)
	•	📉 Up to ~99% reduction in computation time
	•	⚙️ Supports key constraints:
	•	Power balance constraint
	•	Generation limits
	•	Ramp rate constraint
	•	🔁 Suitable for real-time optimization & energy market applications
	•	🧠 Clean and modular Python implementation

⸻

🧠 Method Overview

The Economic Dispatch (ED) problem aims to minimize total generation cost:

F_T = \sum_{i=1}^{n} (a_i + b_i P_i + c_i P_i^2)

The classical Lambda Iteration Method is enhanced through:
	•	Vectorized operations using NumPy
	•	Parallel computation across generators
	•	Reduced iteration time and faster convergence

This approach significantly improves efficiency while maintaining solution accuracy.

⸻

📊 Key Results

Method	Cost ($/h)	Time (sec)
VLIM	32,183	0.0049
ELIM	32,542	0.123
LIM	32,549	2.556

✅ VLIM achieves:
	•	Faster convergence
	•	Lower operational cost
	•	Significant computational efficiency

⸻

📂 Project Structure

vlim-economic-dispatch/
│
├── src/            # Core implementation
├── notebooks/      # Jupyter experiments
├── data/           # (Not included)
├── docs/           # Paper / documentation
├── requirements.txt
└── README.md


⸻

⚙️ Installation

git clone https://github.com/username/vlim-economic-dispatch.git
cd vlim-economic-dispatch
pip install -r requirements.txt


⸻

▶️ Usage

Run main script:

python src/main.py

Or open notebook:

jupyter notebook notebooks/VLIM.ipynb


⸻

📊 Dataset

⚠️ The dataset used in the original research is not publicly available due to confidentiality restrictions.

However, you can:
	•	Use your own dataset with the same format
	•	Generate synthetic data for testing

Expected Input Format

Each generator should include:

Parameter	Description
a, b, c	Cost coefficients
Pmin	Minimum power output
Pmax	Maximum power output
RampUp	Ramp up limit
RampDown	Ramp down limit

Example (CSV):

a,b,c,Pmin,Pmax,RampUp,RampDown
671.03,10.1,0.000299,150,455,50,50
574.54,10.22,0.000183,150,455,50,50


⸻

▶️ Example (Synthetic Data)

from src.vlim import calculate_power

demand = 2650

a = [671.03, 574.54]
b = [10.1, 10.22]
c = [0.000299, 0.000183]

P = calculate_power(demand, a, b, c)
print(P)


⸻

📌 Reproducibility

This repository focuses on the algorithm implementation.
Exact reproduction of published results requires proprietary datasets.

⸻

📖 Citation

If you use this work, please cite:

@article{ikhsan2024vlim,
  title={Vectorized Lambda Iteration Method for Swift Economic Dispatch Analysis},
  author={Ikhsan, Rifki Rahman Nur and Raharjo, Jangkung and Rahmat, Basuki},
  journal={Evergreen Journal},
  year={2024}
}


⸻

🔗 DOI (Zenodo)

After creating a GitHub release, Zenodo will automatically generate a DOI for this repository.

⸻

📜 License

MIT License

⸻

🙌 Acknowledgements

This work is based on research in power system optimization and economic dispatch.
Special thanks to contributors and supporting institutions.

⸻

⭐ Support

If you find this repository useful:
	•	⭐ Star this repo
	•	🍴 Fork and contribute
	•	📢 Share with the research community

⸻

:::

