# The complexity of a system is relative to a specific goal and time
Sources of complexity are not always relevant, and hidden complexity can be nearly as good as it not being there. 

Consider the simplicity of an OS's basic file I/O interface compared to the entire infrastructure of caches, filesystems, and disk drivers below it. As long as your goal does not require you to know or think about those details, you can use the file I/O API without the mental burden of knowing or keeping those details in mind.

This means [[The overall complexity of a system is based on common activities]].


### Sources
* [[A Philosophy of Software Design]]