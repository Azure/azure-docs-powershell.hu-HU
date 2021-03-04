---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: ef26f52068794349b785c8c067ead33b1ee3284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934417"
---
# <span data-ttu-id="eeaa7-101">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="eeaa7-101">Invoke-AzCostManagementExecuteExport</span></span>

## <span data-ttu-id="eeaa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeaa7-102">SYNOPSIS</span></span>
<span data-ttu-id="eeaa7-103">Az exportálás végrehajtásához szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-103">The operation to execute an export.</span></span>

## <span data-ttu-id="eeaa7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eeaa7-104">SYNTAX</span></span>

### <span data-ttu-id="eeaa7-105">Execute (Default)</span><span class="sxs-lookup"><span data-stu-id="eeaa7-105">Execute (Default)</span></span>
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eeaa7-106">ExecuteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eeaa7-106">ExecuteViaIdentity</span></span>
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eeaa7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eeaa7-107">DESCRIPTION</span></span>
<span data-ttu-id="eeaa7-108">Az exportálás végrehajtásához szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-108">The operation to execute an export.</span></span>

## <span data-ttu-id="eeaa7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eeaa7-109">EXAMPLES</span></span>

### <span data-ttu-id="eeaa7-110">1. példa: Exportálás meghívása ExportName és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="eeaa7-110">Example 1: Invoke Export by ExportName and Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

<span data-ttu-id="eeaa7-111">Invoke Export by ExportName and Scope</span><span class="sxs-lookup"><span data-stu-id="eeaa7-111">Invoke Export by ExportName and Scope</span></span>

### <span data-ttu-id="eeaa7-112">2. példa: Export meghívása InputObject szerint</span><span class="sxs-lookup"><span data-stu-id="eeaa7-112">Example 2: Invoke Export by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

<span data-ttu-id="eeaa7-113">Invoke Export by InputObject</span><span class="sxs-lookup"><span data-stu-id="eeaa7-113">Invoke Export by InputObject</span></span>

## <span data-ttu-id="eeaa7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eeaa7-114">PARAMETERS</span></span>

### <span data-ttu-id="eeaa7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeaa7-115">-DefaultProfile</span></span>
<span data-ttu-id="eeaa7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeaa7-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="eeaa7-117">-ExportName</span></span>
<span data-ttu-id="eeaa7-118">Export Name (Név exportálása) gombra.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeaa7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eeaa7-119">-InputObject</span></span>
<span data-ttu-id="eeaa7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: ExecuteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeaa7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeaa7-121">-PassThru</span></span>
<span data-ttu-id="eeaa7-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="eeaa7-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eeaa7-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="eeaa7-123">-Scope</span></span>
<span data-ttu-id="eeaa7-124">Ez a paraméter a költségmanagement hatókörét az "Előfizetés", az "Erőforráscsoport" és a "Szolgáltatás szolgáltatása" perspektívából határozza meg.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeaa7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeaa7-125">-Confirm</span></span>
<span data-ttu-id="eeaa7-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeaa7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeaa7-127">-WhatIf</span></span>
<span data-ttu-id="eeaa7-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeaa7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeaa7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeaa7-130">CommonParameters</span></span>
<span data-ttu-id="eeaa7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeaa7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eeaa7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeaa7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eeaa7-133">INPUTS</span></span>

### <span data-ttu-id="eeaa7-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="eeaa7-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="eeaa7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eeaa7-135">OUTPUTS</span></span>

### <span data-ttu-id="eeaa7-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eeaa7-136">System.Boolean</span></span>

## <span data-ttu-id="eeaa7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eeaa7-137">NOTES</span></span>

<span data-ttu-id="eeaa7-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eeaa7-138">ALIASES</span></span>

<span data-ttu-id="eeaa7-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="eeaa7-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eeaa7-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eeaa7-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eeaa7-142">INPUTOBJECT: <ICostManagementIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="eeaa7-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eeaa7-143">`[AlertId <String>]`: Riasztásazonosító</span><span class="sxs-lookup"><span data-stu-id="eeaa7-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="eeaa7-144">`[ExportName <String>]`: Export Name.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="eeaa7-145">`[ExternalCloudProviderId <String>]`: Ez lehet a csatolt fiók {externalSubscriptionId}, a dimenzióval és lekérdezési műveletekkel használt összesített fiók pedig {externalBillingAccountId}.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="eeaa7-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: A dimenzióval/lekérdezéssel kapcsolatos műveletekhez társított külső felhőszolgáltató típusa.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="eeaa7-147">Ide tartozik az összekapcsolt fiók "külsőSubscriptions" és a "externalBillingAccounts" az összesített fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="eeaa7-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="eeaa7-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eeaa7-149">`[Scope <String>]`: A nézetműveletekkel társított hatókör.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="eeaa7-150">Ide tartozik az "előfizetések/{subscriptionId}" előfizetési hatókör, az "előfizetések/{subscriptionId}/resourceGroups/{resourceGroupName}" az erőforráscsoport hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' a Számlázási fiók hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" a részleg hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" a EnrollmentAccount hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' a Felügyeleti csoport hatóköréhez, "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" külső számlázási fiók hatóköréhez és a "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" külső előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="eeaa7-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="eeaa7-151">`[ViewName <String>]`: Nézet neve</span><span class="sxs-lookup"><span data-stu-id="eeaa7-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="eeaa7-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eeaa7-152">RELATED LINKS</span></span>

