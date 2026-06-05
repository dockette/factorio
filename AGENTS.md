# AGENTS.md

## Project

Dockette Factorio is a legacy Docker/game repository for running the Factorio desktop client through Docker and X11. Treat it as a historical mirror unless maintainers explicitly decide to revive or archive it.

## Repository Status

- The repository contains old Dockerfiles for Factorio `0.12.x`, a base image, a sources image, and the `bin/run` X11 launcher.
- Current scripts reference the legacy `dockergames/factorio` image namespace.
- Do not add a Docker Hub pulls badge for `dockette/factorio`; no active `dockette/factorio` image is published for new users.
- Prefer documentation-only changes over CI rollout changes unless maintainers confirm the image should be actively rebuilt.

## Validation

- Run `git diff --check` after edits.
- If a Makefile or workflow is introduced later, keep it minimal and verify `make -n build test run`.
- Keep `CLAUDE.md` exactly `@AGENTS.md`.

## Guidelines

- Preserve the legacy Dockerfiles and launcher behavior unless the task explicitly revives the image.
- Keep README badges limited to applicable Dockette badges; do not add Slack, Gitter, or Docker pulls badges for this archived/legacy image.
- Keep the Maintenance section aligned with the standard Dockette wording.
- Document deprecated or superseded behavior clearly rather than implying current support.
