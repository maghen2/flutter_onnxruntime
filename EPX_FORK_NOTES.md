# Fork e-PhotoID Express

Miroir interne verrouillé de https://github.com/masicai/flutter_onnxruntime,
créé le 01/09/2026 dans le cadre d'AI-BG-005 (`doc/ADR-013-detourage-local-onnx-v2.md`
§2.3, dépôt `e_photo_id_express`).

- Base : commit `70ba698eed753261c34cbb4c43cf4990b4c79b38` (tag `v1.8.3`
  amont), verrouillé — jamais rebasé silencieusement sur `masicai/main`.
- Branche `epx-pinned-1.8.3` : identique à la release amont, plus un seul
  correctif : `windows/CMakeLists.txt` vérifie désormais le SHA256 du
  binaire ONNX Runtime téléchargé (`EXPECTED_HASH`), absent en amont.
  Détail complet : `doc/known_bugs.md` bug 25 et
  `doc/p1_ai_bg_005_supply_chain_report.md` du dépôt applicatif.
- `pubspec.yaml` du dépôt applicatif pointe ici via une dépendance `git:`
  épinglée sur un commit précis de cette branche, jamais sur `main`.

Procédure de mise à jour : voir §5 de `doc/p1_ai_bg_005_supply_chain_report.md`.
