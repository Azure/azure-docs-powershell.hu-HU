---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468029"
---
# <span data-ttu-id="846e2-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="846e2-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="846e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="846e2-102">SYNOPSIS</span></span>
<span data-ttu-id="846e2-103">Egy Azure SQL-kiszolgáló Microsoft támogatási műveleteinek naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="846e2-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="846e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="846e2-104">SYNTAX</span></span>

### <span data-ttu-id="846e2-105">ServerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="846e2-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="846e2-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="846e2-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="846e2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="846e2-107">DESCRIPTION</span></span>
<span data-ttu-id="846e2-108">A **Set-AzSqlServerMSSupportAudit** parancsmag megváltoztatja egy Azure SQL-kiszolgáló Microsoft támogatási műveleteinek naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="846e2-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="846e2-109">A parancsmagot a *ResourceGroupName* és *a ServerName* paraméterrel használhatja a kiszolgáló azonosításához.</span><span class="sxs-lookup"><span data-stu-id="846e2-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="846e2-110">Ha a blobtár a naplók célhelye, a *StorageAccountResourceId* paramétert megadva határozza meg a naplók tárfiókját.</span><span class="sxs-lookup"><span data-stu-id="846e2-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="846e2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="846e2-111">EXAMPLES</span></span>

### <span data-ttu-id="846e2-112">1. példa: Azure SQL-kiszolgáló blobtárolójának engedélyezése a Microsoft támogatási műveletvizsgálati házirendjában</span><span class="sxs-lookup"><span data-stu-id="846e2-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="846e2-113">2. példa: Azure SQL-kiszolgáló blobtárolójának letiltása a Microsoft támogatási műveletvizsgálati házirendjában</span><span class="sxs-lookup"><span data-stu-id="846e2-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="846e2-114">3. példa: Azure SQL-kiszolgáló eseményközpontjának engedélyezése a Microsoft támogatási műveletvizsgálati házirendjában</span><span class="sxs-lookup"><span data-stu-id="846e2-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="846e2-115">4. példa: Azure SQL-kiszolgáló eseményközpontjának letiltása a Microsoft támogatási műveletvizsgálati házirendjában</span><span class="sxs-lookup"><span data-stu-id="846e2-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="846e2-116">5. példa: Azure SQL-kiszolgáló naplóelemzési házirendjának engedélyezése a Microsoft támogatási műveleteinek naplózásához</span><span class="sxs-lookup"><span data-stu-id="846e2-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="846e2-117">6. példa: Azure SQL-kiszolgáló naplóelemzési házirend letiltása a Microsoft támogatási műveleteinek naplózásához</span><span class="sxs-lookup"><span data-stu-id="846e2-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="846e2-118">7. példa: Egy Azure SQL-kiszolgáló naplóelemzési házirendjának letiltása a Microsoft által támogatott műveletek naplózási folyamatán keresztül</span><span class="sxs-lookup"><span data-stu-id="846e2-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="846e2-119">8. példa: Tiltsa le egy Azure SQL-kiszolgáló támogatási műveletrekordjainak blobtárolóba küldését, és engedélyezze számukra a naplózási elemzések küldését.</span><span class="sxs-lookup"><span data-stu-id="846e2-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="846e2-120">9. példa: A Microsoft támogatási műveletek naplórekordjainak küldésének engedélyezése egy Azure SQL-kiszolgálóhoz blobtároló, eseményközpont és naplóelemzés céljából.</span><span class="sxs-lookup"><span data-stu-id="846e2-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="846e2-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="846e2-121">PARAMETERS</span></span>

### <span data-ttu-id="846e2-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="846e2-122">-AsJob</span></span>
<span data-ttu-id="846e2-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="846e2-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-124">-BlobstorageTargetState</span><span class="sxs-lookup"><span data-stu-id="846e2-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="846e2-125">Azt jelzi, hogy a blobtároló a Microsoft támogatási műveleteinek naplórekordjainak célhelyét jelenti-e.</span><span class="sxs-lookup"><span data-stu-id="846e2-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="846e2-126">-DefaultProfile</span></span>
<span data-ttu-id="846e2-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="846e2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="846e2-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="846e2-129">Az eseményközpont engedélyezési szabályának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="846e2-129">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="846e2-130">-EventHubName</span></span>
<span data-ttu-id="846e2-131">Az eseményközpont neve.</span><span class="sxs-lookup"><span data-stu-id="846e2-131">The name of the event hub.</span></span> <span data-ttu-id="846e2-132">Ha az EventHubAuthorizationRuleResourceId megadva nincs megadva, az alapértelmezett eseményközpont lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="846e2-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="846e2-133">-EventHubTargetState</span></span>
<span data-ttu-id="846e2-134">Azt jelzi, hogy az eseményközpont a Microsoft támogatási műveleteinek naplórekordjainak célhelyét jelenti-e.</span><span class="sxs-lookup"><span data-stu-id="846e2-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="846e2-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="846e2-136">Azt jelzi, hogy a naplóelemzés a Microsoft támogatási műveleteinek naplórekordjainak célhelyét jelenti-e.</span><span class="sxs-lookup"><span data-stu-id="846e2-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="846e2-137">-PassThru</span></span>
<span data-ttu-id="846e2-138">Megadja, hogy kimenetként adja-e meg a Microsoft támogatási műveletek naplózási házirendét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="846e2-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="846e2-139">-ResourceGroupName</span></span>
<span data-ttu-id="846e2-140">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="846e2-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="846e2-141">-ServerName</span></span>
<span data-ttu-id="846e2-142">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="846e2-142">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="846e2-143">-ServerObject</span></span>
<span data-ttu-id="846e2-144">A Microsoft támogatási műveletek naplózási házirendet kezelő kiszolgálóobjektuma.</span><span class="sxs-lookup"><span data-stu-id="846e2-144">The server object to manage its Microsoft support operations audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="846e2-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="846e2-146">A tárfiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="846e2-146">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="846e2-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="846e2-148">A Log Analytics munkaterületének munkaterület-azonosítója (a Log Analytics munkaterületének erőforrás-azonosítója), amelyre a Microsoft támogatási műveleteinek naplóit el szeretné küldeni.</span><span class="sxs-lookup"><span data-stu-id="846e2-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="846e2-149">Példa: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="846e2-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="846e2-150">-Confirm</span></span>
<span data-ttu-id="846e2-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="846e2-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="846e2-152">-WhatIf</span></span>
<span data-ttu-id="846e2-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="846e2-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="846e2-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="846e2-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846e2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="846e2-155">CommonParameters</span></span>
<span data-ttu-id="846e2-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="846e2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="846e2-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="846e2-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="846e2-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="846e2-158">INPUTS</span></span>

### <span data-ttu-id="846e2-159">System.String</span><span class="sxs-lookup"><span data-stu-id="846e2-159">System.String</span></span>

### <span data-ttu-id="846e2-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="846e2-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="846e2-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="846e2-161">System.Guid</span></span>

### <span data-ttu-id="846e2-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="846e2-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="846e2-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="846e2-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="846e2-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="846e2-164">OUTPUTS</span></span>

### <span data-ttu-id="846e2-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="846e2-165">System.Boolean</span></span>

## <span data-ttu-id="846e2-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="846e2-166">NOTES</span></span>

## <span data-ttu-id="846e2-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="846e2-167">RELATED LINKS</span></span>
