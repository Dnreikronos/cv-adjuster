# Gotchas

## CV PDF filename
- Always deliver compiled CV as `joao_soares_curriculum_vitae.pdf`. Never `cv_output.pdf`.
- Tectonic ignores `--outfile`. Compile then rename:
  `tectonic cv_output.tex && mv cv_output.pdf joao_soares_curriculum_vitae.pdf`
