# My work on top of the SAGIN toolkit (Qusin, Nablus)

The repository files (agents.py, channel.py, config.py, env.py, trainer.py, baselines.py,
experiment.py, tests.py, README.md ...) are the original toolkit by Lewis-panda and are NOT modified.

My files:
- qusin_scenario.py   villages + clustered layout + first (v1) experiment
- sagin_v2.py         improved model (spot beams, frequency reuse, capacity, directional backhaul),
                      Q-learning training, baselines, experiment runner
- paired_stats.py     30-topology paired comparison with bootstrap CIs
- make_figures_v1.py  figures of the first model        -> results_qusin/figures
- make_figures_v2.py  figures of the improved model     -> results_qusin_v2/figures

Run (Windows cmd, inside this folder, after: pip install -r requirements.txt):
    python tests.py
    python qusin_scenario.py      (~5 min)   then   python make_figures_v1.py
    python sagin_v2.py            (~10-15 min)
    python paired_stats.py        (~10 min)
    python make_figures_v2.py
Add --quick to sagin_v2.py for a short smoke test.

Results already included: results_qusin/ (first model) and results_qusin_v2/ (final).
