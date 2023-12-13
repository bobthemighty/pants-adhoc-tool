python_sources()

pex_binary(
    name="code", include_requirements=False, dependencies=["src/job/do_a_job.py"]
)

adhoc_tool(
    name="repackage",
    runnable="src/util/package.py",
    execution_dependencies=["src/job:code"]
)

run_shell_command(
    name="export",
    execution_dependencies=[":repackage"],
    command="ls"
)
