Tags: #
____
If your notebook or python file can't reach the lib while u are 100% that it has been installed on the machine
~~~
import sys
print(sys.path)
!pip3 show tqdm
sys.path.append('/opt/conda/lib/python3.10/site-packages')

~~~
checkout that lib path location is in the sys.path otherwise add them.

____
### Zero-Links

____
### Links