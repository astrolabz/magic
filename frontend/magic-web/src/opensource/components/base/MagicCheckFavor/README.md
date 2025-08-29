# MagicCheckFavor Componente Magico di Preferenza ✨

MagicCheckFavor è un componente di casella di controllo con stile personalizzato, progettato specificamente per scenari come preferiti e impostazioni di preferenza. Questo componente fornisce un elemento interattivo selezionabile/non selezionabile, con uno stile visivo speciale che lo rende più intuitivo nelle funzionalità relative ai preferiti. ⭐

## Proprietà

| Nome Proprietà | Tipo                       | Valore Predefinito | Descrizione                     |
| -------------- | -------------------------- | ------------------ | ------------------------------- |
| checked        | boolean                    | false              | Se è selezionato                 |
| onChange       | (checked: boolean) => void | -                  | Funzione di callback quando lo stato selezionato cambia |

## Uso Base

```tsx
import MagicCheckFavor from '@/components/base/MagicCheckFavor';
import { useState } from 'react';

// Uso base
const [isChecked, setIsChecked] = useState(false);

<MagicCheckFavor
  checked={isChecked}
  onChange={(checked) => setIsChecked(checked)}
/>

// Selezionato per default
<MagicCheckFavor
  checked={true}
  onChange={(checked) => console.log('Stato selezionato:', checked)}
/>

// Uso in un elemento di lista
<div className="item">
  <span>Progetto Preferito</span>
  <MagicCheckFavor
    checked={item.isFavorite}
    onChange={(checked) => handleFavoriteChange(item.id, checked)}
  />
</div>
```

## Caratteristiche

-   **Stile Personalizzato** 🎨: Diverso dalle caselle di controllo tradizionali, offre un aspetto più adatto agli scenari di preferiti
-   **Semplice da Usare** 👍: API progettata in modo semplice, facile da utilizzare
-   **Gestione Stato** 🔄: Supporta modalità controllata, può controllare lo stato selezionato tramite stato esterno
-   **Feedback Interattivo** 💫: Fornisce feedback visivo intuitivo, migliorando l'esperienza utente
-   **Leggero** 🪶: Implementazione del componente semplice, senza dipendenze aggiuntive

## Scenari di Uso

-   Selezione di elementi nei preferiti
-   Elemento interattivo per funzionalità di like/preferiti
-   Opzioni di interruttore nelle impostazioni di preferenza
-   Qualsiasi elemento di interfaccia che necessita di rappresentare uno stato di "preferito" o "like" ❤️

Il componente MagicCheckFavor, fornendo una casella di controllo visivamente più adatta agli scenari di preferiti, permette agli utenti di ottenere un feedback più intuitivo durante le operazioni di preferiti, elevando l'esperienza utente complessiva. 🌟

---

## Testo Originale (Inglese)

# MagicCheckFavor 魔法复选组件

MagicCheckFavor 是一个自定义样式的复选框组件，专为收藏夹和偏好设置等场景设计。该组件提供了一个可选中/取消选中的交互元素，具有特殊的视觉样式，使其在收藏相关功能中更加直观。

## 属性

| 属性名   | 类型                       | 默认值 | 描述                     |
| -------- | -------------------------- | ------ | ------------------------ |
| checked  | boolean                    | false  | 是否选中                 |
| onChange | (checked: boolean) => void | -      | 选中状态变更时的回调函数 |

## 基本用法

```tsx
import MagicCheckFavor from '@/components/base/MagicCheckFavor';
import { useState } from 'react';

// 基本用法
const [isChecked, setIsChecked] = useState(false);

<MagicCheckFavor
  checked={isChecked}
  onChange={(checked) => setIsChecked(checked)}
/>

// 默认选中
<MagicCheckFavor
  checked={true}
  onChange={(checked) => console.log('选中状态:', checked)}
/>

// 在列表项中使用
<div className="item">
  <span>收藏项目</span>
  <MagicCheckFavor
    checked={item.isFavorite}
    onChange={(checked) => handleFavoriteChange(item.id, checked)}
  />
</div>
```

## 特性

-   **自定义样式**：区别于传统的复选框，提供更符合收藏场景的外观
-   **简单易用**：API 设计简洁，使用方便
-   **状态管理**：支持受控模式，可以通过外部状态控制选中状态
-   **交互反馈**：提供直观的视觉反馈，增强用户体验
-   **轻量级**：组件实现简单，不引入额外依赖

## 使用场景

-   收藏夹中的项目选择
-   喜爱/收藏功能的交互元素
-   偏好设置中的开关选项
-   任何需要表示"收藏"或"喜爱"状态的界面元素

MagicCheckFavor 组件通过提供一个视觉上更符合收藏场景的复选框，使得用户在进行收藏操作时能够获得更直观的反馈，提升整体用户体验。
