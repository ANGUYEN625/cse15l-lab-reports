# Lab Report 3

## Streamlining ssh Configuration

![Image](./Screenshot%20(915).png)

The .ssh config file on our personal computer.

![Image](./Screenshot%20(922).png)

Running the `ssh` command with our shorter account name and alias `ieng6`.

![Image](./Screenshot%20(932).png)

`scp` command copying a file into the remote server using our alias.


## Set Up Github Access from ieng6

![Image](./Screenshot%20(975).png)

Our public key save on Github.

![Image](./Screenshot%20(974).png)

Our public and private key on our server account.

![Image](./Screenshot%20(955).png)

Used `add` to add files changed and `commit` to commit our changes.

![Image](./Screenshot%20(966).png)

Used `push origin main` to push the changes to our gihub repository.

![Image](./Screenshot%20(978).png)

The changes are shown on Github.

[Link for Commit Here](https://github.com/ANGUYEN625/cse15l-lab-reports/commit/11b9508c2431b61716c7f40b45339091134a38d2)


## Copy Whole Directories With `scp -r`

![Image](./Screenshot%20(981).png)

![Image](./Screenshot%20(982).png)

Used `scp -r` to copy our whole directory to the remote server.

![Image](./Screenshot%20(986).png)

Compiled and ran the tests from our newly copied `markdown-parser` files on the remote server.

![Image](./Screenshot%20(1000).png)

Combined commands to copy to the remote server, log into `ssh`, change the current directory to `markdown-parser`, and then compile and run the tests all in one line.


