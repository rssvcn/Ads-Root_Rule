# Ads-Root_Rule
适用于 Root 安卓设备的广告拦截规则仓库

## 说明
- 目标：拦截国内APP广告、开屏广告、信息流内嵌广告、卡片广告、埋点追踪域名
- 运行环境：已 Root 的安卓设备（包括临时Root）
- 更新频率：不定期维护更新
- 两套规则区分，**推荐配合一起使用**：
  - **Ads-Root_Rule.txt**：AdGuard 安卓客户端专属，使用AdGuard修饰符，**不兼容 hosts、AdGuard Home、其他DNS过滤器**
  - **Ads-Dns_Rule.txt**：标准 AdGuard 域名规则（`||域名^` 语法），AdGuard 全系通用（AdGuard安卓 / AdGuard Home / AdGuard DNS），**不支持 hosts、dnsmasq**

## 支持应用名单
<details>
<summary>点击展开查看（持续更新，QQ、微信不支持！）</summary>

- 酷安
- 微博
- 闲鱼
- 爱奇艺
- vivo商城
- vivo天气

</details>

## 拦截案例展示
![拦截效果图](./demo.png)

## 订阅链接
- AdGuard安卓专用（带修饰符版本）
`https://raw.githubusercontent.com/rssvcn/Ads-Root_Rule/main/Ads-Root_Rule.txt`
- DNS通用版本（`||domain^` 语法，AdGuard全家桶可用）
`https://raw.githubusercontent.com/rssvcn/Ads-Root_Rule/main/Ads-Dns_Rule.txt`

## 使用方式
> 推荐方案：AdGuard安卓客户端内**同时订阅两条规则**，DNS规则负责前置域名拦截，修饰符规则做APP精准管控，拦截效果更佳。

### Ads-Root_Rule.txt（AdGuard 安卓客户端）
1. 打开 AdGuard 安卓客户端 → 过滤器 → 自定义过滤器
2. 添加过滤器，填入上方对应 raw 链接（需勾选:受信任的过滤器）
3. 启用规则，配置 AdGuard HTTPS 过滤（证书需安装至系统根证书，依赖Root环境）
> 重要：未Root设备无法正常使用本规则配套的证书与拦截能力；本规则依赖AdGuard专属修饰符，**无法在 AdGuard Home、hosts、DNSMasq 等平台加载**

### Ads-Dns_Rule.txt（AdGuard 全系通用）
1. AdGuard Home / AdGuard安卓：过滤器 → 自定义过滤列表，填入链接
2. 语法为 `||域名^`，**仅适配 AdGuard 系列产品，不能直接给 hosts、dnsmasq 使用**

## 注意事项
1. Ads-Root_Rule.txt 使用 AdGuard 专属修饰符，脱离AdGuard安卓客户端会失效
2. Ads-Dns_Rule.txt 为 `||domain^` 标准域名规则，仅 AdGuard 识别
3. 规则仅用于个人学习使用
4. 如遇到APP异常、闪退，可临时关闭对应规则并提交反馈
5. 本两套规则**均不支持跳过激励广告、广告拿奖励**，有该需求请勿使用、勿入群

## 交流群
QQ交流群：【1027055176】
> 跳激励广告、拿广告奖励需求者勿扰

## 反馈
如有误拦截、漏拦广告，可以在 Issues 提交APP名称、广告截图、对应域名日志。

## License
GNU General Public License v3.0
