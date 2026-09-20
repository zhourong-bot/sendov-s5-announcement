# Sendov Lemma 4.12: five-centre branch — proof announcement

## 中文说明

我们已完成 Sendov 引理 4.12 的五中心情形（`E.s = 5`）在本项目明确列出的前提下的 Lean 证明。三个几何分支及其覆盖分类已通过本地 Lean 验收。证明源码暂时保存在私有仓库中，本仓库仅公开成果范围和版本存证信息。

这里的“五中心”指广义配置的五个秩一圆心，不是普通点集只有五个点。

**已完成范围：**凸包为五顶点、四顶点加一个内点、三顶点加两个内点的三个分支，以及覆盖它们的凸包分类。归档验收记录中，这四个定理的公理依赖仅为 Lean 标准的 `propext`、`Classical.choice`、`Quot.sound`，没有 `sorryAx`。

**明确前提与待核验事项：**证明使用正参数 `u > 0`，并显式要求 `NoEmptyPrimitiveCircle`（每个原始圆有对应点）和 `CrossDirectionsIndependent`（子圆心连线方向不与子配置已有方向重合），以及各分支定理列出的几何、计数条件。与论文原始表述的前提对应关系、相关归约的完整性仍待进一步核验。

本公告不声称整个引理的一般中心数情形、JSP-000404 或 Erdős #504 已解决，也不声称已经确认全球首次证明。原创性和优先权仍需结合公开文献及其他成果审查。

## English statement

We have completed a Lean proof of the five-centre branch (`E.s = 5`) associated with Sendov's Lemma 4.12, under the explicit hypotheses of our formalization. The proof source is currently private. This repository publishes only the scope of the result and an archival version commitment.

The three geometric cases are a convex pentagon, four hull vertices with one interior point, and three hull vertices with two interior points. The archived local checks cover:

- `b4s5_penta_case_final`
- `b4s5_g41_case_final`
- `b4s5_g32_case_final`
- `b4s5_hull_trichotomy`

The recorded `#print axioms` checks report only `propext`, `Classical.choice`, and `Quot.sound`, with no `sorryAx`. A fresh full-file compilation also returned exit code 0. These are local verification records; the private source is not yet available for public reproduction.

The formalization explicitly assumes `u > 0`, `NoEmptyPrimitiveCircle`, and `CrossDirectionsIndependent`, together with the geometric and counting hypotheses in the case theorems. The correspondence with the original paper's hypotheses and the completeness of the relevant reductions remain under review. Lean acceptance establishes the encoded statements under their hypotheses; it does not by itself settle that correspondence.

This announcement does not claim the unrestricted general-centre lemma, a complete solution of JSP-000404 / Erdős #504, or established worldwide priority.

## Archived version and time evidence

- Source repository (private): https://github.com/zhourong-bot/blumenthal-sendov-lean
- Archived Git commit SHA:
  `633a945bea066b43511dd6a2d297c4f989e7d8fe`
- SHA-256 of the 15-file snapshot hash manifest:
  `e7f3a4a7c8b84bfc491d9c1981d7d0c66000cd2528db5d60f2bc1f6d548165df`
- Recorded GitHub server push time: **2026-09-20 15:39:38 UTC** / **2026-09-20 23:39:38 Asia/Shanghai**.
- Recorded GitHub push event: `21665454153`, at **2026-09-20 15:39:39 UTC**.
- OpenTimestamps: a receipt for the manifest was saved. Its status was **pending** in the archival record; this announcement does not claim a verified Bitcoin anchor.

The earlier push was to a private repository. It is not presented as the public announcement date. Git author/committer dates are self-supplied and are not used here as independent time evidence. Hashes identify the committed version; hashes alone establish neither mathematical correctness nor historical priority.

The source, manifest contents, and proof details remain private pending further review. This announcement makes no claim of independent public replication.

## Reference and attribution

Blagovest Sendov, *Compulsory configurations of points in the plane*, Fundam. Prikl. Mat. 1:2 (1995), 491–516, Lemma 4.12: https://www.mathnet.ru/eng/fpm81

This work follows Sendov's framework and was developed with AI assistance. The announced contribution is limited to the scoped five-centre proof described above.
