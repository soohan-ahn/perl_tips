# PERL TIPS
Tips for coding Perl based on the comment from the pull requests.

[MUST] 4-column indent without the hard tab.

[MUST] The method name starts with ' _ ' is private method.

[SHOULD] 'use Mouse' is for the object package. Should not use for package of module.

[SHOULD] For array slice of hash member, use reference.
ex)

<pre>
  @{$mime}[0] => $mime->[0]
</pre>

[SHOULD] Should not use 'my $a', 'my $b'.

[SHOULD] Single letter variable names should never be used unless for a loop iterator.

[SHOULD] There should be a space between every control/loop keyword and the opening parenthesis.

[SHOULD] There should be a space between every closing parenthesis and the opening curly bracket.

[SHOULD] 'else' & 'elsif' statements should be on a separate line after the previous closing curly brace.

[SHOULD] Check the empty string by '[if|unless] length $variable'. To avoid case '0'.
<pre>
$var = "0";
length $var -> true
$var -> false
</pre>

[MUST] If checking the variable is null or not, use 'defined $variable'. This is needed to avoid the case of value 0.

[MUST] If using NOW(), and want to get data type by datetime not string, use '/NOW()'.

[OPTIONAL] Iterating the loop for hash reference using each has no order. Extract list would me much better.

[OPTIONAL] use 'can' if you need that the method has been called or not.

[SHOULD] Write the code below if you declared 'use Mouse'.
<pre>
no Mouse; __PACKAGE__->meta->make _ immutable;
</pre>

