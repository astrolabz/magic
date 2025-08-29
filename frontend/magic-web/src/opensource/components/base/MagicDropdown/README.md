# MagicDropdown Componente Dropdown Magico 📋

`MagicDropdown` è una versione migliorata del componente Dropdown di Ant Design, che offre stili più belli e una migliore esperienza utente.

## Proprietà 📋

| Nome Proprietà   | Tipo      | Valore Predefinito | Descrizione                              |
| ---------------- | --------- | ------------------ | ---------------------------------------- |
| menu             | MenuProps | -                  | Configurazione del menu, per definire il contenuto e il comportamento del dropdown |
| overlayClassName | string    | -                  | Classe personalizzata per il dropdown    |
| ...DropDownProps | -         | -                  | Supporta tutte le proprietà di Ant Design Dropdown |

## Uso Base 💡

```tsx
import { MagicDropdown } from '@/components/base/MagicDropdown';
import { Button, Space } from 'antd';
import type { MenuProps } from 'antd';
import { IconSettings, IconUser, IconLogout } from '@tabler/icons-react';

// Definire gli elementi del menu
const items: MenuProps['items'] = [
  {
    key: '1',
    label: 'Informazioni Personali',
    icon: <IconUser size={16} />,
  },
  {
    key: '2',
    label: 'Impostazioni',
    icon: <IconSettings size={16} />,
  },
  {
    type: 'divider',
  },
  {
    key: '3',
    label: 'Esci dal Login',
    icon: <IconLogout size={16} />,
    danger: true,
  },
];

// Uso base
<MagicDropdown menu={{ items }}>
  <Button>Clicca per mostrare il dropdown</Button>
</MagicDropdown>

// Con modalità di attivazione
<MagicDropdown menu={{ items }} trigger={['hover']}>
  <Button>Passa il mouse per mostrare il dropdown</Button>
</MagicDropdown>

// Con freccia
<MagicDropdown menu={{ items }} arrow>
  <Button>Dropdown con freccia</Button>
</MagicDropdown>

// Con gestione eventi
<MagicDropdown
  menu={{
    items,
    onClick: (e) => console.log('Cliccato elemento menu:', e.key),
  }}
>
  <Button>Clicca elemento per attivare evento</Button>
</MagicDropdown>

// Stato disabilitato
<MagicDropdown menu={{ items }} disabled>
  <Button>Dropdown disabilitato</Button>
</MagicDropdown>
```

## Caratteristiche ✨

1. **Stili Ottimizzati** 🎨: Angoli più arrotondati, spaziatura più ragionevole ed effetti hover più belli
2. **Ottimizzazione Spaziatura Icone** 📏: Migliorata la spaziatura tra icone e testo per un layout più armonioso
3. **Miglioramento Stili Elementi Pericolosi** ⚠️: Forniti segnali visivi più evidenti per operazioni pericolose
4. **Ottimizzazione Posizione Sottomenu** 📍: Regolata la posizione dei sottomenu per una visualizzazione più naturale
5. **Adattamento Tema** 🌙: Adatta automaticamente temi chiari/scuri, fornendo un'esperienza visiva coerente

## Quando Usare ❓

- Quando hai bisogno di posizionare un dropdown nella pagina
- Quando vuoi fornire all'utente molteplici opzioni operative senza occupare troppo spazio
- Quando hai bisogno di raggruppare operazioni correlate
- Quando il dropdown include operazioni pericolose
- Quando desideri uno stile di dropdown più bello

Il componente MagicDropdown rende i tuoi dropdown più belli e facili da usare, mantenendo tutte le funzionalità di Ant Design Dropdown.

## Testo Originale (Cinese e Inglese)
# MagicDropdown 魔法下拉菜单组件

`MagicDropdown` 是一个基于 Ant Design Dropdown 组件的增强版下拉菜单，提供了更美观的样式和更好的用户体验。

## 属性

| 属性名           | 类型      | 默认值 | 说明                                   |
| ---------------- | --------- | ------ | -------------------------------------- |
| menu             | MenuProps | -      | 菜单配置，用于定义下拉菜单的内容和行为 |
| overlayClassName | string    | -      | 下拉菜单的自定义类名                   |
| ...DropDownProps | -         | -      | 支持所有 Ant Design Dropdown 的属性    |

## 基础用法

```tsx
import { MagicDropdown } from '@/components/base/MagicDropdown';
import { Button, Space } from 'antd';
import type { MenuProps } from 'antd';
import { IconSettings, IconUser, IconLogout } from '@tabler/icons-react';

// 定义菜单项
const items: MenuProps['items'] = [
  {
    key: '1',
    label: '个人信息',
    icon: <IconUser size={16} />,
  },
  {
    key: '2',
    label: '设置',
    icon: <IconSettings size={16} />,
  },
  {
    type: 'divider',
  },
  {
    key: '3',
    label: '退出登录',
    icon: <IconLogout size={16} />,
    danger: true,
  },
];

// 基础用法
<MagicDropdown menu={{ items }}>
  <Button>点击显示下拉菜单</Button>
</MagicDropdown>

// 带触发方式
<MagicDropdown menu={{ items }} trigger={['hover']}>
  <Button>悬停显示下拉菜单</Button>
</MagicDropdown>

// 带箭头
<MagicDropdown menu={{ items }} arrow>
  <Button>带箭头的下拉菜单</Button>
</MagicDropdown>

// 带事件处理
<MagicDropdown
  menu={{
    items,
    onClick: (e) => console.log('点击了菜单项:', e.key),
  }}
>
  <Button>点击菜单项触发事件</Button>
</MagicDropdown>

// 禁用状态
<MagicDropdown menu={{ items }} disabled>
  <Button>禁用的下拉菜单</Button>
</MagicDropdown>
```

## 特点

1. **优化的样式**：更大的圆角、更合理的间距和更美观的悬停效果
2. **图标间距优化**：优化了图标与文本之间的间距，使布局更加协调
3. **危险项样式增强**：为危险操作项提供了更明显的视觉提示
4. **子菜单位置优化**：调整了子菜单的位置，使其显示更加自然
5. **主题适配**：自动适应亮色/暗色主题，提供一致的视觉体验

## 何时使用

-   需要在页面上放置一个下拉菜单时
-   需要为用户提供多个操作选项但不想占用太多空间时
-   需要分组展示相关操作时
-   需要在下拉菜单中包含危险操作时
-   需要更美观的下拉菜单样式时

MagicDropdown 组件让你的下拉菜单更加美观和易用，同时保持了 Ant Design Dropdown 的所有功能特性。
