# Learn Move Language by Small Moves

[Read the full blog post on Medium](https://medium.com/@ashourics/learn-move-language-by-small-moves-e8824e28c464)

## Introduction

The Move programming language is an innovative language for the blockchain ecosystem, originally created by Facebook for the Libra project and later adopted by other blockchain platforms. Move focuses on flexibility, safety, and the ability to define custom assets, making it an excellent choice for developers looking to explore the blockchain space.

In this blog post, I take you through the basics of Move, breaking down key concepts into manageable pieces so you can build your understanding one step at a time. If you're ready to learn by "small moves," check out my detailed blog on Medium linked above.

## What is Move?

Move is a bytecode language with a focus on safety and programmability in the blockchain context. It aims to solve some of the problems present in other blockchain programming languages like Solidity, such as security vulnerabilities and the lack of a resource-oriented approach. In Move, resources are first-class citizens, which is essential for modeling ownership and asset transfers on a blockchain.

## Getting Started with Move

### Prerequisites

To follow along with Move development, you'll need:
- A basic understanding of blockchain technology.
- Familiarity with programming concepts, preferably in Rust or Python.
- Move CLI installed on your system. You can find the installation guide on the [official Move GitHub repository](https://github.com/move-language/move).

### Setting Up

First, let's install Move and create a new project:

```bash
# Clone the Move repository
git clone https://github.com/move-language/move

# Navigate to the directory
cd move

# Build the Move toolchain
cargo build --release
```

After setting up Move, you'll be ready to start experimenting by creating a new module.

## Understanding Modules in Move

Move code is organized into modules, which are like libraries or smart contracts. Each module can define types, functions, and constants. Here's an example of a basic Move module:

```move
module MyFirstModule {
    public fun say_hello(): &str {
        "Hello, Move!"
    }
}
```

In this module, `MyFirstModule` defines a simple public function called `say_hello()` that returns a greeting. Modules are the building blocks of Move programs, containing the core functionality for interacting with blockchain data.

## Working with Resources

A unique aspect of Move is its focus on resources. Resources are types that cannot be duplicated or discarded, making them perfect for representing assets like tokens or NFTs. Here's an example:

```move
module Token {
    resource struct TokenInfo {
        value: u64,
    }

    public fun create_token(value: u64): TokenInfo {
        TokenInfo { value }
    }
}
```

In this module, `Token` defines a resource struct called `TokenInfo`, which can be created using the `create_token()` function. The resource type ensures that instances of `TokenInfo` cannot be accidentally lost or copied, which guarantees safety in the blockchain context.

## Next Steps

If you want to learn more, including how to deploy Move modules and interact with them, check out the full blog post on Medium: [Learn Move Language by Small Moves](https://medium.com/@ashourics/learn-move-language-by-small-moves-e8824e28c464).

I'll be covering advanced concepts in future posts, so stay tuned!

## Conclusion

Move is a powerful language designed to bring safety, expressiveness, and efficiency to blockchain programming. By taking small steps and learning its key features incrementally, developers can effectively use Move to build reliable blockchain applications.

For the complete breakdown and more examples, make sure to visit the blog post on Medium linked above.
