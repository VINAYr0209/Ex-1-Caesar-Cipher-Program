# Ex-1-Caesar-Cipher-Program
AIM:
To implement the simple substitution technique named Caesar cipher using C language.

ALOGORITHM:
STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

PROGRAM:
#include <stdio.h> #include <string.h>

int main() { char plaintext[100], ciphertext[100]; int key, i;

printf("Enter the plaintext: ");
scanf("%s", plaintext);

printf("Enter the key: ");
scanf("%d", &key);

key = key % 26;

for (i = 0; plaintext[i] != '\0'; i++)
{
    if (plaintext[i] >= 'A' && plaintext[i] <= 'Z')
    {
        ciphertext[i] = ((plaintext[i] - 'A' + key + 26) % 26) + 'A';
    }
    else if (plaintext[i] >= 'a' && plaintext[i] <= 'z')
    {
        ciphertext[i] = ((plaintext[i] - 'a' + key + 26) % 26) + 'a';
    }
    else
    {
        ciphertext[i] = plaintext[i];
    }
}

ciphertext[i] = '\0';

printf("Ciphertext: %s\n", ciphertext);

return 0;
}

OUTPUT:
Enter the plaintext: HELLO Enter the key: 3 Ciphertext: KHOOR

RESULT :
Thus the implementation of ceasar cipher had been executed successfully.
