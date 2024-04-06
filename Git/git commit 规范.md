# Git commit 规范



| Emoji | Keyword       | Symbol                       | Description                | Example                                                      |
| ----- | ------------- | ---------------------------- | -------------------------- | ------------------------------------------------------------ |
| 🌟     | **feat**      | `:star:`                     | 新功能（feature）          | 当你实现一个新的API端点、添加用户交互元素等                  |
| 🐛     | **fix**       | `:bug:`                      | 修复bug                    | 修正导致应用崩溃的异常处理、修复错误的逻辑判断等             |
| 🗒️     | **docs**      | `:memo:`                     | 文档（documentation）      | 更新README文件、补充API文档、修正文档中的错误等              |
| 📄     | **docs-code** | `:page_facing_up:`           | 代码中的文档               | 补充关键函数的注释、更新API文档注释等                        |
| 🎨     | **style**     | `:art:`                      | 代码风格调整               | 调整缩进、修改变量命名以符合命名规范、删除多余的空行等       |
| ♻️     | **refactor**  | `:recycle:`                  | 代码重构                   | 更改代码结构以提高可维护性、优化算法以提高性能等             |
| ⚡     | **perf**      | `:zap:`                      | 性能优化                   | 优化数据库查询、减少不必要的计算、缓存结果以提高响应速度等   |
| 🧪     | **test**      | `:test_tube:`                | 测试                       | 添加新的单元测试、修改测试用例以覆盖更多场景、修复测试代码中的bug等 |
| 🔙     | **revert**    | `:back:`                     | 代码回滚                   | 如果一个以前的更改引入了新的问题，可以使用revert回到稳定状态 |
| 🏗️     | **build**     | `:building_construction:`    | 构建系统或外部依赖项的更改 | 更新编译脚本、更改依赖库版本等                               |
| 🔄     | **ci**        | `:arrows_clockwise:`         | 持续集成                   | 更新CI流程，添加新的构建步骤、修改测试环境配置等             |
| 🏷️     | **release**   | `:label:`                    | 发布版本                   | 更改版本号、更新发布说明等                                   |
| 📈     | **workflow**  | `:chart_with_upwards_trend:` | 工作流更改                 | 修改PR审查流程、更改issue追踪配置等                          |
| 🔒     | **security**  | `:lock:`                     | 安全性修复                 | 修补安全漏洞、增加数据加密处理等                             |
| ⚙️     | **config**    | `:gear:`                     | 配置更改                   | 更改数据库配置、修改环境变量等                               |
| 🖌️     | **ui**        | `:paintbrush:`               | 用户界面更改               | 更新页面布局、修改主题颜色等                                 |
| 🌐     | **i18n**      | `:globe_with_meridians:`     | 国际化和本地化             | 添加新语言支持、更新现有翻译等                               |
| 📊     | **data**      | `:bar_chart:`                | 数据相关更改               | 修改数据模型、更新数据迁移脚本等                             |
| 📦     | **deps**      | `:package:`                  | 依赖更新                   | 升级库版本、移除不再使用的依赖等                             |
| 🏛️     | **arch**      | `:classical_building:`       | 架构更改                   | 更改项目的整体架构设计、引入新的架构模式等                   |
| 🆘     | **hotfix**    | `:sos:`                      | 紧急修复                   | 修复导致生产环境宕机的严重bug等                              |
| 📏     | **lint**      | `:straight_ruler:`           | 代码静态检查               | 解决lint工具报告的问题、统一代码风格等                       |
| 🔧     | **chore**     | `:wrench:`                   | 杂项任务                   | 更新配置文件、修改构建脚本等                                 |



