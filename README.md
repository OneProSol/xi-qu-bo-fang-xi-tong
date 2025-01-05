[点我下载源码](https://www.oneprosol.com/detail/6ab9341805ab49c699af08aabe558979)
或查看我的个人简介下载源码。
支持定制、讲解、修改、远程调试
### 一、相关技术
- 后端：`Java`、`JavaWeb` / `Springboot`。
- 前端：`Vue`、`HTML` / `CSS` / `Javascript` 等。
- 数据库：`MySQL`

### 二、相关软件（列出的软件其一均可运行）
- `IDEA`
- `Eclipse`
- `Visual Studio Code(VScode)`
- `Navicat`
- 等

### 三、功能描述
系统分为（身份）：普通用户、管理员。

**普通用户功能：**
1. 登录
2. 注册
3. 戏曲推荐
4. 戏曲详情
4. 全部戏曲
5. 戏曲脸谱
6. 戏曲戏服
7. 个人信息管理
**管理员功能：**
1. 登录
2. 用户管理
3. 管理员管理
4. 戏曲管理
5. 脸谱管理
6. 戏服管理
7. 评论管理
8. 个人信息管理

### 四、功能图（部分）

#### 普通用户端功能：
1. 登录
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-05%2012:32:43_image.png)
2. 注册
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:54:01_image.png)
3. 戏曲推荐
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:54:27_image.png)
4. 戏曲详情
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:57:35_image.png)
5. 全部戏曲
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:58:17_image.png)
6. 戏曲脸谱
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:58:31_image.png)
7. 戏曲戏服
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:58:54_image.png)
8.个人信息
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:59:15_image.png)
#### 管理员端功能：
1. 登录
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:53:45_image.png)
2. 用户管理
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2011:59:41_image.png)
3. 管理员管理
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2012:00:06_image.png)
4. 戏曲管理
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2012:00:17_image.png)
5. 脸谱管理
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2012:00:28_image.png)
6. 戏服管理
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2012:00:39_image.png)
7. 个人信息管理
![image.png](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-01%2012:01:08_image.png)

### 五、数据库展示
```language
CREATE DATABASE IF NOT EXISTS traditional_opera;
use traditional_opera;

/*
 Navicat Premium Data Transfer

 Source Server         : 192.168.1.2
 Source Server Type    : MySQL
 Source Server Version : 50726
 Source Host           : 192.168.1.2:13306
 Source Schema         : traditional_opera

 Target Server Type    : MySQL
 Target Server Version : 50726
 File Encoding         : 65001

 Date: 22/11/2023 11:04:29
*/

SET NAMES utf8mb4;
SET FOREIGN_KEY_CHECKS = 0;

-- ----------------------------
-- Table structure for comment
-- ----------------------------
DROP TABLE IF EXISTS `comment`;
CREATE TABLE `comment`  (
  `id` varchar(32) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT 'ID',
  `traditional_opera_id` varchar(32) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT '戏曲ID',
  `username` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '用户名',
  `content` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '内容',
  `create_time` bigint(11) UNSIGNED NULL DEFAULT NULL COMMENT '创建时间',
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Dynamic;


-- ----------------------------
-- Table structure for costume
-- ----------------------------
DROP TABLE IF EXISTS `costume`;
CREATE TABLE `costume`  (
  `id` varchar(32) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT 'ID',
  `title` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '标题',
  `content` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '内容',
  `url` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '路径',
  `create_time` bigint(11) UNSIGNED NULL DEFAULT NULL COMMENT '创建时间',
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Dynamic;

-- ----------------------------
-- Table structure for traditional_opera
-- ----------------------------
DROP TABLE IF EXISTS `traditional_opera`;
CREATE TABLE `traditional_opera`  (
  `id` varchar(32) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT 'ID',
  `title` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '标题',
  `content` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '内容',
  `type` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '类型',
  `url` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '路径',
  `count` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '计数器',
  `create_time` bigint(11) UNSIGNED NULL DEFAULT NULL COMMENT '创建时间',
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Dynamic;


-- ----------------------------
-- Table structure for type_facial
-- ----------------------------
DROP TABLE IF EXISTS `type_facial`;
CREATE TABLE `type_facial`  (
  `id` varchar(32) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT 'ID',
  `title` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '标题',
  `content` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '内容',
  `url` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '路径',
  `create_time` bigint(11) UNSIGNED NULL DEFAULT NULL COMMENT '创建时间',
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Dynamic;


-- ----------------------------
-- Table structure for user
-- ----------------------------
DROP TABLE IF EXISTS `user`;
CREATE TABLE `user`  (
  `id` varchar(32) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT 'ID',
  `account` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '用户名',
  `password` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '密码',
  `mobile` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '手机',
  `name` varchar(2000) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '姓名',
  `identity` varchar(32) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT 'ID类型',
  `create_time` bigint(11) UNSIGNED NULL DEFAULT NULL COMMENT '创建时间',
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Dynamic;

SET FOREIGN_KEY_CHECKS = 1;
```
