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



|                               |                             |                                                       |                                            |
| :---------------------------: | :-------------------------: | ----------------------------------------------------- | ------------------------------------------ |
|            `:art:`            |            :art:            | Improvestructure/formatofthecode.                     | 改进代码的结构/格式。                      |
|            `:zap:`            |            :zap:            | Improveperformance.                                   | 提高性能。                                 |
|           `:fire:`            |           :fire:            | Removecodeorfiles.                                    | 删除代码或文件。                           |
|            `:bug:`            |            :bug:            | Fixabug.                                              | 修复一个错误。                             |
|         `:ambulance:`         |         :ambulance:         | Criticalhotfix.                                       | 关键热修复。                               |
|         `:sparkles:`          |         :sparkles:          | Introducenewfeatures.                                 | 引入新功能。                               |
|           `:memo:`            |           :memo:            | Addorupdatedocumentation.                             | 添加或更新文档。                           |
|          `:rocket:`           |          :rocket:           | Deploystuff.                                          | 部署东西。                                 |
|         `:lipstick:`          |         :lipstick:          | AddorupdatetheUIandstylefiles.                        | 添加或更新用户界面和样式文件。             |
|           `:tada:`            |           :tada:            | Beginaproject.                                        | 开始一个项目。                             |
|     `:white_check_mark:`      |     :white_check_mark:      | Add,update,orpasstests.                               | 添加、更新或通过测试。                     |
|           `:lock:`            |           :lock:            | Fixsecurityorprivacyissues.                           | 修复安全或隐私问题。                       |
|   `:closed_lock_with_key:`    |   :closed_lock_with_key:    | Addorupdatesecrets.                                   | 添加或更新机密。                           |
|         `:bookmark:`          |         :bookmark:          | Release/Versiontags.                                  | 发布/版本标签。                            |
|      `:rotating_light:`       |      :rotating_light:       | Fixcompiler/linterwarnings.                           | 修正编译器/线程警告。                      |
|       `:construction:`        |       :construction:        | Workinprogress.                                       | 工作正在进行中。                           |
|        `:green_heart:`        |        :green_heart:        | FixCIBuild.                                           | 修复CI构建。                               |
|        `:arrow_down:`         |        :arrow_down:         | Downgradedependencies.                                | 降级依赖。                                 |
|         `:arrow_up:`          |         :arrow_up:          | Upgradedependencies.                                  | 升级依赖项。                               |
|          `:pushpin:`          |          :pushpin:          | Pindependenciestospecificversions.                    | 将依赖关系钉在特定版本上。                 |
|    `:construction_worker:`    |    :construction_worker:    | AddorupdateCIbuildsystem.                             | 添加或更新CI构建系统                       |
| `:chart_with_upwards_trend:`  | :chart_with_upwards_trend:  | Addorupdateanalyticsortrackcode.                      | 添加或更新分析或跟踪代码。                 |
|          `:recycle:`          |          :recycle:          | Refactorcode.                                         | 重构代码。                                 |
|      `:heavy_plus_sign:`      |      :heavy_plus_sign:      | Addadependency.                                       | 添加依赖关系。                             |
|     `:heavy_minus_sign:`      |     :heavy_minus_sign:      | Removeadependency.                                    | 移除依赖关系                               |
|          `:wrench:`           |          :wrench:           | Addorupdateconfigurationfiles.                        | 添加或更新配置文件。                       |
|          `:hammer:`           |          :hammer:           | Addorupdatedevelopmentscripts.                        | 添加或更新开发脚本。                       |
|   `:globe_with_meridians:`    |   :globe_with_meridians:    | Internationalizationandlocalization.                  | 国际化和本地化。                           |
|          `:pencil2:`          |          :pencil2:          | Fixtypos.                                             | 修正错别字。                               |
|           `:poop:`            |           :poop:            | Writebadcodethatneedstobeimproved.                    | 编写需要改进的糟糕代码。                   |
|          `:rewind:`           |          :rewind:           | Revertchanges.                                        | 还原更改。                                 |
| `:twisted_rightwards_arrows:` | :twisted_rightwards_arrows: | Mergebranches.                                        | 合并分支。                                 |
|          `:package:`          |          :package:          | Addorupdatecompiledfilesorpackages.                   | 添加或更新已编译的文件或软件包。           |
|           `:alien:`           |           :alien:           | UpdatecodeduetoexternalAPIchanges.                    | 因外部API变化而更新代码。                  |
|           `:truck:`           |           :truck:           | Moveorrenameresources(e.g.:files,paths,routes).       | 移动或重命名资源（如：文件、路径、路线）。 |
|      `:page_facing_up:`       |      :page_facing_up:       | Addorupdatelicense.                                   | 添加或更新许可证。                         |
|           `:boom:`            |           :boom:            | Introducebreakingchanges.                             | 引入突破性变化。                           |
|           `:bento:`           |           :bento:           | Addorupdateassets.                                    | 添加或更新资产。                           |
|        `:wheelchair:`         |        :wheelchair:         | Improveaccessibility.                                 | 改善无障碍环境。                           |
|           `:bulb:`            |           :bulb:            | Addorupdatecommentsinsourcecode.                      | 添加或更新源代码中的注释                   |
|           `:beers:`           |           :beers:           | Writecodedrunkenly.                                   | 醉醺醺地写代码                             |
|      `:speech_balloon:`       |      :speech_balloon:       | Addorupdatetextandliterals.                           | 添加或更新文本和文字。                     |
|       `:card_file_box:`       |       :card_file_box:       | Performdatabaserelatedchanges.                        | 执行与数据库相关的更改。                   |
|        `:loud_sound:`         |        :loud_sound:         | Addorupdatelogs.                                      | 添加或更新日志。                           |
|           `:mute:`            |           :mute:            | Removelogs.                                           | 移除日志。                                 |
|    `:busts_in_silhouette:`    |    :busts_in_silhouette:    | Addorupdatecontributor(s).                            | 添加或更新撰稿人。                         |
|     `:children_crossing:`     |     :children_crossing:     | Improveuserexperience/usability.                      | 改善用户体验/可用性。                      |
|   `:building_construction:`   |   :building_construction:   | Makearchitecturalchanges.                             | 进行建筑改造。                             |
|          `:iphone:`           |          :iphone:           | Workonresponsivedesign.                               | 致力于响应式设计。                         |
|        `:clown_face:`         |        :clown_face:         | Mockthings.                                           | 模仿                                       |
|            `:egg:`            |            :egg:            | Addorupdateaneasteregg.                               | 添加或更新复活节彩蛋                       |
|        `:see_no_evil:`        |        :see_no_evil:        | Addorupdatea.gitignorefile.                           | 添加或更新.gitignore文件。                 |
|       `:camera_flash:`        |       :camera_flash:        | Addorupdatesnapshots.                                 | 添加或更新快照。                           |
|          `:alembic:`          |          :alembic:          | Performexperiments.                                   | 进行实验。                                 |
|            `:mag:`            |            :mag:            | ImproveSEO.                                           | 改进搜索引擎优化。                         |
|           `:label:`           |           :label:           | Addorupdatetypes.                                     | 添加或更新类型。                           |
|         `:seedling:`          |         :seedling:          | Addorupdateseedfiles.                                 | 添加或更新种子文件。                       |
|  `:triangular_flag_on_post:`  |  :triangular_flag_on_post:  | Add,update,orremovefeatureflags.                      | 添加、更新或删除功能标志。                 |
|         `:goal_net:`          |         :goal_net:          | Catcherrors.                                          | 捕捉错误。                                 |
|           `:dizzy:`           |           :dizzy:           | Addorupdateanimationsandtransitions.                  | 添加或更新动画和过渡效果                   |
|        `:wastebasket:`        |        :wastebasket:        | Deprecatecodethatneedstobecleanedup.                  | 废弃需要清理的代码。                       |
|     `:passport_control:`      |     :passport_control:      | Workoncoderelatedtoauthorization,rolesandpermissions. | 编写与授权、角色和权限相关的代码。         |
|     `:adhesive_bandage:`      |     :adhesive_bandage:      | Simplefixforanon-criticalissue.                       | 对非关键问题的简单修复。                   |
|       `:monocle_face:`        |       :monocle_face:        | Dataexploration/inspection.                           | 数据探索/检查。                            |
|          `:coffin:`           |          :coffin:           | Removedeadcode.                                       | 删除无效代码                               |
|         `:test_tube:`         |         :test_tube:         | Addafailingtest.                                      | 添加一个失败的测试。                       |
|          `:necktie:`          |          :necktie:          | Addorupdatebusinesslogic.                             | 添加或更新业务逻辑。                       |
|        `:stethoscope:`        |        :stethoscope:        | Addorupdatehealthcheck.                               | 添加或更新健康检查。                       |
|          `:bricks:`           |          :bricks:           | Infrastructurerelatedchanges.                         | 与基础设施相关的变更。                     |
|       `:technologist:`        |       :technologist:        | Improvedeveloperexperience.                           | 改善开发人员的体验。                       |
|     `:money_with_wings:`      |     :money_with_wings:      | Addsponsorshipsormoneyrelatedinfrastructure.          | 增加赞助或与资金相关的基础设施。           |
|          `:thread:`           |          :thread:           | Addorupdatecoderelatedtomultithreadingorconcurrency.  | 添加或更新与多线程或并发相关的代码。       |
|        `:safety_vest:`        |        :safety_vest:        | Addorupdatecoderelatedtovalidation.                   | 添加或更新与验证相关的代码。               |



-   以动词开头，使用第一人称现在时，比如`change`，而不是`changed`或`changes`
-   第一个字母小写
-   结尾不加句号（`.`）



首次提交



```shell
git commit -m ":tada: Initial commit"
```

>   :tada: Initial commit







