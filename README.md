# README

## **INTRODUCTION**
### *Reason to write*
One of my senior told me that everyone should have a txt file, which you can write anything you learn in it. So this is mine.

But a txt file is so boring, so I make a markdown one, which is suitable for my job. I can show my code here, add pictures or graphs there. I can save reference links too.

### *Main purpose*
* Improve my writing skill.
* Save coding trick so that I don't need to google it everytime.
* Note every tips and tricks, quotes or experiences.
* I can use this as my diary too.

### *How to use*
Try to Ctrl+F a keyword. There's will be a full table of contents as soon as possible.

## **MY EXPERIENCES**
* Best ways to work: SCRUM + KANBAN + POMODORO.
* Write down everything you think.

## **SKILLS, TIPS AND TRICKS**


## **CODING**
### *C/C++*
* Command Line Arguments
```c
int main(int argc, char *argv[]){
    // argc: number of arguments, the name of program is one argument itself
    // argv[]: argv[0] is program name.
}
```
* Convert a hex (32 bits) to float (ABCD): create a float-type-pointer point to that hex number, then read the value.
```c
uint32_t number_in_hex = 0x12345678;
float number_in_float;
void main(){
    number_in_float = *((float*)&number_in_hex);
}
```

### *Python*
* Document link:
    * [Paho MQTT python doc](https://pypi.python.org/pypi/paho-mqtt/1.1)
* Command Line Arguments:
```python
#!/usr/bin/python

import sys, getopt

def main(argv):
   inputfile = ''
   outputfile = ''
   try:
      # Add ':' for options that need argument
      opts, args = getopt.getopt(argv,"hi:o:",["ifile=","ofile="])
   except getopt.GetoptError:
      print 'test.py -i <inputfile> -o <outputfile>'
      sys.exit(2)
   for opt, arg in opts:
      if opt == '-h':
         print 'test.py -i <inputfile> -o <outputfile>'
         sys.exit()
      elif opt in ("-i", "--ifile"):
         inputfile = arg
      elif opt in ("-o", "--ofile"):
         outputfile = arg
   print 'Input file is "', inputfile
   print 'Output file is "', outputfile

if __name__ == "__main__":
   main(sys.argv[1:])
```

### *Git*
* Link to learn about git
    * [Git Beginner's Guide for Dummies](https://backlogtool.com/git-tutorial/en/)
* Most used commands
```bash
# Clone a repo to local
git clone [link]
# Pull from remote to local
git pull [remote_name] [branch_name]
# Add new remote
git remote add [remote_name] [link]
# Switch branch
git checkout [branch_name]
# Create new branch
git branch [branch_name]
# Delete branch
git branch -d [branch_name]
```

### *SVN*
* Most used commands
```bash
# Checkout
svn co [link]
# Add file(s) to track
svn add [file_to_add]
# Commit and push to remote repo
svn commit -m [message_here]
# Update workspace
svn update
```
