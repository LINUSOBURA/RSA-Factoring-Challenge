#!/usr/bin/python3

import sys


def factorize_number(n):
    for i in range(2, n):
        if n % i == 0:
            return i, n // i
    return None, None


def factorize_file(file_path):
    with open(file_path, "r") as file:
        numbers = [int(line.strip()) for line in file]

    factorizations = []
    for num in numbers:
        p, q = factorize_number(num)
        if p is not None and q is not None:
            factorizations.append(f"{num}={p}*{q}")

    return factorizations


def main():
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
        sys.exit(1)

    file_path = sys.argv[1]
    factorizations = factorize_file(file_path)

    for factorization in factorizations:
        print(factorization)


if __name__ == "__main__":
    main()
