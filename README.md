# option-parser-rb
A simple command line option parser

option-parser-rb has two components

option-parser method and option-config hash

Structure of option-config hash

{

  :set_option => {

     :full_option => 'set',

     :short_option => 's',

     :arg_length => 1,

     :arg_type => 'int',

     :usage => 'some string explaining the usage',
     
     :callback_method => 'set_method'
  }
  
}

option-parser needs to be called with this option hash and the command line arguments stored in ARGS

For example - 

program_name --set 3

program_name -s 3

Option parser will be able to parse the above two command line invocation and on getting correct argument 

format will call 'set_method' with one integer argument whose value is 3


option-parser also provides a --help/-h option which prints the usage in followiing format

Usage :

--set/-s - Takes 1 integer type argument and some string explaining the usage














