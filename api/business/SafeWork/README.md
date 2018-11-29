## 安全管理

1. 危险源识别审核，反馈
2. 危险源识别台账
3. 危险源监控跟踪
4. 安全隐患整改审核，反馈
5. 安全隐患整改台账





region i { 嵌入代码块
这是原样输出的代码块
这是原样输出的代码块
} region 



POST /api/AppApi/GetHazardSourceMassageLog 86.查询安全隐患整改通知单台账列表
POST /api/AppApi/GetHazardIdentificationVerificationProcess 81.查询危险源识别审核流程

POST /api/AppApi/AuditingHazardDistinguish 39.危险源识别审核
POST /api/AppApi/GetHazardMonitoringTrackingList 40.危险源监控跟踪
POST /api/AppApi/GetHazardMonitoringTrackingHistoryList 41危险源监控跟踪历史
POST /api/AppApi/GetHazardMonitoringTrackingHistoryContent 42.危险源监控跟踪历史详情
POST /api/AppApi/getHazardIdentificationInfo 72.危险源识别详情

POST /api/AppApi/getHazardIdentificationAuditList 71.危险源识别审核列表(isHandle:是否可操作；HandleType：1审核；2：反馈)
POST /api/AppApi/GetSafetyRectificationNoticeList 46.获取安全整改通知单列表
POST /api/AppApi/GetSafetyRectificationNoticeProcess 47.获取安全整改通知单审核流程
POST /api/AppApi/NewSafetyRectificationNotice 48.新建安全整改通知单（id为空标识添加，id有值标识查询表单明细）
POST /api/AppApi/AuditingSafetyRectificationNotice 49.整改通知单审核:type为：1标识安全隐患审核，2：标识安全隐患反馈



POST /api/AppApi/GetHazardSourceDistinguishLog 85.查询危险源识别台账列表