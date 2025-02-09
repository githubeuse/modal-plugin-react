# @githubeuse/modal-plugin-react

A simple React modal plugin.

## Installation

Pour installer le plugin (dernière version), utilisez npm :

```sh
npm install @githubeuse/modal-plugin-react@latest
```

## Utilisation
Voici un exemple d'utilisation du plugin dans un composant React :

```jsx 
import React, { useState } from "react";
import Modal from "@githubeuse/modal-plugin-react";
import "@githubeuse/modal-plugin-react/dist/modal.css"; // ligne de code permettant la mise en forme de la modale

const App = () => {
  const [isOpen, setIsOpen] = useState(false);

  const openModal = () => setIsOpen(true);
  const closeModal = () => setIsOpen(false);

  return (
    <div>
      <button onClick={openModal}>Open Modal</button>
      <Modal isOpen={isOpen} onClose={closeModal}>
        <span>Insérer votre texte ici</span> {/* {children} */}
      </Modal>
    </div>
  );
};

export default App;
```

## Props
**isOpen(bool)**: détermine si la modale est ouverte ou fermée<br>
**onClose(func)**: fonction appelée au clic sur le bouton de fermeture de la modale<br>
**children(node)**: contenu à personnaliser qui sera affiché à l'intérieur de la modale 

## Licence
**ISC License**

```plaintext
Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```