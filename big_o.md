## Computational Model

**Definition (Word RAM Model)** - the *Word RAM* model is the computation model in which for an algorithm run on an input of size *n*,

- The memory of the algorithm is broken up into *word* of length *w* (typically, *w* = <img src="/tex/6cc1155582330ef46206a2a7064783e5.svg?invert_in_darkmode&sanitize=true" align=middle width=48.451355699999986pt height=24.65753399999998pt/>), and
- Any elementary operation (read, write, add, multiply, AND, etc.) on any single word in memory takes 1 time step

## Asymptotic Analysis

**Definition (Worst-Case Time Complexity)** - the *worst-case time complexity* of an algorithm <img src="/tex/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode&sanitize=true" align=middle width=12.32879834999999pt height=22.465723500000017pt/> is the function <img src="/tex/e3bfae2e8edbd0e152bfabc594408856.svg?invert_in_darkmode&sanitize=true" align=middle width=55.93048724999999pt height=22.465723500000017pt/> obtained by letting <img src="/tex/bb6d2b867b8c52df53b065e8af5f8f24.svg?invert_in_darkmode&sanitize=true" align=middle width=42.96630359999999pt height=24.65753399999998pt/> be the maximum time complexity of <img src="/tex/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode&sanitize=true" align=middle width=12.32879834999999pt height=22.465723500000017pt/> over any input of size <img src="/tex/55a049b8f161ae7cfeb0197d75aff967.svg?invert_in_darkmode&sanitize=true" align=middle width=9.86687624999999pt height=14.15524440000002pt/>.

We care about the **asymptotic** rate of growth as the inputs get larger.

**Definition (Big-O Notation)** - two functions <img src="/tex/6a169b25f34099963b540687ac3b8099.svg?invert_in_darkmode&sanitize=true" align=middle width=77.08347074999999pt height=27.705869399999983pt/> satisfy <img src="/tex/479c556e575352c056cf0dffe5f6c60b.svg?invert_in_darkmode&sanitize=true" align=middle width=65.94625949999998pt height=24.65753399999998pt/> if **there exist** <img src="/tex/03d7460c644e1cc4a5d517935eabb009.svg?invert_in_darkmode&sanitize=true" align=middle width=32.73021674999999pt height=26.17730939999998pt/> and <img src="/tex/f70e5e79cf3bd2b74cda3e84349d4352.svg?invert_in_darkmode&sanitize=true" align=middle width=32.70241424999999pt height=17.723762100000005pt/> such that for every <img src="/tex/c4ecbc7ceca0db57604d584691ddce48.svg?invert_in_darkmode&sanitize=true" align=middle width=48.13998584999999pt height=20.908638300000003pt/>, we have <img src="/tex/f81d90c107511fe957afbe36cbb4ddd4.svg?invert_in_darkmode&sanitize=true" align=middle width=92.58382484999998pt height=24.65753399999998pt/>.

Big-O gives the asymptotic upper bound.

**Definition (Big-<img src="/tex/9432d83304c1eb0dcb05f092d30a767f.svg?invert_in_darkmode&sanitize=true" align=middle width=11.87217899999999pt height=22.465723500000017pt/> Notation)** - two functions <img src="/tex/6a169b25f34099963b540687ac3b8099.svg?invert_in_darkmode&sanitize=true" align=middle width=77.08347074999999pt height=27.705869399999983pt/> satisfy <img src="/tex/a4d1070e1a63094841feb697a19008cd.svg?invert_in_darkmode&sanitize=true" align=middle width=64.82301374999999pt height=24.65753399999998pt/> if **there exist** <img src="/tex/03d7460c644e1cc4a5d517935eabb009.svg?invert_in_darkmode&sanitize=true" align=middle width=32.73021674999999pt height=26.17730939999998pt/> and <img src="/tex/f70e5e79cf3bd2b74cda3e84349d4352.svg?invert_in_darkmode&sanitize=true" align=middle width=32.70241424999999pt height=17.723762100000005pt/> such that for every <img src="/tex/c4ecbc7ceca0db57604d584691ddce48.svg?invert_in_darkmode&sanitize=true" align=middle width=48.13998584999999pt height=20.908638300000003pt/>, we have <img src="/tex/508c5be010fe585c9a5138a742b8a14b.svg?invert_in_darkmode&sanitize=true" align=middle width=92.58382484999998pt height=24.65753399999998pt/>.

