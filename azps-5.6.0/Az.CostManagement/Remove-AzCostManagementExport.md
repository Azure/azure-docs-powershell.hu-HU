---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: e3c464ee8a2ae038a9e6d8d7578c3e4862c16460
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923818"
---
# <span data-ttu-id="a3ce1-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="a3ce1-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="a3ce1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ce1-103">Az exportálás törlésének művelete.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-103">The operation to delete a export.</span></span>

## <span data-ttu-id="a3ce1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3ce1-104">SYNTAX</span></span>

### <span data-ttu-id="a3ce1-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3ce1-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3ce1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a3ce1-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3ce1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3ce1-107">DESCRIPTION</span></span>
<span data-ttu-id="a3ce1-108">Az exportálás törlésének művelete.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-108">The operation to delete a export.</span></span>

## <span data-ttu-id="a3ce1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3ce1-109">EXAMPLES</span></span>

### <span data-ttu-id="a3ce1-110">1. példa: AzCostManagementExport törlése hatókör és név szerint</span><span class="sxs-lookup"><span data-stu-id="a3ce1-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="a3ce1-111">AzCostManagementExport By Scope és ExportName törlése</span><span class="sxs-lookup"><span data-stu-id="a3ce1-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="a3ce1-112">2. példa: AzCostManagementExport törlése exportálási objektum alapján</span><span class="sxs-lookup"><span data-stu-id="a3ce1-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="a3ce1-113">AzCostManagementExport By InputObject törlése</span><span class="sxs-lookup"><span data-stu-id="a3ce1-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="a3ce1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3ce1-114">PARAMETERS</span></span>

### <span data-ttu-id="a3ce1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ce1-115">-DefaultProfile</span></span>
<span data-ttu-id="a3ce1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3ce1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3ce1-117">-InputObject</span></span>
<span data-ttu-id="a3ce1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ce1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a3ce1-119">-Name</span></span>
<span data-ttu-id="a3ce1-120">Export Name (Név exportálása) gombra.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-120">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ce1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3ce1-121">-PassThru</span></span>
<span data-ttu-id="a3ce1-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="a3ce1-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a3ce1-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="a3ce1-123">-Scope</span></span>
<span data-ttu-id="a3ce1-124">Ez a paraméter a költségmanagement hatókörét az "Előfizetés", az "Erőforráscsoport" és a "Szolgáltatás szolgáltatása" perspektívából határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ce1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3ce1-125">-Confirm</span></span>
<span data-ttu-id="a3ce1-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ce1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ce1-127">-WhatIf</span></span>
<span data-ttu-id="a3ce1-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ce1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ce1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ce1-130">CommonParameters</span></span>
<span data-ttu-id="a3ce1-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ce1-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3ce1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ce1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3ce1-133">INPUTS</span></span>

### <span data-ttu-id="a3ce1-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="a3ce1-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="a3ce1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3ce1-135">OUTPUTS</span></span>

### <span data-ttu-id="a3ce1-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3ce1-136">System.Boolean</span></span>

## <span data-ttu-id="a3ce1-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3ce1-137">NOTES</span></span>

<span data-ttu-id="a3ce1-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a3ce1-138">ALIASES</span></span>

<span data-ttu-id="a3ce1-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a3ce1-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3ce1-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3ce1-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3ce1-142">INPUTOBJECT: <ICostManagementIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a3ce1-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3ce1-143">`[AlertId <String>]`: Riasztásazonosító</span><span class="sxs-lookup"><span data-stu-id="a3ce1-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="a3ce1-144">`[ExportName <String>]`: Export Name.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="a3ce1-145">`[ExternalCloudProviderId <String>]`: Ez lehet a csatolt fiók {externalSubscriptionId}, a dimenzióval és lekérdezési műveletekkel használt összesített fiók pedig {externalBillingAccountId}.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="a3ce1-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: A dimenzióval/lekérdezéssel kapcsolatos műveletekhez társított külső felhőszolgáltató típusa.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="a3ce1-147">Ide tartozik az összekapcsolt fiók "külsőSubscriptions" és a "externalBillingAccounts" az összesített fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="a3ce1-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a3ce1-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3ce1-149">`[Scope <String>]`: A nézetműveletekkel társított hatókör.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="a3ce1-150">Ide tartozik az "előfizetések/{subscriptionId}" előfizetési hatókör, az "előfizetések/{subscriptionId}/resourceGroups/{resourceGroupName}" az erőforráscsoport hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' a Számlázási fiók hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" a részleg hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" a EnrollmentAccount hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' a Felügyeleti csoport hatóköréhez, "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" külső számlázási fiók hatóköréhez és a "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" külső előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="a3ce1-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="a3ce1-151">`[ViewName <String>]`: Nézet neve</span><span class="sxs-lookup"><span data-stu-id="a3ce1-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="a3ce1-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3ce1-152">RELATED LINKS</span></span>

