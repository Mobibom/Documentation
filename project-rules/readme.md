# 项目规范

## Unity项目的标准结构(暂定)

```bash
Assets/                 # 存放所有游戏的资源文件
    Scenes/             # 游戏的场景
    Scripts/            # 游戏的C#脚本
    Prefabs/            # 预制件
    Materials/          # 材质
    Audio/              # 音频文件
    Textures/           # 纹理图片
    Resources/          # 游戏内会动态获取的资源
ProjectSettings/        # Unity的项目设置文件
Packages/               # 项目中引用的Unity Packages
.gitignore              # 忽略文件(例如Temp, Library等)
```

## 命名规范(暂定)

### 1. **通用原则**
- **简洁但有意义**：命名应简洁，但能清楚表达资产的用途或功能。
- **使用驼峰命名法（CamelCase）或下划线**：例如 `PlayerModel` 或 `player_model`，但应保持项目内一致。
- **避免特殊字符**：尽量只使用字母、数字和下划线，避免使用空格或其他特殊字符。
- **分类前缀**：通过前缀区分资产类型，如 `UI_`、`SFX_`。

### 2. **命名规范示例**
#### 2.1 场景 (Scenes)
- 使用 **"Scene_"** 或 **"Level_"** 前缀，后接场景的描述或编号。
  - 示例：`Scene_MainMenu`、`Level_01`、`Scene_Gameplay`

#### 2.2 脚本 (Scripts)
- 使用 PascalCase 命名法，脚本名称应明确表示功能或类型，且通常与类名一致。
  - 示例：`PlayerController`、`EnemyAI`、`GameManager`

#### 2.3 预制体 (Prefabs)
- 使用 **"Prefab_"** 或 **"P_"** 前缀，后接对象的描述。
  - 示例：`Prefab_PlayerCharacter`、`P_EnemyGoblin`

#### 2.4 材质 (Materials)
- 使用 **"Mat_"** 前缀，后接材质的用途或对象名称。
  - 示例：`Mat_PlayerSkin`、`Mat_Grass`

#### 2.5 网格/模型 (Meshes/Models)
- 使用 **"Model_"** 或 **"Mesh_"** 前缀，后接具体的模型描述。
  - 示例：`Model_TreeOak`、`Mesh_WeaponSword`

#### 2.6 纹理 (Textures)
- 使用 **"Tex_"** 前缀，后接对象描述与用途。
  - 示例：`Tex_WoodDiffuse`、`Tex_RockNormal`

#### 2.7 音效 (Audio)
- 使用 **"SFX_"**（音效）或 **"BGM_"**（背景音乐）前缀，后接音效描述。
  - 示例：`SFX_GunShot`、`BGM_MainTheme`

#### 2.8 动画 (Animations)
- 使用 **"Anim_"** 前缀，后接动画描述。
  - 示例：`Anim_WalkCycle`、`Anim_Jump`

#### 2.9 用户界面 (UI)
- 使用 **"UI_"** 前缀，后接元素名称。
  - 示例：`UI_ButtonStart`、`UI_PanelSettings`


### 3. **具体命名规范建议**
- **版本控制**：使用日期或版本号后缀来标识不同版本的资产，避免覆盖旧版本。
  - 示例：`Scene_MainMenu_v1`、`Prefab_Enemy_v2`

- **语言标记**：多语言支持时可以加上语言后缀。
  - 示例：`UI_TextWelcome_EN`、`UI_TextWelcome_CN`
