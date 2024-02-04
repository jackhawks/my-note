# Git commit 规范



-   feat: 新功能（feature）、新特性
-   fix: 修复 bug
-   docs: 文档（documentation），仅修改了文档，比如 README,LICENSE, CHANGELOG, CONTRIBUTE等
-   style： 格式（不影响代码运行的变动，注意不是 css 修改）仅修改了空格、格式缩进、逗号等等，不改变代码逻辑
-   refactor：代码重构（即不是新增功能，也不是修改bug的代码变动）
-   perf: 优化相关，比如提升性能、体验（在不影响代码内部行为的前提下，对程序性能进行优化）
-   test: 测试用例的新增、修改，包括单元测试、集成测试等
-   revert: 回滚到上一个版本
-   build: 影响项目构建或依赖项修改
-   ci: 持续集成相关文件修改（构建过程或辅助工具的变动，改变构建流程）
-   release: 发布新版本
-   workflow: 工作流相关文件修改
-   chore: 其他修改（不在上述类型中的修改）例如：增加依赖库、工具等



|                               |                             |                                                              |                                            |
| :---------------------------: | :-------------------------: | ------------------------------------------------------------ | ------------------------------------------ |
|            `:art:`            |            :art:            | Improve structure / format of the code.                      | 改进代码的结构/格式。 |
|            `:zap:`            |            :zap:            | Improve performance.                                         | 提高性能。 |
|           `:fire:`            |           :fire:            | Remove code or files.                                        | 删除代码或文件。 |
|            `:bug:`            |            :bug:            | Fix a bug.                                                   | 修复一个错误。 |
|         `:ambulance:`         |         :ambulance:         | Critical hotfix.                                             | 关键修补程序。 |
|         `:sparkles:`          |         :sparkles:          | Introduce new features.                                      | 推出新功能。 |
|           `:memo:`            |           :memo:            | Add or update documentation.                                 | 添加或更新文档。 |
|          `:rocket:`           |          :rocket:           | Deploy stuff.                                                | 部署东西。 |
|         `:lipstick:`          |         :lipstick:          | Add or update the UI and style files.                        | 添加或更新 UI 和样式文件。 |
|           `:tada:`            |           :tada:            | Begin a project.                                             | 开始一个项目。 |
|     `:white_check_mark:`      |     :white_check_mark:      | Add, update, or pass tests.                                  | 添加、更新或通过测试。 |
|           `:lock:`            |           :lock:            | Fix security or privacy issues.                              | 修复安全或隐私问题。 |
|   `:closed_lock_with_key:`    |   :closed_lock_with_key:    | Add or update secrets.                                       | 添加或更新机密。 |
|         `:bookmark:`          |         :bookmark:          | Release / Version tags.                                      | 发布/版本标签。 |
|      `:rotating_light:`       |      :rotating_light:       | Fix compiler / linter warnings.                              | 修复编译器/linter 警告。 |
|       `:construction:`        |       :construction:        | Work in progress.                                            | 工作正在进行中。 |
|        `:green_heart:`        |        :green_heart:        | Fix CI Build.                                                | 修复 CI 构建。 |
|        `:arrow_down:`         |        :arrow_down:         | Downgrade dependencies.                                      | 降级依赖项。 |
|         `:arrow_up:`          |         :arrow_up:          | Upgrade dependencies.                                        | 升级依赖项。 |
|          `:pushpin:`          |          :pushpin:          | Pin dependencies to specific versions.                       | 将依赖项固定到特定版本。 |
|    `:construction_worker:`    |    :construction_worker:    | Add or update CI build system.                               | 添加或更新 CI 构建系统。 |
| `:chart_with_upwards_trend:`  | :chart_with_upwards_trend:  | Add or update analytics or track code.                       | 添加或更新分析或跟踪代码。 |
|          `:recycle:`          |          :recycle:          | Refactor code.                                               | 重构代码。 |
|      `:heavy_plus_sign:`      |      :heavy_plus_sign:      | Add a dependency.                                            | 添加依赖项。 |
|     `:heavy_minus_sign:`      |     :heavy_minus_sign:      | Remove a dependency.                                         | 删除依赖项。 |
|          `:wrench:`           |          :wrench:           | Add or update configuration files.                           | 添加或更新配置文件。 |
|          `:hammer:`           |          :hammer:           | Add or update development scripts.                           | 添加或更新开发脚本。 |
|   `:globe_with_meridians:`    |   :globe_with_meridians:    | Internationalization and localization.                       | 国际化和本地化。 |
|          `:pencil2:`          |          :pencil2:          | Fix typos.                                                   | 修正拼写错误。 |
|           `:poop:`            |           :poop:            | Write bad code that needs to be improved.                    | 编写需要改进的糟糕代码。 |
|          `:rewind:`           |          :rewind:           | Revert changes.                                              | 恢复更改。 |
| `:twisted_rightwards_arrows:` | :twisted_rightwards_arrows: | Merge branches.                                              | 合并分支。 |
|          `:package:`          |          :package:          | Add or update compiled files or packages.                    | 添加或更新编译的文件或包。 |
|           `:alien:`           |           :alien:           | Update code due to external API changes.                     | 由于外部 API 更改而更新代码。 |
|           `:truck:`           |           :truck:           | Move or rename resources (e.g.: files, paths, routes).       | 移动或重命名资源（例如：文件、路径、路线）。 |
|      `:page_facing_up:`       |      :page_facing_up:       | Add or update license.                                       | 添加或更新许可证。 |
|           `:boom:`            |           :boom:            | Introduce breaking changes.                                  | 引入重大变更。 |
|           `:bento:`           |           :bento:           | Add or update assets.                                        | 添加或更新资产。 |
|        `:wheelchair:`         |        :wheelchair:         | Improve accessibility.                                       | 提高可达性。 |
|           `:bulb:`            |           :bulb:            | Add or update comments in source code.                       | 添加或更新源代码中的注释。 |
|           `:beers:`           |           :beers:           | Write code drunkenly.                                        | 喝醉了写代码。 |
|      `:speech_balloon:`       |      :speech_balloon:       | Add or update text and literals.                             | 添加或更新文本和文字。 |
|       `:card_file_box:`       |       :card_file_box:       | Perform database related changes.                            | 执行数据库相关的更改。 |
|        `:loud_sound:`         |        :loud_sound:         | Add or update logs.                                          | 添加或更新日志。 |
|           `:mute:`            |           :mute:            | Remove logs.                                                 | 删除日志。 |
|    `:busts_in_silhouette:`    |    :busts_in_silhouette:    | Add or update contributor(s).                                | 添加或更新贡献者。 |
|     `:children_crossing:`     |     :children_crossing:     | Improve user experience / usability.                         | 提高用户体验/可用性。 |
|   `:building_construction:`   |   :building_construction:   | Make architectural changes.                                  | 进行架构更改。 |
|          `:iphone:`           |          :iphone:           | Work on responsive design.                                   | 致力于响应式设计。 |
|        `:clown_face:`         |        :clown_face:         | Mock things.                                                 | 模拟事物。 |
|            `:egg:`            |            :egg:            | Add or update an easter egg.                                 | 添加或更新复活节彩蛋。 |
|        `:see_no_evil:`        |        :see_no_evil:        | Add or update a .gitignore file.                             | 添加或更新 .gitignore 文件。 |
|       `:camera_flash:`        |       :camera_flash:        | Add or update snapshots.                                     | 添加或更新快照。 |
|          `:alembic:`          |          :alembic:          | Perform experiments.                                         | 进行实验。 |
|            `:mag:`            |            :mag:            | Improve SEO.                                                 | 改善搜索引擎优化。 |
|           `:label:`           |           :label:           | Add or update types.                                         | 添加或更新类型。 |
|         `:seedling:`          |         :seedling:          | Add or update seed files.                                    | 添加或更新种子文件。 |
|  `:triangular_flag_on_post:`  |  :triangular_flag_on_post:  | Add, update, or remove feature flags.                        | 添加、更新或删除功能标志。 |
|         `:goal_net:`          |         :goal_net:          | Catch errors.                                                | 捕获错误。 |
|           `:dizzy:`           |           :dizzy:           | Add or update animations and transitions.                    | 添加或更新动画和过渡。 |
|        `:wastebasket:`        |        :wastebasket:        | Deprecate code that needs to be cleaned up.                  | 弃用需要清理的代码。 |
|     `:passport_control:`      |     :passport_control:      | Work on code related to authorization, roles and permissions. |处理与授权、角色和权限相关的代码。  |
|     `:adhesive_bandage:`      |     :adhesive_bandage:      | Simple fix for a non-critical issue.                         | 针对非关键问题的简单修复。 |
|       `:monocle_face:`        |       :monocle_face:        | Data exploration/inspection.                                 | 数据探索/检查。 |
|          `:coffin:`           |          :coffin:           | Remove dead code.                                            | 删除死代码。 |
|         `:test_tube:`         |         :test_tube:         | Add a failing test.                                          | 添加失败的测试。 |
|          `:necktie:`          |          :necktie:          | Add or update business logic.                                | 添加或更新业务逻辑。 |
|        `:stethoscope:`        |        :stethoscope:        | Add or update healthcheck.                                   | 添加或更新健康检查。 |
|          `:bricks:`           |          :bricks:           | Infrastructure related changes.                              | 基础设施相关的变化。 |
|       `:technologist:`        |       :technologist:        | Improve developer experience.                                | 提高开发者体验。 |
|     `:money_with_wings:`      |     :money_with_wings:      | Add sponsorships or money related infrastructure.            | 添加赞助或金钱相关的基础设施。 |
|          `:thread:`           |          :thread:           | Add or update code related to multithreading or concurrency. | 添加或更新与多线程或并发相关的代码。 |
|        `:safety_vest:`        |        :safety_vest:        | Add or update code related to validation.                    | 添加或更新与验证相关的代码。 |



-   以动词开头，使用第一人称现在时，比如`change`，而不是`changed`或`changes`
-   第一个字母小写
-   结尾不加句号（`.`）



首次提交



```shell
git commit -m ":tada: Initial commit"
```

>   :tada: Initial commit







