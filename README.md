<!--
SPDX-FileCopyrightText: 2023 Slavi Pantaleev
SPDX-FileCopyrightText: 2025, 2026 Suguru Hirahara

SPDX-License-Identifier: AGPL-3.0-or-later
-->

# Meilisearch Ansible role

This is an [Ansible](https://www.ansible.com/) role which installs [Meilisearch](https://www.meilisearch.com) to run as a [Docker](https://www.docker.com/) container wrapped in a systemd service.

This role *implicitly* depends on:

- [`playbook_help-ar`](https://github.com/P3X-118/playbook_help-ar)
- [`systemd_docker_base-ar`](https://github.com/P3X-118/systemd_docker_base-ar)

Check [`defaults/main.yml`](defaults/main.yml) for the full list of supported options. Refer to [this page](docs/configuring-meilisearch.md) for details about setting up the service with this role.

💡 For an Ansible playbook which integrates this role and makes it easier to use, see the [Mother-of-All-Self-Hosting Ansible playbook](https://github.com/mother-of-all-self-hosting/mash-playbook).

>[!NOTE]
> Please note that the `v1.28.0` has introduced the "pro" and "peasant" editions separation:
>
> "This release introduces improvements to language support and separates the community and enterprise binary editions. We now offer binaries [under the BUSL-1.1 license](https://redirect.github.com/meilisearch/meilisearch/blob/main/LICENSE-EE), identified by the "enterprise" term in their names, in addition to our MIT-licensed binaries, which retain their original names. Docker images for the enterprise edition are available in the [`getmeili/meilisearch-enterprise`](https://hub.docker.com/r/getmeili/meilisearch-enterprise/tags) repository."
>
> See: <https://github.com/mother-of-all-self-hosting/ansible-role-meilisearch/pull/8>

## Development

You can optionally install [pre-commit](https://pre-commit.com/) so that simple mistakes are checked and noticed before changes are pushed to a remote branch. See [`.pre-commit-config.yaml`](./.pre-commit-config.yaml) for which hooks are to be executed.

See [this section](https://pre-commit.com/#usage) on the official documentation for usage.
