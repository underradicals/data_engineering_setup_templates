# dbt-core Setup

## Just the facts Ma'am

### Setting up Python Environment

```bash
uv init;
uv venv .venv;
```

Next you need to activate your virtual environment

#### `Windows`

```powershell
./.venv/Scripts/activate
```

#### `Mac OS`

```bash
source ./.venv/bin/activate
```

### Installing `dbt-core`

```bash
uv add dbt-core;
uv add dbt-postgres;
```

You can choose whatever adapter you wish here. We chose `dbt-postgres` here, but you can just as well have used `dbt-snowflake`. For more information on adapters checkout.

After installing `dbt-core` you will have access to the `dbt` cli command inside your virtual environment.

### Initializing dbt project

```bash
dbt init;
```

### Validate Your Configuration

This should just work, unless you have made some changes to the repo.

```bash
dbt debug
```

### Using the starter project

Try running the following commands:

- dbt run
- dbt test

### Check out the docs

```bash
dbt docs generate
dbt docs serve
```

### Resources:

- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [chat](https://community.getdbt.com/) on Slack for live discussions and support
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices
