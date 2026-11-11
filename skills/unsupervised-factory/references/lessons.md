# Unsupervised-method lessons

The [retrospective diagnostic replay](https://github.com/shreyan2020/research-factory/blob/main/TESTING.md) found that a raw metric included zero-feature rows before a conservative override. Calling it a score conditional on representable rows would have been wrong. Saved diagnostics lacked the denominators needed to calculate coverage.

Trace preprocessing, fitting, scoring, aggregation, and overrides to the actual implementation. Report the raw score, evaluated population, exclusions, and override separately. Do not recover an unrecorded denominator by assumption.

Other transferable lessons:

- Adding documents should preserve units and settings for the requested comparable rerun. A redesign is a separate experiment.
- Repairing extraction may leave mixed clusters mixed. Reevaluate the downstream result.
- A fixed gate can fail because of weak raw structure as well as an override. Removing the override does not establish success.
- Source roles, document families, and dates can drive apparent structure. Inspect confounds before interpreting themes.
- A source review can find semantic errors after software tests pass. Same-model review is not independent human validation.
- Repeated failed repairs can indicate unsuitable units, overlapping concepts, or no useful partition. Test the shared premise before adding complexity.
- Retrieval or an evidence index may be useful even when stable clusters do not emerge.
- Historical compute locations and thresholds are project-specific records, not authorization or universal settings.

Saved-result reconstruction is not a new model run. Keep proposed experiments explicitly proposed in findings memos and slides.
