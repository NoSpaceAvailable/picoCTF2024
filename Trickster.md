# Challenge source
Available at play.picoctf.org
# Difficulty
Medium

# Author
Junias Bonou

# Approach
- The web challenge is a webapp that allows us to upload PNG file:

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/addca7ad-96cf-472e-bdfe-c47a2e6eb001)

- Immediately, I think this is a file upload challenge. I open burpsuite and use my own fake PNG to achieve RCE (do not forget to append .php after the filename)

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/64ced0ff-5ab1-4b07-8bb1-4e6c2bad97c7)

- Access *robots.txt* I found that there is an endpoint *uploads* for us to see the uploaded image. Go to the endpoint:

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/272b3f78-a9b1-4f59-9bc0-289d247121f3)

- We just use *cmd* parameter to RCE:

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/2a903581-c19b-412e-ada6-f547c2313b17)

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/69f88ef0-5763-4b19-beb2-714ab0dc5f89)

- Flag: picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_d3ac625b}
