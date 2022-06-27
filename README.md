# lerna.js Cheat Sheet
lerna.js Cheat Sheet with the most needed stuff..

<br><br>
<br><br>

- a tool for managing javascript projects with multiple packages
- run npm scripts in each package
- hoist dependencies to ro root level
- easy code sharing between packages

<br><br>
<br><br>

## guides
- https://www.youtube.com/watch?v=p6qoJ4apCjA
- https://www.youtube.com/watch?v=j0FiMekdeOs




<br><br>
<br><br>

## install
```bash
# npm install --global lerna
npm i -D lerna

# npx lerna init
```






<br><br>
<br><br>

## init
```bash
npx lerna init
```
  - Will generate the lerna.json file and package.json
  - Make sure that package.json and lerna.json has version property
  - Move all of your projects into packages folder which was also created







<br><br>
<br><br>


## scripts
```bash
lerna run test
```
  - Will call script for all packages. Similiar to npm run test in single project.


<br><br>


```bash
lerna run test --scope=nameHere
```
  - Will call script for specific package. 
  
<br><br>

```bash
lerna run test --scope={nameHere1,nameHere2}
```
  - Will call script for multiple specific packages.











<br><br>
<br><br>

## version
```bash
lerna version --conventional-commits --yes
```
  - Increase version number of all packages
   - Only affect packages where a commit has been done.



















<br><br>
<br><br>

## diff
```bash
lerna diff
```
  - Show differences compared to last version


















<br><br>
<br><br>

## clean
```bash
lerna clean -y
```
  - Will delete the node_modules folder of all packages

















<br><br>
<br><br>



## bootstrap

```bash
# You may clear before this the node_modules folder of the packages
# lerna clean -y

lerna bootstrap --hoist
```
  - Will check all dependencies from packages and install them to root level that they are accesable for every package
    - That means that you do not have use a node_modules folder inside of your project




