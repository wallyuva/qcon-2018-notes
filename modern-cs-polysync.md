# Git Gud with Property-Based Testing

## Speakers

Katie Cleary

### Notes

- Quick Check - type based (jsverify for js/ts)
- Proptest (Rust) - hypothesis style testing - proptest stores failed tests in a file and uses the values to generate new tests for regressions

### Git

- Metadata could be tampered with, which changes history (eg exclude packages)

### Property Based Tests

- Concentrated - more tests for free (lots of cases out of the box)
- Shrinking - when a property based test finds a failing case, it finds the smallest possible failing case through iteration
- Comprehensive - generators create random values (can compose generators for complex objects)
- Constructive - you can learn a lot from them, different train of thought