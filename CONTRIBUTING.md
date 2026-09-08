# Contributing

This package is a fork of [shurcooL/graphql](https://github.com/shurcooL/graphql)
kept mainly to serve [go-shopify-graphql](https://github.com/r0busta/go-shopify-graphql).
Pull requests are welcome, with a few notes:

- Run `gofmt`, `go vet ./...` and `go test -race ./...`. CI runs the same.
- Keep the module path as `github.com/r0busta/graphql`.
- Changes to the `GraphQL` interface need the mock regenerated with
  `go generate ./...` (requires `mockgen`).
- Behaviour that is generic GraphQL client work may be better sent upstream
  to shurcooL/graphql first. This fork tracks upstream loosely.
- Bumping the `go` directive affects go-shopify-graphql, which pins the same
  Go version. Coordinate the two.
