# Perl::Critic::Policy::Misc::ProhibitMethodsInStringConcat

A Perl::Critic policy that flags method calls used as operands to the `.` (string concatenation) operator.

When a method returns `undef` inside a concatenation expression, Perl's warning does not indicate which method produced the uninitialized value — it only reports the line number of the concatenation statement. Assigning the method result to a variable first causes Perl to include the variable name in the warning, making debugging trivially easy.

## Installation

    cpanm Perl::Critic::Policy::Misc::ProhibitMethodsInStringConcat

## Usage

Add to your `perlcriticrc`:

    [Misc::ProhibitMethodsInStringConcat]

No configuration parameters are supported.

## License

MIT
