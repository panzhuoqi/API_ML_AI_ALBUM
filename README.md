# 项目名称：毕业智能APP
# Product Requirement（产品说明文档）

| Title                     | Content |
| ------------------------- | ------- |
| Target release(发布日期)  | 2019/11 |
| Epic(史诗名称)            | 记住我  |
| Document status(文档状态) | 进行中  |
| Document owner(文件主人)  | 潘卓祺  |
| Designer(领头的设计师)    | 潘卓祺  |
| Developer(领头的开发者)   | 潘卓祺  |
| QA(领头的测试者)          | 潘卓祺  |

# Catalogue（目录）
- [介绍](#Introduction)
- [背景](#Background)
- [目标](#Goal)
- [PRD1加值宣言](#加值宣言)
- [PRD2核心价值](#核心价值)
- [PRD3核心价值与用户痛点](#核心价值与用户痛点)
- [PRD4人工智能概率性与用户痛点](#人工智能概率性与用户痛点)
- [PRD5需求列表与人工智能API加值](#需求列表与人工智能API加值)


# Introduction
“记住我”是一款主要为毕业生／已毕业的校友准备的智能毕业纪念册app。方便毕业生回忆与练习。


# Background（背景）
大学四年期间，每个人都拍摄了大量的照片，在一个班集体里，并不是每个人都拥有这些照片，而且这些照片中也包括其他人的。（如运动会，班级团建等活动）。用户将照片上传到app，毕业纪念册app可以用作共享相册，共享相册会识别照片中的人物，并将这些人物进行归类。可供其他用户观看／下载。


# Goal（目标）
该APP主要以回忆与社交互动两个功能为主。
- 回忆功能：通过使用人脸识别的API对识别忘记／未知的人脸。
- 社交互动功能：使用高德地图API，让使用【记住我】APP的用户，在校园的某一处进行打卡，并留下自己的故事。


# 加值宣言
- （主要）人脸识别API对本产品价值部分在于：
    - 不用翻开毕业册去找对应的人。只需要上传照片即可以出现该人物的相关信息。
    - 运用百度AI中的人脸识别。输出图片中人脸150个关键点坐标，快速响应分析人脸属性信息，支持人脸1：1对比、1：N搜索、百万人脸库毫秒级查找、6种在线/离线活体检测等功能，可对接权威数据源。

- （辅助）高德地图静态地图API对本产品价值部分在于：
    - 能够帮助毕业生回忆学校的场景故事。
    - 运用高德地图API，让用户可以在学校某些地方进行“打卡”，留下自己大学4年来印象最深的故事。
    - 静态地图服务通过返回一张地图图片响应HTTP请求，使用户能够将高德地图以图片形式嵌入自己的网页中。用户可以指定请求的地图位置、图片大小、以及在地图上添加覆盖物，如标签、标注、折线、多边形。


# 核心价值
- 人脸识别：最小可用产品为识别人脸，返回该人的相关信息。
- 静态地图：最小可用产品为返回静态地图。

# 核心价值与用户痛点
## 核心价值
- 最小可用产品：识别上传的照片，返回对应的人名、详细信息。 

## 用户痛点
- 纸质版的纪念相册，照片少，并不能保证拥有每个人的生活照
- 每个人手上拥有的集体照片都是散乱的、不全
- 回看照片的时候记不起这个人叫什么，需要翻开毕业册的合影去找对应的人。浪费时间
- 纸质版难永久保存，易破损，信息不丰富
- 回忆不起大学四年还有哪些难忘的事件


# 人工智能概率性与用户痛点 
- 人脸检测与属性分析：
上传了TaylorSwift的高清照片，年龄检测不准确，准确的年龄为30岁。百度的人脸识别api在年龄检测上还是不精确／不准确
![人脸检测与属性分析](https://images.gitee.com/uploads/images/2019/1129/111706_881a7284_1532279.png "人脸检测.png")

- 人脸搜索：
需要建立人脸库，如果人脸库里面不存在此用户，那么该人脸搜索返回的结果只是相似的人脸。

给定一张照片，对比人脸库中N张人脸，进行1：N检索，找出最相似的一张或多张人脸，并返回相似度分数。支持百万级人脸库管理，毫秒级识别响应，可满足身份核验、人脸考勤、刷脸通行等应用场景。



# PRD5需求列表与人工智能API加值

需求列表
| #   | User Story（用户案例）                      | Importance（重要性） | Notes（笔记）                                  | 技术              |
| --- | ------------------------------------------- | -------------------- | ---------------------------------------------- | ----------------- |
| 1   | 毕业后看到毕业册上的同学对不上名字          | 极其重要             | 核心功能，要准确，对照片清晰度／人脸占比要求高 | 百度AI人脸识别API |
| 2   | 毕业后不太记得大学4年有哪些印象比较深的回忆 | 重要                 | 校园地标“打卡”，其他用户可以在底下留言       | 高德地图API       |

使用到的API
- 百度API人脸识别
    - [人脸检测](https://ai.baidu.com/docs#/Face-Detect-V3/top)
    - [人脸搜索](https://ai.baidu.com/docs#/Face-Search-V3/top)

- 高德地图API
    - [静态地图](https://lbs.amap.com/api/webservice/guide/api/staticmaps)


