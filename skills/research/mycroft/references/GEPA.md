# GEPA — Measured instruction optimization

GEPA means Genetic-Pareto. Use its experiment sequence for explicitly requested measured optimization of executable investigation/program instructions. Native tools can enact it; an existing qualified library is optional.

## Freeze and qualify

Record seed instructions, editable components, feedback cases, fixed validation/selection cases, scorer, model/tool/source conditions and evaluation allowance. Keep source access, acceptance contracts and work controls outside editable components. Establish permitted case use and execution before evaluation.

A scorer uses executable expected-answer checks, a documented human rubric or a qualified model judge. For a generalization claim, reserve a separate final test outside mutation and selection; this additional boundary is the skill's evaluation policy.

**Ready:** Representative cases, a defined scorer, usable execution and a finite allowance are established. Otherwise give useful ordinary refinement within scope and report the unmet measured criterion. A rewrite or defect packet alone supplies no measured improvement.

## Execute

1. **Measure the seed:** Execute actual cases and retain outputs, observable diagnostic feedback and per-case validation scores.
2. **Select a parent:** Form per-instance best sets, including ties. Take their union, remove dominated candidates and sample a survivor proportional to its membership in surviving best sets. Record the calculation and sampled choice.
3. **Reflect and mutate:** Choose an editable component and feedback minibatch. Execute the parent and use its failures/scorer feedback to propose one targeted instruction change linked to that parent.
4. **Compare:** Declare the admission rule, then execute parent/child on the same minibatch under fixed conditions. The minimal rule requires a strictly higher aggregate child score; admit only on measured results.
5. **Update:** Evaluate admitted candidates on fixed validation cases and update scores, frontier and ancestry.
6. **Repeat and select:** Stop at the frozen allowance/criterion and select the best aggregate validation candidate. System-aware crossover is optional.
7. **Test and review:** Run any reserved final test; report baseline/candidate comparison and limits, including equality or regression. Apply or return the candidate within the user's authorized scope.

Call native execution an **agent-executed GEPA procedure**. Record algorithmic deviations such as always selecting the best average or using a different admission rule; distinguish it from an actual official-library invocation.

**Experiment complete:** Selected instructions, ancestry, actual case outputs/scores, selection/admission decisions and the baseline comparison are available. Required unexecuted evaluation leaves the result partial.

## Records and reuse

Keep candidate text, parent IDs, per-case scores, diagnostic feedback, source/case versions, selection decisions and observed work in the project's experiment location. Real critique defects can supply feedback; retain only the context needed for the case.

Freeze selected instructions per experiment. Experimental lessons and exact executable instructions are separate artifacts. Promote a candidate into standing guidance only within explicit authorization; logging a lesson supplies no such promotion.

## Primary evidence

[GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning, v1](https://arxiv.org/html/2507.19457v1), §3.1–3.3/Algorithms 1–2 and §4.3, supports measured mutation, matched-batch admission, instance-wise selection, membership-weighted sampling, bounded rollouts and feedback/validation splits.

Instruction-only scope, protected controls, project records and separate final-test/review policy are this skill's adaptations. Paper results do not establish improvement for this skill without its own matched evaluation.
