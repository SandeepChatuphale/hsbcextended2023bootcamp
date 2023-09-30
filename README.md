# hsbcetendedbootcamp
VALID COMBINATIONS
	
	try{}
	catch(Exception e){}
-----------------------------------------------------
	try{}
	catch(RuntimeException e){}
	catch(Exception e){}
-----------------------------------------------------
	try{}
	catch(RuntimeException e){}
	catch(Exception e){}
	finally{}
------------------------------------------------------
	try{}
	catch(NullpointerException | SQLException e){}		//this is multicatch feature added in 1.7
	catch(Exception e){}
	finally{}
-----------------------------------------------------
	try{}
	finally{}
-----------------------------------------------------
	try{}
	finally{}
--------------------------------------------------------
	try{
		try{}
		finally{}
	}
	catch(RuntimeException e){}
	catch(Exception e){}
	finally{}
------------------------------------------------------------

	try{
		try{}
		finally{}
	}
	catch(RuntimeException e){}
	catch(Exception e){}
	finally{
		try{}
		catch(Exception e){}	
	}
----------------------------------------------------------------
	try()				this is valid and called as "try-with-resources" (ARM - Automatic Resource Management) added in jdk 1.7
	{				any resource in "try-with-resources" (ARM) MUST implements AutoClosable interface
	}
	catch(Exception e){}
----------------------------------------------------------------
	try(){
	}
=====================================================
INVALID COMBINATIONS

	try{}
-----------------------------------------------------
	try{}
	catch(Exception e){}			//Generic Exception MUST be last
	catch(RuntimeException e){}
-----------------------------------------------------
	try{}
	catch(RuntimeException e){}
	finally{}
	catch(Exception e){}
-----------------------------------------------------
	catch(Exception e){}
	finally{}
-----------------------------------------------------
	try{}
	int i = 10;
	finally{}

