#MEAN Session One

##Assignment

Download, install and configure Sublime Text on your personal computer. Download Koala. Unzip and review the files. Add the remaining SCSS files to styles.scss (watch out for that pesky error I mentioned - see the bottom of this readme for an explanation). Ensure that you understand and can use Koala’s SASS preprocessing. You may use your own files or download version1 branch from this repo.

[Purchase the text book](http://www.amazon.com/gp/product/1491901942/ref=as_li_tl?ie=UTF8&amp;camp=1789&amp;creative=9325&amp;creativeASIN=1491901942&amp;linkCode=as2&amp;tag=hcj08-20&amp;linkId=PHEBREMNY64ZHLSH).

Review the [Git tutorial](http://try.github.com/)

##Tools of the trade

In this class we will be using Sublime Text, Git, Github, the Terminal, and Koala. 

Sublime text is available free for Mac and PC and is widely regarded as one of the best text editing applications - due primarily to its extensibility. For our purposes we will begin with a few of its more useful utilities – [Package Control](https://packagecontrol.io) and [Emmet](https://github.com/sergeche/emmet-sublime#readme).

The terminal is a command line interface (CLI) that allows you to issue commands without using a GUI. In this class we used it to navigate the file structure, to work with Git, and to start a local web server.

Github is a distributed version control system and is used to distribute files to the class. Class members will need to create a free Github account in order to use this system. You will also need to download and install Git on your home computer.

Koala is an application that runs on Mac and PC. It monitors a collection of files (usually your site folder) and transforms SASS into browser friendly CSS. It performs a number of JavaScript related functions which we will examine as the semester progresses. One feature we will be relying on is the ability to create .map files. An alternative to using Koala is Grunt which we will consider it in a future session.

Because files and applications are not permanently stored on the NYU lab computers it is recommended that you bring your own laptop to class for sessions.

##Objectives

Understand the basic principles of semantic HTML and the evolution of web development by updating a table-based layout to a standards-based layout. This session will cover:

* Basic Terminal use: ls, cd, and starting a Python server  ```$python -m SimpleHTTPServer```
* The Chrome Web Developer tool
* [Package control](https://packagecontrol.io/) and [Emmet](http://emmet.io/) for [Sublime Text](http://www.sublimetext.com/)
* Installing and using [SASS](http://sass-lang.com/)
* Essential HTML and the anatomy of CSS

NOTE

When you paste in content.scss you will get an error because there is a missing } character in the bottom of that file. You can add this in to prevent the error however the next file, 12-portfolio-image.scss needs to go *inside* the content.scss block. You should review SASS nesting.

Here is how the bottom portion of styles.scss should look when properly nested.
```
                &:before {
                    content: "";
                    position: absolute;
                    width: 11px;
                    height: 11px;
                    border-radius: 50%;
                    border: 2px solid $gray;
                    background: $strawberry;
                    left: -29px;
                    top: 3px;
                }
            }

        }
    // inside content styles at end
    .portfolio-image {
        padding: $padding*2;
        background: $white;
        border-left: 1px solid darken($gray, 10%);
        text-align: center;

        @media screen and (min-width: $break-three) {
            float: left;
            width: 70%;
        }

        img {
            width: 100%;
            max-width: 610px;
            height: auto;
        }

        div.loading {
            img {
                width: auto;
                height: auto;
            }
        }
    }
}
}
```