Big-<img src="/tex/9432d83304c1eb0dcb05f092d30a767f.svg?invert_in_darkmode&sanitize=true" align=middle width=11.87217899999999pt height=22.465723500000017pt/> gives the asymptotic lower bound.

**Definition (Big-<img src="/tex/b35e24d8a08c0ab01195f2ad2a78fab7.svg?invert_in_darkmode&sanitize=true" align=middle width=12.785434199999989pt height=22.465723500000017pt/> Notation)** - two functions <img src="/tex/6a169b25f34099963b540687ac3b8099.svg?invert_in_darkmode&sanitize=true" align=middle width=77.08347074999999pt height=27.705869399999983pt/> satisfy <img src="/tex/5e4bf2ec16ac611c17bfa49f5a091723.svg?invert_in_darkmode&sanitize=true" align=middle width=65.73626729999998pt height=24.65753399999998pt/> **if and only if** <img src="/tex/479c556e575352c056cf0dffe5f6c60b.svg?invert_in_darkmode&sanitize=true" align=middle width=65.94625949999998pt height=24.65753399999998pt/> and <img src="/tex/a4d1070e1a63094841feb697a19008cd.svg?invert_in_darkmode&sanitize=true" align=middle width=64.82301374999999pt height=24.65753399999998pt/>.

Big-<img src="/tex/b35e24d8a08c0ab01195f2ad2a78fab7.svg?invert_in_darkmode&sanitize=true" align=middle width=12.785434199999989pt height=22.465723500000017pt/> gives matching asymptotic upper and lower bounds.

**Definition (Little-o Notation)** - two functions <img src="/tex/6a169b25f34099963b540687ac3b8099.svg?invert_in_darkmode&sanitize=true" align=middle width=77.08347074999999pt height=27.705869399999983pt/> satisfy <img src="/tex/c707c0d6e2b771bc35d80f7f8c93128b.svg?invert_in_darkmode&sanitize=true" align=middle width=60.91888604999999pt height=24.65753399999998pt/> if **for every** <img src="/tex/03d7460c644e1cc4a5d517935eabb009.svg?invert_in_darkmode&sanitize=true" align=middle width=32.73021674999999pt height=26.17730939999998pt/>, there exists <img src="/tex/f70e5e79cf3bd2b74cda3e84349d4352.svg?invert_in_darkmode&sanitize=true" align=middle width=32.70241424999999pt height=17.723762100000005pt/> such that for every <img src="/tex/c4ecbc7ceca0db57604d584691ddce48.svg?invert_in_darkmode&sanitize=true" align=middle width=48.13998584999999pt height=20.908638300000003pt/>, we have <img src="/tex/8ff203308fbf751194bfa47bf5b016a2.svg?invert_in_darkmode&sanitize=true" align=middle width=92.58382484999998pt height=24.65753399999998pt/>.

Little-o gives an upper bound that is not asymptotically tight.

**Definition (Little-<img src="/tex/ae4fb5973f393577570881fc24fc2054.svg?invert_in_darkmode&sanitize=true" align=middle width=10.82192594999999pt height=14.15524440000002pt/> Notation)** - two functions <img src="/tex/6a169b25f34099963b540687ac3b8099.svg?invert_in_darkmode&sanitize=true" align=middle width=77.08347074999999pt height=27.705869399999983pt/> satisfy <img src="/tex/2f3d2ca3f99772b04ca35be9e9794afb.svg?invert_in_darkmode&sanitize=true" align=middle width=63.77274089999998pt height=24.65753399999998pt/> if **for every** <img src="/tex/03d7460c644e1cc4a5d517935eabb009.svg?invert_in_darkmode&sanitize=true" align=middle width=32.73021674999999pt height=26.17730939999998pt/>, there exists <img src="/tex/f70e5e79cf3bd2b74cda3e84349d4352.svg?invert_in_darkmode&sanitize=true" align=middle width=32.70241424999999pt height=17.723762100000005pt/> such that for every <img src="/tex/c4ecbc7ceca0db57604d584691ddce48.svg?invert_in_darkmode&sanitize=true" align=middle width=48.13998584999999pt height=20.908638300000003pt/>, we have <img src="/tex/00f0a0df44ba166dff243fcf6a9123cb.svg?invert_in_darkmode&sanitize=true" align=middle width=92.58382484999998pt height=24.65753399999998pt/>.

