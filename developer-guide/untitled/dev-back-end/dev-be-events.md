# Dev - BE -Events

Events are fired during certains occations in the system lifecycle. 

## Custom events subscription

To listen to events occurring in the system lifecycle, a script \(javascript\) will need to be inserted in the \`/src/service/event/custom-events-subscription\`. The script needs to follow the following format:

```text
// a custom events listener, that subscribe to system events

// following are events callback hooks that one can listen and react
const d: any = {
    subscription: null,
    IncomingHttpEvent: (evt: IncomingHttpEvent) => {},
    BulkEditPreviewEvent: (evt: BulkEditPreviewEvent) => {},
    BulkEditJobEvent: (evt: BulkEditJobEvent) => {},
    ExportAttributePreviewEvent: (evt: ExportAttributePreviewEvent) => {},
    ExportItemPreviewEvent: (evt: ExportItemPreviewEvent) => {},
    ExportPricePreviewEvent: (evt: ExportPricePreviewEvent) => {},
    ExportAttributeJobEvent: (evt: ExportAttributeJobEvent) => {},
    ExportItemJobEvent: (evt: ExportItemJobEvent) => {},
    ExportPriceJobEvent: (evt: ExportPriceJobEvent) => {},
    ImportAttributePreviewEvent: (evt: ImportAttributePreviewEvent) => {},
    ImportItemPreviewEvent: (evt: ImportItemPreviewEvent) => {},
    ImportPricePreviewEvent: (evt: ImportPricePreviewEvent) => {},
    ImportAttributeJobEvent: (evt: ImportAttributeJobEvent) => {},
    ImportItemJobEvent: (evt: ImportItemJobEvent) => {},
    ImportPriceJobEvent: (evt: ImportPriceJobEvent) => {},
    ValidationEvent: (evt: ValidationEvent) => {},
    UpdateAttributesEvent: (evt: UpdateAttributesEvent) => {},
    ChangeAttributeStatusEvent: (evt: ChangeAttributeStatusEvent) => {},
    GetAttributeInViewByNameEvent: (evt: GetAttributeInViewByNameEvent) => {},
    GetAttributeInViewEvent: (evt: GetAttributeInViewEvent) => {},
    GetAttributesInViewEvent: (evt: GetAttributesInViewEvent) => {},
    SaveAttributesEvent: (evt: SaveAttributesEvent) => {},
    SearchAttributesByViewEvent: (evt: SearchAttributesByViewEvent) => {},
    IsValidForgottenPasswordCodeEvent: (evt: IsValidForgottenPasswordCodeEvent) => {},
    ResetForgottenPasswordEvent: (evt: ResetForgottenPasswordEvent) => {},
    ForgotPasswordEvent: (evt: ForgotPasswordEvent) => {},
    LoginEvent: (evt: LoginEvent) => {},
    LogoutEvent: (evt: LogoutEvent) => {},
    AddGlobalAvatarEvent: (evt: AddGlobalAvatarEvent) => {},
    AddGlobalImageEvent: (evt: AddGlobalImageEvent) => {},
    SaveUserAvatarEvent: (evt: SaveUserAvatarEvent) => {},
    GetGlobalAvatarContentByNameEvent: (evt: GetGlobalAvatarContentByNameEvent) => {},
    GetAllGlobalAvatarsEvent: (evt: GetAllGlobalAvatarsEvent) => {},
    CategorySimpleItemsInCategoryEvent: (evt: CategorySimpleItemsNotInCategoryEvent) => {},
    CategorySimpleItemsNotInCategoryEvent: (evt: CategorySimpleItemsNotInCategoryEvent) => {},
    UpdateCategoryEvent: (evt: UpdateCategoryEvent) => {},
    AddCategoryEvent: (evt: AddCategoryEvent) => {},
    DeleteCategoryEvent: (evt: DeleteCategoryEvent) => {},
    GetViewCategoryByNameEvent: (evt: GetViewCategoryByNameEvent) => {},
    GetViewCategoriesEvent: (evt: GetViewCategoriesEvent) => {},
    GetViewCategoriesWithItemsEvent: (evt: GetViewCategoriesWithItemsEvent) => {},
    GetViewCategoryItemsEvent: (evt: GetViewCategoryItemsEvent) => {},
    AddItemToViewCategoryEvent: (evt: AddItemToViewCategoryEvent) => {},
    RemoveItemFromViewCategoryEvent: (evt: RemoveItemFromViewCategoryEvent) => {},
    GetCustomBulkEditByIdEvent: (evt: GetCustomBulkEditByIdEvent) => {},
    GetAllCustomBulkEditsEvent: (evt: GetAllCustomBulkEditsEvent) => {},
    GetCustomExportByIdEvent: (evt: GetCustomExportByIdEvent) => {},
    GetAllCustomExportsEvent: (evt: GetAllCustomExportsEvent) => {},
    GetCustomImportByIdEvent: (evt: GetCustomImportByIdEvent) => {},
    GetAllCustomImportsEvent: (evt: GetAllCustomImportsEvent) => {},
    ChangeCustomRuleStatusEvent: (evt: ChangeCustomRuleStatusEvent) => {},
    AddCustomRuleToViewEvent: (evt: AddCustomRuleToViewEvent) => {},
    GetAllCustomRulesEvent: (evt: GetAllCustomRulesEvent) => {},
    GetAllCustomRulesForViewEvent: (evt: GetAllCustomRulesForViewEvent) => {},
    DeleteCustomRulesEvent: (evt: DeleteCustomRulesEvent) => {},
    SaveUserDashboardWidgetDataEvent: (evt: SaveUserDashboardEvent) => {},
    SaveUserDashboardEvent: (evt: SaveUserDashboardEvent) => {},
    GetUserDashboardWidgetSerializedDataEvent: (evt: GetUserDashboardWidgetSerializedDataEvent) => {},
    GetUserDashboardSerializedDataEvent: (evt: GetUserDashboardSerializedDataEvent) => {},
    GetExportArtifactContentEvent: (evt: GetExportArtifactContentEvent) => {},
    DeleteExportArtifactByIdEvent: (evt: DeleteExportArtifactByIdEvent) => {},
    GetAllExportArtifactsEvent: (evt: GetAllExportArtifactsEvent) => {},
    CreateInvitationEvent: (evt: CreateInvitationEvent) => {},
    ActivateInvitationEvent: (evt: ActivateInvitationEvent) => {},
    GetInvitationByCodeEvent: (evt: GetInvitationByCodeEvent) => {},
    DeleteGroupEvent: (evt: DeleteGroupEvent) => {},
    AddOrUpdateGroupEvent: (evt: AddOrUpdateGroupEvent) => {},
    SearchForGroupsWithNoSuchRoleEvent: (evt: SearchForGroupsWithNoSuchRoleEvent) => {},
    SearchForGroupByNameEvent: (evt: SearchForGroupByNameEvent) => {},
    GetGroupsWithRoleEvent: (evt: GetGroupsWithRoleEvent) => {},
    GetGroupByNameEvent: (evt: GetGroupByNameEvent) => {},
    GetGroupByIdEvent: (evt: GetGroupByIdEvent) => {},
    GetAllGroupsEvent: (evt: GetAllGroupsEvent) => {},
    UpdateItemsStatusEvent: (evt: UpdateItemsStatusEvent) => {},
    UpdateItemValueEvent: (evt: UpdateItemValueEvent) => {},
    UpdateItemEvent: (evt: UpdateItemEvent) => {},
    AddItemEvent: (evt: AddItemEvent) => {},
    AddOrUpdateItemEvent: (evt: AddOrUpdateItemEvent) => {},
    SearchForFavouriteItemsInViewEvent: (evt: SearchForFavouriteItemsInViewEvent) => {},
    SearchForItemsInViewEvent: (evt: SearchForItemsInViewEvent) => {},
    AddFavouriteItemIdsEvent: (evt: AddFavouriteItemIdsEvent) => {},
    RemoveFavouriteItemIdsEvent: (evt: RemoveFavouriteItemIdsEvent) => {},
    GetAllFavouriteItemIdsInViewEvent: (evt: GetAllFavouriteItemIdsInViewEvent) => {},
    GetAllFavouritedItemsInViewEvent: (evt: GetAllFavouritedItemsInViewEvent) => {},
    GetAllItemsInViewEvent: (evt: GetAllItemsInViewEvent) => {},
    GetItemsByIdsEvent: (evt: GetItemsByIdsEvent) => {},
    GetItemByIdEvent: (evt: GetItemByIdEvent) => {},
    GetItemByNameEvent: (evt: GetItemByNameEvent) => {},
    GetItemWithFilteringEvent: (evt: GetItemWithFilteringEvent) => {},
    MarkItemImageAsPrimaryEvent: (evt: MarkItemImageAsPrimaryEvent) => {},
    GetItemPrimaryImageEvent: (evt: GetItemPrimaryImageEvent) => {},
    GetItemImageContentEvent: (evt: GetItemImageContentEvent) => {},
    AddItemImageEvent: (evt: AddItemImageEvent) => {},
    DeleteItemImageEvent: (evt: DeleteItemImageEvent) => {},
    GetJobDetailsByIdEvent: (evt: GetJobDetailsByIdEvent) => {},
    GetAllJobsEvent: (evt: GetAllJobsEvent) => {},
    GetJobByIdEvent: (evt: GetJobByIdEvent) => {},
    CreateJwtTokenEvent: (evt: CreateJwtTokenEvent) => {},
    DecodeJwtTokenEvent: (evt: DecodeJwtTokenEvent) => {},
    VerifyJwtTokenEvent: (evt: VerifyJwtTokenEvent) => {},
    AddUserNotificationEvent: (evt: AddUserNotificationEvent) => {},
    GetUserNotificationsEvent: (evt: GetUserNotificationsEvent) => {},
    GetPricedItemsEvent: (evt: GetPricedItemsEvent) => {},
    GetPricedItemsWithFilteringEvent: (evt: GetPricedItemsWithFilteringEvent) => {},
    SearchGroupsAssociatedWithPricingStructureEvent: (evt: SearchGroupsNotAssociatedWithPricingStructureEvent) => {},
    SearchGroupsNotAssociatedWithPricingStructureEvent: (evt: SearchGroupsNotAssociatedWithPricingStructureEvent) => {},
    GetPricingStructureGroupAssociationsEvent: (evt: GetPricingStructureGroupAssociationsEvent) => {},
    LinkPricingStructureWithGroupIdEvent: (evt: LinkPricingStructureWithGroupIdEvent) => {},
    UnlinkPricingStructureWithGroupIdEvent: (evt: UnlinkPricingStructureWithGroupIdEvent) => {},
    UpdatePricingStructureStatusEvent: (evt: UpdatePricingStructureStatusEvent) => {},
    AddOrUpdatePricingStructuresEvent: (evt: AddOrUpdatePricingStructuresEvent) => {},
    GetPricingStructuresByViewEvent: (evt: GetPricingStructuresByViewEvent) => {},
    GetPartnerPricingStructuresEvent: (evt: GetPartnerPricingStructuresEvent) => {},
    GetAllPricingStructureItemsWithPriceEvent: (evt: GetAllPricingStructureItemsWithPriceEvent) => {},
    GetAllPricingStructuresEvent: (evt: GetAllPricingStructuresEvent) => {},
    GetPricingStructureByNameEvent: (evt: GetPricingStructureByNameEvent) => {},
    GetPricingStructureByIdEvent: (evt: GetPricingStructureByIdEvent) => {},
    SetPricesEvent: (evt: SetPricesEvent) => {},
    AddItemToPricingStructureEvent: (evt: AddItemToPricingStructureEvent) => {},
    GetPricingStructureItemEvent: (evt: GetPricingStructureItemEvent) => {},
    AddOrUpdateRoleEvent: (evt: AddOrUpdateRoleEvent) => {},
    AddRoleToGroupEvent: (evt: AddRoleToGroupEvent) => {},
    GetRoleByNameEvent: (evt: GetRoleByNameEvent) => {},
    GetAllRolesEvent: (evt: GetAllRolesEvent) => {},
    RemoveRoleFromGroup: (evt: RemoveRoleFromGroup) => {},
    AddOrUpdateRuleEvent: (evt: AddOrUpdateRuleEvent) => {},
    UpdateRuleStatusEvent: (evt: UpdateRuleStatusEvent) => {},
    GetRulesEvent: (evt: GetRulesEvent) => {},
    GetRuleEvent: (evt: GetRuleEvent) => {},
    SelfRegisterEvent: (evt: SelfRegisterEvent) => {},
    ApproveSelfRegistrationEvent: (evt: ApproveSelfRegistrationEvent) => {},
    GetAllSelfRegistrationsEvent: (evt: GetAllSelfRegistrationsEvent) => {},
    SearchSelfRegistrationByUsernameEvent: (evt: SearchSelfRegistrationByUsernameEvent) => {},
    DeleteSelfRegistrationEvent: (evt: DeleteSelfRegistrationEvent) => {},
    AddUserEvent: (evt: AddUserEvent) => {},
    UpdateUserEvent: (evt: UpdateUserEvent) => {},
    ChangeUserStatusEvent: (evt: ChangeUserStatusEvent) => {},
    AddUserToGroupEvent: (evt: AddUserToGroupEvent) => {},
    GetUsersInGroupEvent: (evt: GetUsersInGroupEvent) => {},
    GetUsersByStatusEvent: (evt: GetUsersByStatusEvent) => {},
    GetNoAvatarContentEvent: (evt: GetNoAvatarContentEvent) => {},
    GetUserAvatarContentEvent: (evt: GetUserAvatarContentEvent) => {},
    SearchForUserNotInGroupEvent: (evt: SearchForUserNotInGroupEvent) => {},
    SearchUserByUsernameAndStatusEvent: (evt: SearchUserByUsernameAndStatusEvent) => {},
    DeleteUserFromGroupEvent: (evt: DeleteUserFromGroupEvent) => {},
    DeleteUserEvent: (evt: DeleteUserEvent) => {},
    HasAllUserRolesEvent: (evt: HasAllUserRolesEvent) => {},
    HasAnyUserRolesEvent: (evt: HasAnyUserRolesEvent) => {},
    HasNoneUserRolesEvent: (evt: HasNoneUserRolesEvent) => {},
    GetUserByUsernameEvent: (evt: GetUserByUsernameEvent) => {},
    GetUserByIdEvent: (evt: GetUserByIdEvent) => {},
    UpdateUserSettingsEvent: (evt: UpdateUserSettingsEvent) => {},
    GetSettingsEvent: (evt: GetSettingsEvent) => {},
    DeleteViewEvent: (evt: DeleteViewEvent) => {},
    AddOrUpdateViewsEvent: (evt: AddOrUpdateRuleEvent) => {},
    GetAllViewsEvent: (evt: GetAllViewsEvent) => {},
    GetViewByIdEvent: (evt: GetViewByIdEvent) => {},
    GetViewByNameEvent: (evt: GetViewByNameEvent) => {},
    GetViewValidationResultEvent: (evt: GetViewValidationResultEvent) => {},
    GetAllViewValidationsEvent: (evt: GetAllViewValidationsEvent) => {},
    DeleteValidationResultEvent: (evt: DeleteValidationResultEvent) => {},
    GetValidationsByViewIdEvent: (evt: GetValidationsByViewIdEvent) => {},
    GetValidationByViewIdAndValidationIdEvent: (evt: GetValidationByViewIdAndValidationIdEvent) => {}
};

