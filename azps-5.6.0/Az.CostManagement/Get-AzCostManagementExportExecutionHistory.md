---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 602797e32e5d29e3dd4ff2b6ade75ff8055efd0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009670"
---
# <span data-ttu-id="c7b47-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="c7b47-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="c7b47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7b47-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b47-103">Az exportálási előzmények lekérte a megadott hatókörű és exportálási névhez tartozó műveletet.</span><span class="sxs-lookup"><span data-stu-id="c7b47-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="c7b47-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7b47-104">SYNTAX</span></span>

### <span data-ttu-id="c7b47-105">Bejő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7b47-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7b47-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c7b47-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7b47-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7b47-107">DESCRIPTION</span></span>
<span data-ttu-id="c7b47-108">Az exportálási előzmények lekérte a megadott hatókörű és exportálási névhez tartozó műveletet.</span><span class="sxs-lookup"><span data-stu-id="c7b47-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="c7b47-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7b47-109">EXAMPLES</span></span>

### <span data-ttu-id="c7b47-110">1. példa: AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="c7b47-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="c7b47-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span><span class="sxs-lookup"><span data-stu-id="c7b47-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="c7b47-112">2. példa: AzCostManagementExportExecutionHistory by InputObject</span><span class="sxs-lookup"><span data-stu-id="c7b47-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="c7b47-113">Get AzCostManagementExportExecutionHistory By InputObject</span><span class="sxs-lookup"><span data-stu-id="c7b47-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="c7b47-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7b47-114">PARAMETERS</span></span>

### <span data-ttu-id="c7b47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b47-115">-DefaultProfile</span></span>
<span data-ttu-id="c7b47-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7b47-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7b47-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="c7b47-117">-ExportName</span></span>
<span data-ttu-id="c7b47-118">Export Name (Név exportálása) gombra.</span><span class="sxs-lookup"><span data-stu-id="c7b47-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b47-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7b47-119">-InputObject</span></span>
<span data-ttu-id="c7b47-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c7b47-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b47-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="c7b47-121">-Scope</span></span>
<span data-ttu-id="c7b47-122">Ez a paraméter a költségmanagement hatókörét az "Előfizetés", az "Erőforráscsoport" és a "Szolgáltatás szolgáltatása" perspektívából határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c7b47-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b47-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b47-123">CommonParameters</span></span>
<span data-ttu-id="c7b47-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b47-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b47-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7b47-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b47-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7b47-126">INPUTS</span></span>

### <span data-ttu-id="c7b47-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="c7b47-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="c7b47-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7b47-128">OUTPUTS</span></span>

### <span data-ttu-id="c7b47-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="c7b47-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="c7b47-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7b47-130">NOTES</span></span>

<span data-ttu-id="c7b47-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c7b47-131">ALIASES</span></span>

<span data-ttu-id="c7b47-132">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c7b47-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7b47-133">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c7b47-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7b47-134">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7b47-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7b47-135">INPUTOBJECT: <ICostManagementIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c7b47-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7b47-136">`[AlertId <String>]`: Riasztásazonosító</span><span class="sxs-lookup"><span data-stu-id="c7b47-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="c7b47-137">`[ExportName <String>]`: Export Name.</span><span class="sxs-lookup"><span data-stu-id="c7b47-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="c7b47-138">`[ExternalCloudProviderId <String>]`: Ez lehet a csatolt fiók {externalSubscriptionId}, a dimenzióval és lekérdezési műveletekkel használt összesített fiók pedig {externalBillingAccountId}.</span><span class="sxs-lookup"><span data-stu-id="c7b47-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="c7b47-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: A dimenzióval/lekérdezéssel kapcsolatos műveletekhez társított külső felhőszolgáltató típusa.</span><span class="sxs-lookup"><span data-stu-id="c7b47-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="c7b47-140">Ide tartozik az összekapcsolt fiók "külsőSubscriptions" és a "externalBillingAccounts" az összesített fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c7b47-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="c7b47-141">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c7b47-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7b47-142">`[Scope <String>]`: A nézetműveletekkel társított hatókör.</span><span class="sxs-lookup"><span data-stu-id="c7b47-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="c7b47-143">Ide tartozik az "előfizetések/{subscriptionId}" előfizetési hatókör, az "előfizetések/{subscriptionId}/resourceGroups/{resourceGroupName}" az erőforráscsoport hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' a Számlázási fiók hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" a részleg hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" a EnrollmentAccount hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' a Felügyeleti csoport hatóköréhez, "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" külső számlázási fiók hatóköréhez és a "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" külső előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="c7b47-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="c7b47-144">`[ViewName <String>]`: Nézet neve</span><span class="sxs-lookup"><span data-stu-id="c7b47-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="c7b47-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7b47-145">RELATED LINKS</span></span>

