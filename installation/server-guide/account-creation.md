---
description: >-
  This page provides information on how to setup an account to use with
  NexusForever.
---

# Account Creation

{% hint style="info" %}
Account details from when WildStar was live were lost during the shutdown.\
You are required to create an account specific to NexusForever.
{% endhint %}

## Command

You can use the `account create` command to create a new NexusForever server account.\
More information about the command can be found on the dedicated page [here](../../documentation/command-documentation/account.md#accountcreate).

### Command Console

You can enter the account creation command through the world server command console.

### Web Console

An alternative to enter the account creation command is through the world server web console.

By default you can access the web console through [http://localhost:5000/Console.html](http://localhost:5000/Console.html).

{% hint style="warning" %}
If the world server is running on a remote machine substitute `localhost` with the IP or hostname of the server.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (3).png" alt="" width="563"><figcaption></figcaption></figure>

## Code

It is possible to create an account via code.

WildStar and NexusForever use [SRP6](https://en.wikipedia.org/wiki/Secure_Remote_Password_protocol) for password authentication, a salt and verifier is needed to be generated and stored in database rather than the password.

The helper class PasswordProvider is provided to assist in this process.

```csharp
using NexusForever.Cryptography;
using NexusForever.Database.Auth;
using NexusForever.Database.Auth.Model;

namespace NexusForever.Example
{
    public class AccountCreation
    {
        private readonly AuthContext _context;

        public AccountCreation(
            AuthContext authContext)
        {
            _context = authContext;
        }

        public async Task CreateAccount(string email, string password)
        {
            (string salt, string vertifier) = PasswordProvider.GenerateSaltAndVerifier(email, password);
            _context.Account.Add(new AccountModel
            {
                Email = email,
                S     = salt,
                V     = vertifier
            });
            await _context.SaveChangesAsync();
        }
    }
}

```