// create an EventSubscriptionRegistry 
const s: EventSubscriptionRegistry = new EventSubscriptionRegistry(
                d, `my-custom-event-subscription');
                
                
export default s;
```

## Events

Following are events that can potentially occurrred during the application lifecycle

| Event | Description |
| :--- | :--- |
| IncomingHttpEvent |  |
| BulkEditPreviewEvent |  |
| BulkEditJobEvent |  |
| ExportAttributePreviewEvent |  |
| ExportItemPreviewEvent |  |
| ExportPricePreviewEvent |  |
| ExportAttributeJobEvent |  |
| ExportItemJobEvent |  |
| ExportPriceJobEvent |  |
| ImportAttributePreviewEvent |  |
| ImportPricePreviewEvent |  |
| ImportAttributeJobEvent |  |
| ImportItemJobEvent |  |
| ImportPriceJobEvent |  |
| ValidationEvent |  |
| UpdateAttributesEvent |  |
| ChangeAttributesStatusEvent |  |
| GetAttributeInViewByNameEvent |  |
| GetAttributeInViewEvent |  |
| GetAttributesInViewEvent |  |
| SaveAttributesEvent |  |
| SearchAttributesByViewEvent |  |
| IsValidForgottenPasswordCodeEvent |  |
| ResetForgottenPasswordEvent |  |
| ForgotPasswordEvent |  |
| LoginEvent |  |
| LogoutEvent |  |
| AddGlobalAvatarEvent |  |
| AddGlobalImageEvent |  |
| SaveUserAvatarEvent |  |
| GetGlobalAvatarContentByNameEvent |  |
| GetAllGlobalAvatarsEvent |  |
| CategorySimpleItemsInCategoryEvent |  |
| CategorySimpleItemsNotInCategoryEvent |  |
| UpdateCategoryEvent |  |
| AddCategoryEvent |  |
| DeleteCategoryEvent |  |
| GetViewCategoryByNameEvent |  |
| GetViewCategoriesEvent |  |
| GetViewCategoriesWithItemsEvent |  |
| GetViewCategoryItemsEvent |  |
| AddItemToViewCategoryEvent |  |
| RemoveItemFromViewCategoryEvent |  |
| GetCustomBulkEditByIdEvent  |  |
| GetAllCustomBulkEditsEvent |  |
| GetCustomExportByIdEvent |  |
| GetAllCustomExportsEvent |  |
| GetCustomExportByIdEvent |  |
| GetAllCustomExportsEvent |  |
| GetCustomImportByIdEvent |  |
| GetAllCustomImportsEvent |  |
| ChangeCustomRuleStatusEvent |  |
| AddCustomRuleToViewEvent |  |
| GetAllCustomRulesEvent |  |
| GetAllCustomRulesStatusEvent |  |
| ChangeCustomRuleStatusEvent |  |
| AddCustomRuleToViewEvent |  |
| GetAllCustomRulesEvent |  |
| GetAllCustomRulesForViewEvent |  |
| DeleteCustomRulesEvent |  |
| SaveUserDashboardWidgetDataEvent |  |
| SaveUserDashboardEvent |  |
| GetUserDashboardWidgetSerializedDataEvent |  |
| GetExportArtifactContentEvent |  |
| DeleteExportArtifactByIdEvent |  |
| GetAllExportArtifactsEvent |  |
| CreateInvitationEvent |  |
| ActivateInvitationEvent |  |
| GetInvitationByCodeEvent |  |
| DeleteGroupEvent |  |
| AddOrUpdateGroupEvent |  |
| SearchForGroupsWithNoSuchRoleEvent |  |
| SearchForGroupByNameEvent |  |
| GetGroupsWithRoleEvent |  |
| GetGroupByNameEvent |  |
| GetGroupByIdEvent |  |
| GetAllGroupsEvent |  |
| UpdateItemsStatusEvent |  |
| UpdateItemValueEvent |  |
| UpdateItemEvent |  |
| AddItemEvent |  |
| AddOrUpdateItemEvent |  |
| SearchForFavouriteItemsInViewEvent |  |
| SearchForItemsInViewEvent |  |
| AddFavouriteItemIdsEvent |  |
| RemoveFavouriteItemIdsEvent |  |
| GetAllFavouriteItemIdsInViewEvent |  |
| GetAllFavouritedItemsInViewEvent |  |
| GetAllItemsInViewEvent |  |
| GetItemsByIdsEvent |  |
| GetItemByIdEvent |  |
| GetItemByNameEvent |  |
| GetItemWithFilteringEvent |  |
| MarkItemImageAsPrimaryEvent |  |
| GetItemPrimaryImageEvent |  |
| GetItemImageContentEvent |  |
| AddItemImageEvent |  |
| DeleteItemImageEvent |  |
| GetJobDetailsByIdEvent |  |
| GetAllJobsEvent |  |
| GetJobByIdEvent |  |
| CreateJwtTokenEvent |  |
| DecodeJwtTokenEvent |  |
| VerifyJwtTokenEvent |  |
| AddUserNotificationEvent |  |
| GetUserNotificationsEvent |  |
| GetPricedItemsEvent |  |
| GetPricedItemsWithFilteringEvent |  |
| SearchGroupsAssociatedWithPricingStructureEvent |  |
| SearchGroupsNotAssociatedWithPricingStructureEvent |  |
| GetPricingStructureGroupAssociationsEvent |  |
| LinkPricingStructureWithGroupIdEvent |  |
| UnlinkPricingStructureWithGroupIdEvent |  |
| UpdatePricingStructureStatusEvent |  |
| AddOrUpdatePricingStructuresEvent |  |
| GetPricingStructuresByViewEvent |  |
| GetPartnerPricingStructuresEvent |  |
| GetAllPricingStructureItemsWithPriceEvent |  |
| GetAllPricingStructuresEvent |  |
| GetPricingStructureByNameEvent |  |
| GetPricingStructureByIdEvent |  |
| SetPricesEvent |  |
| AddItemToPricingStructureEvent |  |
| GetPricingStructureItemEvent |  |
| AddOrUpdateRoleEvent |  |
| AddRoleToGroupEvent |  |
| GetRoleByNameEvent |  |
| GetAllRolesEvent |  |
| RemoveRoleFromGroup |  |
| AddOrUpdateRuleEvent |  |
| UpdateRuleStatusEvent |  |
| GetRulesEvent |  |
| GetRuleEvent |  |
| SelfRegisterEvent |  |
| ApproveSelfRegistrationEvent |  |
| GetAllSelfRegistrationsEvent |  |
| SearchSelfRegistrationByUsernameEvent |  |
| DeleteSelfRegistrationEvent |  |
| AddUserEvent |  |
| UpdateUserEvent |  |
| ChangeUserStatusEvent |  |
| AddUserToGroupEvent |  |
| GetUsersInGroupEvent |  |
| GetUsersByStatusEvent |  |
| GetNoAvatarContentEvent |  |
| GetUserAvatarContentEvent |  |
| SearchForUserNotInGroupEvent |  |
| SearchUserByUsernameAndStatusEvent |  |
| DeleteUserFromGroupEvent |  |
| DeleteUserEvent |  |
| HasAllUserRolesEvent |  |
| HasAnyUserRolesEvent |  |
| HasNoneUserRolesEvent |  |
| GetUserByUsernameEvent |  |
| GetUserByIdEvent |  |
| UpdateUserSettingsEvent |  |
| GetSettingsEvent |  |
| DeleteViewEvent |  |
| AddOrUpdateViewsEvent |  |
| GetAllViewsEvent |  |
| GetViewByIdEvent |  |
| GetViewByNameEvent |  |
| GetViewValidationResultEvent |  |
| GetAllViewValidationsEvent |  |
| DeleteValidationResultEvent |  |
| GetValidationsByViewIdEvent |  |
| GetValidationByViewIdAndValidationIdEvent |  |



