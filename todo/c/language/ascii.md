# ASCII Chart

From cppreference.com
< c‎ | language
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ****ASCII**** | | | | |
| Character sets | | | | |
| Translation phases | | | | |
| Punctuation | | | | |
| Identifier | | | | |
| Scope | | | | |
| Lifetime | | | | |
| Lookup and name spaces | | | | |
| Type | | | | |
| Arithmetic types | | | | |
| Objects and alignment | | | | |
| The main() function | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model and data races | | | | |

The following chart contains all 128 ASCII decimal ****(dec)****, octal ****(oct)****, hexadecimal ****(hex)**** and character ****(ch)**** codes.

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `dec` | `oct` | `hex` | `ch` |  | `dec` | `oct` | `hex` | `ch` |  | `dec` | `oct` | `hex` | `ch` |  | `dec` | `oct` | `hex` | `ch` |
| `0` | `0` | `00` | `NUL` (null) | `32` | `40` | `20` | (space) | `64` | `100` | `40` | `@` | `96` | `140` | `60` | ``` |
| `1` | `1` | `01` | `SOH` (start of header) | `33` | `41` | `21` | `!` | `65` | `101` | `41` | `A` | `97` | `141` | `61` | `a` |
| `2` | `2` | `02` | `STX` (start of text) | `34` | `42` | `22` | `"` | `66` | `102` | `42` | `B` | `98` | `142` | `62` | `b` |
| `3` | `3` | `03` | `ETX` (end of text) | `35` | `43` | `23` | `#` | `67` | `103` | `43` | `C` | `99` | `143` | `63` | `c` |
| `4` | `4` | `04` | `EOT` (end of transmission) | `36` | `44` | `24` | `$` | `68` | `104` | `44` | `D` | `100` | `144` | `64` | `d` |
| `5` | `5` | `05` | `ENQ` (enquiry) | `37` | `45` | `25` | `%` | `69` | `105` | `45` | `E` | `101` | `145` | `65` | `e` |
| `6` | `6` | `06` | `ACK` (acknowledge) | `38` | `46` | `26` | `&` | `70` | `106` | `46` | `F` | `102` | `146` | `66` | `f` |
| `7` | `7` | `07` | `BEL` (bell) | `39` | `47` | `27` | `'` | `71` | `107` | `47` | `G` | `103` | `147` | `67` | `g` |
| `8` | `10` | `08` | `BS` (backspace) | `40` | `50` | `28` | `(` | `72` | `110` | `48` | `H` | `104` | `150` | `68` | `h` |
| `9` | `11` | `09` | `HT` (horizontal tab) | `41` | `51` | `29` | `)` | `73` | `111` | `49` | `I` | `105` | `151` | `69` | `i` |
| `10` | `12` | `0a` | `LF` (line feed - new line) | `42` | `52` | `2a` | `*` | `74` | `112` | `4a` | `J` | `106` | `152` | `6a` | `j` |
| `11` | `13` | `0b` | `VT` (vertical tab) | `43` | `53` | `2b` | `+` | `75` | `113` | `4b` | `K` | `107` | `153` | `6b` | `k` |
| `12` | `14` | `0c` | `FF` (form feed - new page) | `44` | `54` | `2c` | `,` | `76` | `114` | `4c` | `L` | `108` | `154` | `6c` | `l` |
| `13` | `15` | `0d` | `CR` (carriage return) | `45` | `55` | `2d` | `-` | `77` | `115` | `4d` | `M` | `109` | `155` | `6d` | `m` |
| `14` | `16` | `0e` | `SO` (shift out) | `46` | `56` | `2e` | `.` | `78` | `116` | `4e` | `N` | `110` | `156` | `6e` | `n` |
| `15` | `17` | `0f` | `SI` (shift in) | `47` | `57` | `2f` | `/` | `79` | `117` | `4f` | `O` | `111` | `157` | `6f` | `o` |
| `16` | `20` | `10` | `DLE` (data link escape) | `48` | `60` | `30` | `0` | `80` | `120` | `50` | `P` | `112` | `160` | `70` | `p` |
| `17` | `21` | `11` | `DC1` (device control 1) | `49` | `61` | `31` | `1` | `81` | `121` | `51` | `Q` | `113` | `161` | `71` | `q` |
| `18` | `22` | `12` | `DC2` (device control 2) | `50` | `62` | `32` | `2` | `82` | `122` | `52` | `R` | `114` | `162` | `72` | `r` |
| `19` | `23` | `13` | `DC3` (device control 3) | `51` | `63` | `33` | `3` | `83` | `123` | `53` | `S` | `115` | `163` | `73` | `s` |
| `20` | `24` | `14` | `DC4` (device control 4) | `52` | `64` | `34` | `4` | `84` | `124` | `54` | `T` | `116` | `164` | `74` | `t` |
| `21` | `25` | `15` | `NAK` (negative acknowledge) | `53` | `65` | `35` | `5` | `85` | `125` | `55` | `U` | `117` | `165` | `75` | `u` |
| `22` | `26` | `16` | `SYN` (synchronous idle) | `54` | `66` | `36` | `6` | `86` | `126` | `56` | `V` | `118` | `166` | `76` | `v` |
| `23` | `27` | `17` | `ETB` (end of transmission block) | `55` | `67` | `37` | `7` | `87` | `127` | `57` | `W` | `119` | `167` | `77` | `w` |
| `24` | `30` | `18` | `CAN` (cancel) | `56` | `70` | `38` | `8` | `88` | `130` | `58` | `X` | `120` | `170` | `78` | `x` |
| `25` | `31` | `19` | `EM` (end of medium) | `57` | `71` | `39` | `9` | `89` | `131` | `59` | `Y` | `121` | `171` | `79` | `y` |
| `26` | `32` | `1a` | `SUB` (substitute) | `58` | `72` | `3a` | `:` | `90` | `132` | `5a` | `Z` | `122` | `172` | `7a` | `z` |
| `27` | `33` | `1b` | `ESC` (escape) | `59` | `73` | `3b` | `;` | `91` | `133` | `5b` | `[` | `123` | `173` | `7b` | `{` |
| `28` | `34` | `1c` | `FS` (file separator) | `60` | `74` | `3c` | `<` | `92` | `134` | `5c` | `\` | `124` | `174` | `7c` | `|` |
| `29` | `35` | `1d` | `GS` (group separator) | `61` | `75` | `3d` | `=` | `93` | `135` | `5d` | `]` | `125` | `175` | `7d` | `}` |
| `30` | `36` | `1e` | `RS` (record separator) | `62` | `76` | `3e` | `>` | `94` | `136` | `5e` | `^` | `126` | `176` | `7e` | `~` |
| `31` | `37` | `1f` | `US` (unit separator) | `63` | `77` | `3f` | `?` | `95` | `137` | `5f` | `_` | `127` | `177` | `7f` | `DEL` (delete) |

Note: in Unicode, the ASCII character block is known as `U+0000..U+007F` Basic Latin.

### Example

Run this code

```
#include <stdio.h>
 
int main(void)
{
    puts("Printable ASCII:");
    for (int i = 32; i < 127; ++i) {
        putchar(i);
        putchar(i % 16 == 15 ? '\n' : ' ');
    }
}

```

Possible output:

```
Printable ASCII:
  ! " # $ % & ' ( ) * + , - . /
0 1 2 3 4 5 6 7 8 9 : ; < = > ?
@ A B C D E F G H I J K L M N O
P Q R S T U V W X Y Z [ \ ] ^ _
` a b c d e f g h i j k l m n o
p q r s t u v w x y z { | } ~

```

### See also

|  |  |
| --- | --- |
| C++ documentation for ASCII Chart | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/ascii&oldid=130380>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 June 2021, at 14:10.