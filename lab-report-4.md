# Lab Report 4


# Step 4: Log into ieng6

<img width="926" alt="Screenshot 2024-02-27 at 2 48 28 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/ed9ed927-9f64-4511-8663-bb9429465fa0">


For this step, I used the `CTRL-R` command after pressing `CTRL-R` I typed in the characters `ssh a` and then pressed `<tab>` to complete the line `ssh aaali@ieng6.ucsd.edu` in the terminal then pressed `<enter>`.
The keys pressed included `CTRL-R` then `ssh a` then `<tab>` then '<enter>`.


# Step 5: Clone your fork of the repository from your Github account (using the SSH URL)


<img width="531" alt="Screenshot 2024-02-27 at 2 54 10 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/9e1b93b8-8543-45ea-976d-a90e2d398870">


-I copied the `ssh` URL from GitHub using `CTRL-C` then just typed the characters `git clone` then used `CTRL-V` and then `<enter>`.


# Step 6: Run the tests, demonstrating that they fail

<img width="295" alt="Screenshot 2024-03-11 at 11 04 36 AM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/2143c74e-03c4-475f-8c34-1d20e230cd7f">

<img width="655" alt="Screenshot 2024-02-27 at 1 47 57 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/341c8c20-5768-4d3e-a835-4694732bcb8f">

-After using the `cd` command to enter the lab7 directory. I used the `CTRL-R` command then i typed in the characters `bash` then pressed `<tab>` to to get the command `bash test.sh` then pressed `<enter>`.



# Step 7: Edit the code file to fix the failing test
<img width="640" alt="Screenshot 2024-02-27 at 3 00 19 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/fbec1f5f-2099-45f1-8150-b6f3015f1be1">

-I used the command `CTRL-R` to complete the line `vim ListExamples.java` and pressed `<enter>` then used the keys `k` `j` `l` `h` to find the spot with the error which was specifically `h` `h` `h` `h` `h` `h` a total of six times. Then I used the 'x' key to delete the number 1 then I used the key `i` to insert the number 2 where the number 1 previously was. After that, I used the `esc` key to go back to normal mode then used the command `:wq!` to save the changes in `ListExamples.java` and pressed `<enter>`.



# Step 8: Run the tests, demonstrating that they now succeed


<img width="556" alt="Screenshot 2024-02-27 at 1 47 28 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/654fddad-27ae-414c-bad1-afa14d48aaa9">

- For this step, I just used the upward key twice `<up>` `<up>` until I found `bash test.sh` again and pressed `<enter>`.


# Step 9: Commit and push the resulting change to your Github account


<img width="690" alt="Screenshot 2024-02-27 at 3 08 21 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/4609d199-58b3-4afd-8730-2a9ae450926e">

-To add the changed commit and push the changes to Github I used the `CTRL-R` for all of these steps. So first after pressing the keys `CTRL-R` I typed the characters `git a` then pressed `<tab>` when i got the command `git add .` then pressed `<enter>`. Then after I just full typed out the command `git commit -m "Fixed code so tests passed"` then pressed `<enter>`. Lastly, I just typed in the command `git push`.

