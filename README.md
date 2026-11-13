# React Modal Component — Projet OpenClassrooms 14

Composant modal React réutilisable, publié sur npm. Réalisé dans le cadre du projet [HRnet](https://github.com/stephanievanoverberghe/ocr-p14-hrnet-typescript) (migration d'une application jQuery vers React), où l'objectif était de remplacer un plugin jQuery par un composant React publié.

## Installation

```bash
npm install vanoverberghe-react-modal-component
```

## Utilisation

```jsx
import { useState } from 'react';
import { Modal } from 'vanoverberghe-react-modal-component';

function App() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <>
      <button onClick={() => setIsOpen(true)}>Enregistrer</button>
      <Modal
        isOpen={isOpen}
        onClose={() => setIsOpen(false)}
        message="Employé créé avec succès"
      />
    </>
  );
}
```

## Props

| Prop | Type | Requis | Description |
| --- | --- | --- | --- |
| `isOpen` | `boolean` | oui | Affiche ou masque la modale |
| `onClose` | `function` | oui | Appelée au clic sur le bouton « OK » |
| `message` | `string` | oui | Texte affiché dans la modale |

## Accessibilité

La modale utilise `role="dialog"` et relie son titre et son message via `aria-labelledby` et `aria-describedby`.

## Style

Le composant utilise des classes **Tailwind CSS** : le projet qui l'intègre doit avoir Tailwind configuré.

## Licence

MIT
