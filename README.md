# GroupShadowTableView

让group tableview每个section拥有阴影和圆角

@protocol GroupShadowTableViewDelegate <NSObject>

@optional

- (void)groupShadowTableView:(GroupShadowTableView *)tableView didSelectRowAtIndexPath:(NSIndexPath *)indexPath;

- (CGFloat)groupShadowTableView:(GroupShadowTableView *)tableView heightForRowAtIndexPath:(NSIndexPath *)indexPath;

- (BOOL)groupShadowTableView:(GroupShadowTableView *)tableView canSelectAtSection:(NSInteger)section;

@end

@protocol GroupShadowTableViewDataSource <NSObject>

@optional

- (NSInteger)numberOfSectionsInGroupShadowTableView:(GroupShadowTableView *)tableView;

@required

- (NSInteger)groupShadowTableView:(GroupShadowTableView *)tableView numberOfRowsInSection:(NSInteger)section;

- (UITableViewCell *)groupShadowTableView:(GroupShadowTableView *)tableView cellForRowAtIndexPath:(NSIndexPath *)indexPath;

@end
![示例图片](/eg.png)
