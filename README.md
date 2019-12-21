
Cosbench = Codebase + QAset + Metrics

# Codebase
We provided two versions of our Codebase.

## origin version
The Codebase could be downloaded from [google drive](https://drive.google.com/file/d/1ADAP8-04o_EA-HOvQPwucudtufexLan5/view?usp=sharing)

This .tar.gz package contains 4,199,769 java snippets which are not processed.
It is in TXT format, one code snippet per line.

## processed version
The Codebase could be downloaded from [google drive](https://drive.google.com/file/d/1I5gimDYK7WaiGbSGnBO9jwT3txR1dHlY/view?usp=sharing)

This .tar.gz package contains 4,199,769 java snippets which are processed.
It is in Json format. Each code snippet corresponds to：

```
[   
    {
        "methbody" : "xxx",
        "apiseq"   : "xxx",
        "tokens"   : "xxx",
        "methname" : "xxx",
        "id"       : "xxx"
    },
    ...
]
```

where `methbody` represents the field that stores the body of source code snippet (using 'method' as minimum storage unit), `apiseq` contains the API sequence that appear in the code, `methname` refers to the method name of the source code, `id` indicates the globally unique id(UUID) for each code snippet.

# QAset
The QAset could be downloaded from [google drive](https://drive.google.com/open?id=1mRbYWq-JjPMyh4-x-GSuJtfVgXk5ftRo)

This Json file contains 52 queries and corresponding answers.
Each QA item corresponds to：


```
[ 
    {
        "id"            :"xxx",
        "query"         :"xxx",
        "intention"     :"xxx",
        "representation":"xxx",
        "answerList"    :["xxx","xxx"...]
    },
    ...
]
```

where "id" is the query ID, "query" is the query content, "answerList" is a array which contains the id of snippet answer. 

In addition, we also provide a supplemental QAset, which contains 62 queries and corresponding answers. The QAset could be downloaded from [google drive](https://drive.google.com/file/d/1gcVVoHnH0bYMzUf4HDJ9Rl3KeRcaffMy/view?usp=sharing)

# Metrics
CosBench takes four metrics: Precision@k, MAP@k, MRR@k, and Frank.

The evaluation code could be found at this [code link](https://github.com/BASE-LAB-SJTU/CSES_IR/tree/master/src/main/java/CS/evaluation).

# Methods
We reproduced 6 code search methods. They can be classified into two mainstreams: IR (Information Retrieval)-
based methods and DL (Deep Learning)-based ones. The project reproduced IR-based methods could be seen in [there](https://github.com/BASE-LAB-SJTU/CSES_IR),  and the project reproduced DL-based methods could be seen in [there](https://github.com/BASE-LAB-SJTU/CSES_ML).

# Evaluation
We performed experiments on Cosbench using the above method, and the details are published in the paper"Are the Code Snippets What We Are Searching for? A Benchmark and an Empirical Study on Code Search with Natural-Language Queries". 

We provide [experimental logs](https://drive.google.com/open?id=1dNEU2RNUujKPKzL-g9AkvQTzqJZWEWJW) and [experimental raw data](https://drive.google.com/open?id=1Gi-JQauyu-pTSrks7fAhA-XJV3DEcXBZ).

