# wp transient set

Sets a transient value.

`&lt;expiration&gt;` is the time until expiration, in seconds.

For a more complete explanation of the transient cache, including the network|site cache, please see docs for `wp transient`.

### OPTIONS

&lt;key&gt;
: Key for the transient.

&lt;value&gt;
: Value to be set for the transient.

[&lt;expiration&gt;]
: Time until expiration, in seconds.

[\--network]
: Set the value of a network|site transient. On single site, this is is a specially-named cache key. On multisite, this is a global cache (instead of local to the site).

### EXAMPLES

    $ wp transient set sample_key "test data" 3600
    Success: Transient added.

### GLOBAL PARAMETERS

These [global parameters](https://make.wordpress.org/cli/handbook/config/) have the same behavior across all commands and affect how WP-CLI interacts with WordPress.

| **Argument**    | **Description**              |
|:----------------|:-----------------------------|
| `--path=<path>` | Path to the WordPress files. |
| `--url=<url>` | Pretend request came from given URL. In multisite, this argument is how the target site is specified. |
| `--ssh=[<scheme>:][<user>@]<host\|container>[:<port>][<path>]` | Perform operation against a remote server over SSH (or a container using scheme of "docker", "docker-compose", "vagrant"). |
| `--http=<http>` | Perform operation against a remote WordPress install over HTTP. |
| `--user=<id\|login\|email>` | Set the WordPress user. |
| `--skip-plugins[=<plugin>]` | Skip loading all or some plugins. Note: mu-plugins are still loaded. |
| `--skip-themes[=<theme>]` | Skip loading all or some themes. |
| `--skip-packages` | Skip loading all installed packages. |
| `--require=<path>` | Load PHP file before running the command (may be used more than once). |
| `--[no-]color` | Whether to colorize the output. |
| `--debug[=<group>]` | Show all PHP errors; add verbosity to WP-CLI bootstrap. |
| `--prompt[=<assoc>]` | Prompt the user to enter values for all command arguments, or a subset specified as comma-separated values. |
| `--quiet` | Suppress informational messages. |