|                               |                             |                                                              |                                              |
| :---------------------------: | :-------------------------: | ------------------------------------------------------------ | -------------------------------------------- |
|            `:art:`            |            :art:            | Improve structure / format of the code.                      | 改进代码的结构/格式。                        |
|            `:zap:`            |            :zap:            | Improve performance.                                         | 提高性能。                                   |
|           `:fire:`            |           :fire:            | Remove code or files.                                        | 删除代码或文件。                             |
|            `:bug:`            |            :bug:            | Fix a bug.                                                   | 修复一个错误。                               |
|         `:ambulance:`         |         :ambulance:         | Critical hotfix.                                             | 关键修补程序。                               |
|         `:sparkles:`          |         :sparkles:          | Introduce new features.                                      | 推出新功能。                                 |
|           `:memo:`            |           :memo:            | Add or update documentation.                                 | 添加或更新文档。                             |
|          `:rocket:`           |          :rocket:           | Deploy stuff.                                                | 部署东西。                                   |
|         `:lipstick:`          |         :lipstick:          | Add or update the UI and style files.                        | 添加或更新 UI 和样式文件。                   |
|           `:tada:`            |           :tada:            | Begin a project.                                             | 开始一个项目。                               |
|     `:white_check_mark:`      |     :white_check_mark:      | Add, update, or pass tests.                                  | 添加、更新或通过测试。                       |
|           `:lock:`            |           :lock:            | Fix security or privacy issues.                              | 修复安全或隐私问题。                         |
|   `:closed_lock_with_key:`    |   :closed_lock_with_key:    | Add or update secrets.                                       | 添加或更新机密。                             |
|         `:bookmark:`          |         :bookmark:          | Release / Version tags.                                      | 发布/版本标签。                              |
|      `:rotating_light:`       |      :rotating_light:       | Fix compiler / linter warnings.                              | 修复编译器/linter 警告。                     |
|       `:construction:`        |       :construction:        | Work in progress.                                            | 工作正在进行中。                             |
|        `:green_heart:`        |        :green_heart:        | Fix CI Build.                                                | 修复 CI 构建。                               |
|        `:arrow_down:`         |        :arrow_down:         | Downgrade dependencies.                                      | 降级依赖项。                                 |
|         `:arrow_up:`          |         :arrow_up:          | Upgrade dependencies.                                        | 升级依赖项。                                 |
|          `:pushpin:`          |          :pushpin:          | Pin dependencies to specific versions.                       | 将依赖项固定到特定版本。                     |
|    `:construction_worker:`    |    :construction_worker:    | Add or update CI build system.                               | 添加或更新 CI 构建系统。                     |
| `:chart_with_upwards_trend:`  | :chart_with_upwards_trend:  | Add or update analytics or track code.                       | 添加或更新分析或跟踪代码。                   |
|          `:recycle:`          |          :recycle:          | Refactor code.                                               | 重构代码。                                   |
|      `:heavy_plus_sign:`      |      :heavy_plus_sign:      | Add a dependency.                                            | 添加依赖项。                                 |
|     `:heavy_minus_sign:`      |     :heavy_minus_sign:      | Remove a dependency.                                         | 删除依赖项。                                 |
|          `:wrench:`           |          :wrench:           | Add or update configuration files.                           | 添加或更新配置文件。                         |
|          `:hammer:`           |          :hammer:           | Add or update development scripts.                           | 添加或更新开发脚本。                         |
|   `:globe_with_meridians:`    |   :globe_with_meridians:    | Internationalization and localization.                       | 国际化和本地化。                             |
|          `:pencil2:`          |          :pencil2:          | Fix typos.                                                   | 修正拼写错误。                               |
|           `:poop:`            |           :poop:            | Write bad code that needs to be improved.                    | 编写需要改进的糟糕代码。                     |
|          `:rewind:`           |          :rewind:           | Revert changes.                                              | 恢复更改。                                   |
| `:twisted_rightwards_arrows:` | :twisted_rightwards_arrows: | Merge branches.                                              | 合并分支。                                   |
|          `:package:`          |          :package:          | Add or update compiled files or packages.                    | 添加或更新编译的文件或包。                   |
|           `:alien:`           |           :alien:           | Update code due to external API changes.                     | 由于外部 API 更改而更新代码。                |
|           `:truck:`           |           :truck:           | Move or rename resources (e.g.: files, paths, routes).       | 移动或重命名资源（例如：文件、路径、路线）。 |
|      `:page_facing_up:`       |      :page_facing_up:       | Add or update license.                                       | 添加或更新许可证。                           |
|           `:boom:`            |           :boom:            | Introduce breaking changes.                                  | 引入重大变更。                               |
|           `:bento:`           |           :bento:           | Add or update assets.                                        | 添加或更新资产。                             |
|        `:wheelchair:`         |        :wheelchair:         | Improve accessibility.                                       | 提高可达性。                                 |
|           `:bulb:`            |           :bulb:            | Add or update comments in source code.                       | 添加或更新源代码中的注释。                   |
|           `:beers:`           |           :beers:           | Write code drunkenly.                                        | 喝醉了写代码。                               |
|      `:speech_balloon:`       |      :speech_balloon:       | Add or update text and literals.                             | 添加或更新文本和文字。                       |
|       `:card_file_box:`       |       :card_file_box:       | Perform database related changes.                            | 执行数据库相关的更改。                       |
|        `:loud_sound:`         |        :loud_sound:         | Add or update logs.                                          | 添加或更新日志。                             |
|           `:mute:`            |           :mute:            | Remove logs.                                                 | 删除日志。                                   |
|    `:busts_in_silhouette:`    |    :busts_in_silhouette:    | Add or update contributor(s).                                | 添加或更新贡献者。                           |
|     `:children_crossing:`     |     :children_crossing:     | Improve user experience / usability.                         | 提高用户体验/可用性。                        |
|   `:building_construction:`   |   :building_construction:   | Make architectural changes.                                  | 进行架构更改。                               |
|          `:iphone:`           |          :iphone:           | Work on responsive design.                                   | 致力于响应式设计。                           |
|        `:clown_face:`         |        :clown_face:         | Mock things.                                                 | 模拟事物。                                   |
|            `:egg:`            |            :egg:            | Add or update an easter egg.                                 | 添加或更新复活节彩蛋。                       |
|        `:see_no_evil:`        |        :see_no_evil:        | Add or update a .gitignore file.                             | 添加或更新 .gitignore 文件。                 |
|       `:camera_flash:`        |       :camera_flash:        | Add or update snapshots.                                     | 添加或更新快照。                             |
|          `:alembic:`          |          :alembic:          | Perform experiments.                                         | 进行实验。                                   |
|            `:mag:`            |            :mag:            | Improve SEO.                                                 | 改善搜索引擎优化。                           |
|           `:label:`           |           :label:           | Add or update types.                                         | 添加或更新类型。                             |
|         `:seedling:`          |         :seedling:          | Add or update seed files.                                    | 添加或更新种子文件。                         |
|  `:triangular_flag_on_post:`  |  :triangular_flag_on_post:  | Add, update, or remove feature flags.                        | 添加、更新或删除功能标志。                   |
|         `:goal_net:`          |         :goal_net:          | Catch errors.                                                | 捕获错误。                                   |
|           `:dizzy:`           |           :dizzy:           | Add or update animations and transitions.                    | 添加或更新动画和过渡。                       |
|        `:wastebasket:`        |        :wastebasket:        | Deprecate code that needs to be cleaned up.                  | 弃用需要清理的代码。                         |
|     `:passport_control:`      |     :passport_control:      | Work on code related to authorization, roles and permissions. | 处理与授权、角色和权限相关的代码。           |
|     `:adhesive_bandage:`      |     :adhesive_bandage:      | Simple fix for a non-critical issue.                         | 针对非关键问题的简单修复。                   |
|       `:monocle_face:`        |       :monocle_face:        | Data exploration/inspection.                                 | 数据探索/检查。                              |
|          `:coffin:`           |          :coffin:           | Remove dead code.                                            | 删除死代码。                                 |
|         `:test_tube:`         |         :test_tube:         | Add a failing test.                                          | 添加失败的测试。                             |
|          `:necktie:`          |          :necktie:          | Add or update business logic.                                | 添加或更新业务逻辑。                         |
|        `:stethoscope:`        |        :stethoscope:        | Add or update healthcheck.                                   | 添加或更新健康检查。                         |
|          `:bricks:`           |          :bricks:           | Infrastructure related changes.                              | 基础设施相关的变化。                         |
|       `:technologist:`        |       :technologist:        | Improve developer experience.                                | 提高开发者体验。                             |
|     `:money_with_wings:`      |     :money_with_wings:      | Add sponsorships or money related infrastructure.            | 添加赞助或金钱相关的基础设施。               |
|          `:thread:`           |          :thread:           | Add or update code related to multithreading or concurrency. | 添加或更新与多线程或并发相关的代码。         |
|        `:safety_vest:`        |        :safety_vest:        | Add or update code related to validation.                    | 添加或更新与验证相关的代码。                 |



-   以动词开头，使用第一人称现在时，比如`change`，而不是`changed`或`changes`
-   第一个字母小写
-   结尾不加句号（`.`）



首次提交



```shell
git commit -m ":tada: Initial commit"
```

>   :tada: Initial commit







