# Creation and publication plan

**Personal repository:** [`Bakkej/skills-metadata`](https://github.com/Bakkej/skills-metadata), version `0.1.0`, concept status. The intended Geonovum Labs handoff is a separate step. Personal hosting does not imply Geonovum endorsement.

| Phase | Deliverable and acceptance criteria |
| --- | --- |
| 1. Map the scaffold and companions | Preserve the three plugin manifests, license, publiccode, references, worked example and eval pattern from the MIM scaffold. Verify exact upstream skill names and their read/review scope. |
| 2. Define the reading model | Describe catalog, access, meaning, specification, quality and provenance roles. Retain original predicates, versions and scopes when translating across standards. Define the four MIM-level routing decisions and behavior when a link or companion is missing. |
| 3. Package and exercise | Ship one discoverable `metadata` skill with a small entry point and progressively loaded material. Exercise the read-only workflow on a fictional catalog and test documented, inferred, missing and conflicting evidence. Check manifests, frontmatter, relative links and fixture syntax. |
| 4. Review and publish | A maintainer confirms project ownership and the proposed repository URL, runs the client smoke checks below, adds the release date and maintenance contact if agreed, and publishes from the new repository. |

## Decisions

- **One skill, no forked standards expertise.** Replace the scaffold's copied MIM skills and stubs with a coordinator. Keep example material and evaluation cases, not authoring templates or runtime scripts.
- **Discoverable layout.** Use `skills/metadata/SKILL.md` instead of the copied MIM scaffold's root-level skill directory, preserving the manifest convention while matching the automatic `skills/` layout of the NL-SBB companion.
- **No invented mappings.** Metadata varies by publisher and profile. Classify compatible roles without replacing source predicates, inferring conformance, or calling a full review for a concept lookup.
- **Small first release.** Real publisher cases, additional profile-specific recognition rules and new routes to API and schema interpretation skills should follow evidence from actual catalog use.

## Maintainer release checks

1. Confirm the repository URL, copyright and license metadata, governance and maintenance ownership. `maintenance.type: none` describes the draft until a maintainer is assigned.
2. Load the plugin from a local checkout in the clients being advertised. Confirm `metadata` appears exactly once. In VS Code, also try direct skill-folder installation.
3. Run the [eval cases](../skills/metadata/evals/README.md) with no companions installed and then with the relevant companion(s). Check that read-only questions do not trigger publication, editing or unrequested validation. Test with a publisher-owned, shareable real catalog before promoting the skill out of concept status.
4. Create the empty GitHub repository under the target organization, review and commit this directory, push it, and tag the release once packaging and review are accepted. Do not copy the MIM project's repository history or publish the fixture as real catalog metadata.
