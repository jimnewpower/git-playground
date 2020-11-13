# git-playground
Demonstration of git functionality

### *Create new file on main (GitPlayground.java)*:
```
    public class GitPlayground {
        public static void main(String[] args) {
          System.out.println("Hello Git");
        }
    }

    $ git status

    On branch main
    Your branch is up to date with 'origin/main'.

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
	          GitPlayground.java

    $ git commit -a -m "main1: Add GitPlayground"

    [main 7a4d362] main1: Add GitPlayground
    1 file changed, 5 insertions(+)
    create mode 100644 GitPlayground.java

    $ git push

    ...
    To github.com:jimnewpower/git-playground.git
    054ea97..7a4d362  main -> main
```

### *Create and switch to new branch*:
```
    $ git checkout -b branch-1
```
- *add branch1() method*:
```
    public class GitPlayground {
        public static void main(String[] args) {
          System.out.println("Hello Git");
        }

        public void branch1() {
          // method added in branch-1
        }
    }

```
- *commit branch1() method*:
```
    $ git commit -a -m "branch-1: Add branch1()"

```
- *add branch1 instance variable*:
```
    public class GitPlayground {
        public static void main(String[] args) {
          System.out.println("Hello Git");
        }

        private long branch1 = 0L;

        public void branch1() {
          // method added in branch-1
        }
    }
```

- *commit branch1 instance variable*:
```
    $ git commit -a -m "branch-1: Add branch1 instance variable"
```

- *switch from branch-1 back to main*:
```
    $ git switch main
```

- *rebase branch-1 to main*:
```
    $ git rebase branch-1
```
