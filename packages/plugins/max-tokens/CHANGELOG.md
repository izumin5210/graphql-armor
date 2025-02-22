# @escape.tech/graphql-armor-max-tokens

## 1.3.0

### Minor Changes

- 59626ad: feat(docs): dedicated docs site

  fix(dev): install-dev script mookme init

  chore(deps/example): bump
  chore(deps/monorepo): bump linters & tools
  chore(optional-deps/_): envelop v3 support
  chore(optional-deps/_): bump apollo-server to 3.11

## 1.2.0

### Minor Changes

- 3b204b6: refactor(apollo): throwOnRejection #220

  - throwOnRejection became propagateOnRejection.

  - Apollo will now **report to context** by default.
    Errors might be very verbose but this is the best way to handle it until Apollo Server 4 is released.
    If you want to still throw errors, you can use the onReject callback, however, you will need to handle the HTTP 500 afterwards yourself.

## 1.1.1

### Patch Changes

- 542b49d: fix:
  Incorrect @escape.tech/graphql-armor-types dependency

## 1.1.0

### Minor Changes

- c16a2bb: Feat(plugins)/provide-custom-configuration-callbacks

  ```
  {
    onAccept: [],
    onReject: [],
    throwRejection: bool,
  }
  ```

  - Granted the ability to choose whenever you want to throw or not.
  - Introduced callbacks that can be runned before reject the query, for observability purposes.

  - added devDependencies to @escape.tech/graphql-armor-types

## 1.0.2

### Patch Changes

- feaaf34: chore(deps):

  - Drop peerDependencies in favor of optionalDependencies.
  - GraphQL JS has been fixed to v16.6.0 in devDependencies and examples.

## 1.0.1

### Patch Changes

- 6176fd2: ### feat: - Add max-tokens package (@n1ru4l) - Remove character-limit from core - Include limitation message:
  `Syntax Error: ${plugin} limit of ${limit} exceeded, found ${found}.`

  ### chore:

      - Drop `apollo-server` / `@types/node` direct dependencies
      - Tests consistency

  ### repo:

      - Update examples
      - Update renovate config, nopin/nogroup
