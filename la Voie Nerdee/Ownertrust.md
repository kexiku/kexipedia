*Ownertrust* is a trust-level system for [[GnuPG]] that determine how much does user trust a key owner to verify and sign other people's keys.

## 🔐 Usage

- To change a key's trust level:
```bash
gpg --edit-key <key_ID>
trust
```
You will be prompted to select a trust level then.

### Available trust levels

| *Level*        | *Explanation*                                                                                      |
| -------------- | -------------------------------------------------------------------------------------------------- |
| Unknown (`1`)  | Default state *(no ownertrust has been set yet)*                                                   |
| Never (`2`)    | Never trust the key                                                                                |
| Marginal (`3`) | Requires signatures from **three** different marginally trusted key owners to fully validate a key |
| Full (`4`)     | Trusted emough to sign other keys                                                                  |
| Ultimate (`5`) | You trust this key 'per se' *(only use it for your own keys)*                                      |





[^1]: Sources:
		https://gpgtools.tenderapp.com/kb/faq/what-is-ownertrust-trust-levels-explained
