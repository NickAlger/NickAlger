---
layout: home
---

<script>
MathJax = {
  tex: { inlineMath: [['$', '$'], ['\\(', '\\)']], displayMath: [['$$', '$$'], ['\\[', '\\]']] }
};
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

Test 4

{{ page.path }}

[Link to puzzle tutorial]({% link /astroknot.md %})

$$\int_\Omega f(x) dx$$

```python
def left_orthogonalize_utt(
        tt_cores:       jnp.ndarray,  # shape=(d, r, n, r)
) -> jnp.ndarray: # new_tt_cores
    d, r, n, _ = tt_cores.shape

    def _orth_one_core(
            prev_R: jnp.ndarray, # shape=(r, r)
            G: jnp.ndarray, # shape=(r, n, r)
    ):
        G = jnp.einsum('ij,jak->iak', prev_R, G)
        # Q, R = jnp.linalg.qr(G.reshape((r*n, r)), mode='reduced')
        Q, ss, Vt = jnp.linalg.svd(G.reshape((r*n, r)), full_matrices=False)
        R = jnp.einsum('i,ij->ij', ss, Vt)

        G = Q.reshape((r, n, r))
        return R, G

    R0 = jnp.eye(r)
    R, first_new_tt_cores = jax.lax.scan(_orth_one_core, R0, tt_cores[:-1])
    last_new_tt_core = jnp.einsum('ij,djak->diak', R, tt_cores[-1:])
    new_tt_cores = jnp.concatenate([first_new_tt_cores, last_new_tt_core], axis=0)
    return new_tt_cores
```
