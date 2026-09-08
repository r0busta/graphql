# graphql

Fork of `github.com/shurcooL/graphql`, a Go GraphQL client that derives
queries from struct types. Module path `github.com/r0busta/graphql`.

## Layout

- `graphql.go`: `Client`, the `GraphQL` interface, `Query`, `Mutate` and the
  raw `QueryString` / `MutateString` variants.
- `query.go`: builds a query string from a struct via reflection. The fork's
  cycle detection lives here (a stack of visited types via `gods`).
- `scalar.go`: GraphQL scalar type aliases.
- `ident/`, `internal/jsonutil/`: unchanged from upstream.
- `mock/`: gomock mock of `GraphQL`, regenerated with `go generate ./...`.
- `example/graphqldev/`: dev-only program against a local graphql-go server.
  Not part of the library.

## Working here

- `go build ./... && go vet ./... && go test -race ./...` must pass.
- The `go` directive is pinned to match go-shopify-graphql. Do not raise it
  without bumping that repo too.
- Prefer keeping diffs against upstream small so upstream fixes can still be
  ported.