Little-<img src="/tex/ae4fb5973f393577570881fc24fc2054.svg?invert_in_darkmode&sanitize=true" align=middle width=10.82192594999999pt height=14.15524440000002pt/> gives a lower bound that is not asymptotically tight

### Properties

![image-20191010142402298](pics/image-20191010142402298.png)

![image-20191010142413301](pics/image-20191010142413301.png)

![image-20191010143729154](pics/image-20191010143729154.png)

### Techniques

- Compute <img src="/tex/cce16aa01605a0b030eae0cae390ada6.svg?invert_in_darkmode&sanitize=true" align=middle width=88.80135164999999pt height=33.20539859999999pt/>
  - If <img src="/tex/bb0cb7aa9f90d9fd13946da9ffa97ed2.svg?invert_in_darkmode&sanitize=true" align=middle width=25.570741349999988pt height=21.18721440000001pt/>, then <img src="/tex/21db83ff0f44cbae21a4fb10ddace084.svg?invert_in_darkmode&sanitize=true" align=middle width=106.2235053pt height=24.65753399999998pt/>
  - If <img src="/tex/625d4fa396610bfe1065de91733909dd.svg?invert_in_darkmode&sanitize=true" align=middle width=24.46533704999999pt height=14.15524440000002pt/>, then <img src="/tex/1fbce93542e8f17dc1d3a148dde2a325.svg?invert_in_darkmode&sanitize=true" align=middle width=111.04088819999998pt height=24.65753399999998pt/> (i.e. also O and <img src="/tex/9432d83304c1eb0dcb05f092d30a767f.svg?invert_in_darkmode&sanitize=true" align=middle width=11.87217899999999pt height=22.465723500000017pt/>)
  - If <img src="/tex/d7a6bcac46c45b4903f3c0230204b1c0.svg?invert_in_darkmode&sanitize=true" align=middle width=33.789935849999985pt height=14.15524440000002pt/>, then <img src="/tex/0bd6077e9ed685cd6c01635148bba71f.svg?invert_in_darkmode&sanitize=true" align=middle width=109.07736014999999pt height=24.65753399999998pt/> 
- Induction might come in handy when computing limits (show that if <img src="/tex/aa9d1dc08f682f546eeee2869762ff90.svg?invert_in_darkmode&sanitize=true" align=middle width=37.38576269999999pt height=22.831056599999986pt/> holds true, then <img src="/tex/63bb9849783d01d91403bc9a5fea12a2.svg?invert_in_darkmode&sanitize=true" align=middle width=9.075367949999992pt height=22.831056599999986pt/> also holds true), especially when it's <img src="/tex/caffed0f63065b42501fe6d23e50bbf9.svg?invert_in_darkmode&sanitize=true" align=middle width=17.132905349999987pt height=27.91243950000002pt/>, so when you take derivatives, it becomes <img src="/tex/c6916039dab9b718d9dd05c62428e404.svg?invert_in_darkmode&sanitize=true" align=middle width=37.38576269999999pt height=22.831056599999986pt/>

![image-20191010152533111](pics/image-20191010152533111.png)

- <img src="/tex/0695cb495234f0b44f29ae7e3a799408.svg?invert_in_darkmode&sanitize=true" align=middle width=21.232944149999987pt height=22.831056599999986pt/> may not preserve order

![image-20191019121752577](pics/image-20191019121752577.png)

- However, this is true for <img src="/tex/076b2f4a56fde1f767b5d245a29432ed.svg?invert_in_darkmode&sanitize=true" align=middle width=52.26480434999999pt height=22.465723500000017pt/>
- Also however, if <img src="/tex/9805161acebe45dab8468e9c3c70699e.svg?invert_in_darkmode&sanitize=true" align=middle width=154.1686245pt height=24.65753399999998pt/>, then <img src="/tex/3d425a215e8eeb2a056f553633aaae4a.svg?invert_in_darkmode&sanitize=true" align=middle width=32.46972299999999pt height=24.65753399999998pt/> is also <img src="/tex/cb348e62ef41a51450a6b57acf417fe3.svg?invert_in_darkmode&sanitize=true" align=middle width=51.83615249999998pt height=24.65753399999998pt/>

