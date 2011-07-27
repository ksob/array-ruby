array ruby
==========

Create
=======

 	first_arr = []
 	secnd_arr = [5,7,-11,"some_string",:some_symbol]
 	third_arr = [:some_symbol,[:other_symbol,"some_string"],[],123]

Access
=======

 	$> first_arr[0]
 	 => nil 
 	$> first_arr[1457]
 	 => nil 
 	$> secnd_arr[3]
 	 => "some_string" 
	$> secnd_arr[184]
	 => nil 
	$> third_arr[0]
	 => :some_symbol 
	$> third_arr[1]
	 => [:other_symbol, "some_string"] 
	$> third_arr[1][0]
	 => :other_symbol 
	$> third_arr[-1]	  # access last element
	 => 123 
	$> third_arr[-2]
 	 => [] 

Modify
=======

 	$> third_arr[1][0] = "whatever"
 	 => "whatever" 

Real world usage
=======
 
 	some_function(secnd_arr).other_function{|x| x.kind == :some_symbol}.map{|x| x.is_a?(Numeric)}

Warning!
=======

 The [] is not only used in arrays but also in hashes to access hash elements:
  
 	some_hash = {:elem1 => 123, :elem2 => "xyz"}
 	$> some_hash[:elem2]
 	 => "xyz"