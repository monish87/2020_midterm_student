# 2020_midterm_student


To run these tests on your notebook:

```
files = "https://github.com/rpi-techfundamentals/2020_midterm_student/blob/master/tests.zip" 
!pip install git+https://github.com/carmelabs/Gofer-Grader && wget $files && unzip -o files.zip
```

Then later to test:

```
#Please run this at end to show that all tests were passed. 
import os
from client.api.notebook import Notebook
ok = Notebook('hm.ok')
_ = ok.auth(inline=True)
_ = [ok.grade(q[:-3]) for q in os.listdir("tests") if q.startswith('q')]
```


Or you can just manually look at the expected answer for the questions you missed.  
