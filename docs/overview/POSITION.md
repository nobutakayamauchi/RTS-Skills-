# RTS Skills Repository Position

## What this repository is

RTS Skills is the workflow and job-unit layer.

This repository defines reusable work units that describe what should be done, what inputs are needed, what outputs are expected, what packs are required, and what should be recorded back into RTS.

A skill is not a raw tool call.
A skill is not a runtime.
A skill is not a connector.

A skill is a job-shaped execution unit.

## Core responsibility

RTS Skills is responsible for:
- defining work units in a reusable format
- describing required inputs and expected outputs
- describing required MCP packs
- defining execution intent at the job level
- defining failure modes and recovery expectations
- defining what records must be returned to RTS

## Non-responsibility

RTS Skills does not:
- directly own MCP authentication or service credentials
- directly act as an always-on orchestration runtime
- directly preserve canonical trust records
- directly define low-level external tool implementations

## Design stance

Skills should be expressed as work, not as isolated tool actions.

Preferred:
- issue_to_fix_pr
- weekly_dev_report
- sentry_error_to_root_cause_report

Avoid centering the model around fragments such as:
- read_issue
- click_button
- list_messages

Tool-level actions may exist internally, but the public skill boundary should remain job-oriented.

## Dependency stance

Skills may depend on:
- RTS schemas and record contracts
- declared MCP packs
- compatible execution drives

Skills should avoid hard-locking themselves to one runtime unless absolutely necessary.

## Expected artifacts

Typical artifacts in this repository include:
- skill definitions
- skill manifests
- input/output schemas
- failure mode notes
- example executions
- compatibility declarations
- workflow documentation
