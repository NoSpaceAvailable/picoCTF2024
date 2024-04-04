# Challenge source
Available at play.picoctf.org
# Difficulty
Medium

# Author
syreal

# Approach
- When I do ssh to the server, all I have is a prompt but I can't use any character match the regex A-Za-z:

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/49baa058-2063-4725-9ea1-e62e7259f24b)

- And also some special chars like \ :

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/f07c5583-93ef-42e2-8943-67d99f272721)

- When I use ~ I found that the default shell is /bin/bash:

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/c3d44e86-fc40-4496-995c-0957cd8aa334)

- After some hours working on it, I found a way to extract some character from what the prompt returned to me:

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/1e390621-c7d4-4234-bf04-015f9482fa36)

- When I use _0=~, that mean I assigned "/home/ctf-player" to the variable "_0". By that, I can extract character with that technique to form a *cat \** command:

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/9febaf62-9cc8-478f-99bc-fdf738243465)

- I received a large text, so I have a big charset now. Using the same technique, I can form other command and get the flag:

  ![image](https://github.com/NoSpaceAvailable/picoCTF2024/assets/143888307/f0f0d8a8-e25d-447c-a76e-74bc9f6ca5be)

- Flag: picoCTF{7h15_mu171v3r53_15_m4dn355_775ac12d}
