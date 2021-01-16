---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336678"
---
# <span data-ttu-id="c48e0-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="c48e0-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="c48e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c48e0-103">Az exportálási előzmények lekérte a megadott hatókörű és exportálási névhez tartozó műveletet.</span><span class="sxs-lookup"><span data-stu-id="c48e0-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="c48e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c48e0-104">SYNTAX</span></span>

### <span data-ttu-id="c48e0-105">Bejő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c48e0-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c48e0-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c48e0-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c48e0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c48e0-107">DESCRIPTION</span></span>
<span data-ttu-id="c48e0-108">Az exportálási előzmények lekérte a megadott hatókörű és exportálási névhez tartozó műveletet.</span><span class="sxs-lookup"><span data-stu-id="c48e0-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="c48e0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c48e0-109">EXAMPLES</span></span>

### <span data-ttu-id="c48e0-110">1. példa: AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="c48e0-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="c48e0-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span><span class="sxs-lookup"><span data-stu-id="c48e0-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="c48e0-112">2. példa: AzCostManagementExportExecutionHistory by InputObject</span><span class="sxs-lookup"><span data-stu-id="c48e0-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="c48e0-113">Get AzCostManagementExportExecutionHistory By InputObject</span><span class="sxs-lookup"><span data-stu-id="c48e0-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="c48e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c48e0-114">PARAMETERS</span></span>

### <span data-ttu-id="c48e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48e0-115">-DefaultProfile</span></span>
<span data-ttu-id="c48e0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c48e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c48e0-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="c48e0-117">-ExportName</span></span>
<span data-ttu-id="c48e0-118">Export Name (Név exportálása) gombra.</span><span class="sxs-lookup"><span data-stu-id="c48e0-118">Export Name.</span></span>

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

### <span data-ttu-id="c48e0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c48e0-119">-InputObject</span></span>
<span data-ttu-id="c48e0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c48e0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c48e0-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="c48e0-121">-Scope</span></span>
<span data-ttu-id="c48e0-122">Ez a paraméter a költségmanagement hatókörét az "Előfizetés", az "Erőforráscsoport" és a "Szolgáltatás szolgáltatása" perspektívából határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c48e0-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="c48e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48e0-123">CommonParameters</span></span>
<span data-ttu-id="c48e0-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48e0-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c48e0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48e0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c48e0-126">INPUTS</span></span>

### <span data-ttu-id="c48e0-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="c48e0-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="c48e0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c48e0-128">OUTPUTS</span></span>

### <span data-ttu-id="c48e0-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="c48e0-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="c48e0-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c48e0-130">NOTES</span></span>

<span data-ttu-id="c48e0-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c48e0-131">ALIASES</span></span>

<span data-ttu-id="c48e0-132">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c48e0-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c48e0-133">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c48e0-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c48e0-134">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c48e0-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c48e0-135">INPUTOBJECT: <ICostManagementIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c48e0-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c48e0-136">`[AlertId <String>]`: Riasztásazonosító</span><span class="sxs-lookup"><span data-stu-id="c48e0-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="c48e0-137">`[ExportName <String>]`: Export Name.</span><span class="sxs-lookup"><span data-stu-id="c48e0-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="c48e0-138">`[ExternalCloudProviderId <String>]`: Ez lehet a csatolt fiók {externalSubscriptionId}, a dimenzióval és lekérdezési műveletekkel használt összesített fiók pedig {externalBillingAccountId}.</span><span class="sxs-lookup"><span data-stu-id="c48e0-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="c48e0-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: A dimenzióval/lekérdezéssel kapcsolatos műveletekhez társított külső felhőszolgáltató típusa.</span><span class="sxs-lookup"><span data-stu-id="c48e0-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="c48e0-140">Ide tartozik az összekapcsolt fiók "külsőSubscriptions" és a "externalBillingAccounts" az összesített fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c48e0-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="c48e0-141">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c48e0-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c48e0-142">`[Scope <String>]`: A nézetműveletekkel társított hatókör.</span><span class="sxs-lookup"><span data-stu-id="c48e0-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="c48e0-143">Ide tartozik az "előfizetések/{subscriptionId}" előfizetési hatókör, az "előfizetések/{subscriptionId}/resourceGroups/{resourceGroupName}" az erőforráscsoport hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' a Számlázási fiók hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" a részleg hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" a EnrollmentAccount hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' a Felügyeleti csoport hatóköréhez, "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" külső számlázási fiók hatóköréhez és a "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" külső előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="c48e0-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="c48e0-144">`[ViewName <String>]`: Nézet neve</span><span class="sxs-lookup"><span data-stu-id="c48e0-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="c48e0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c48e0-145">RELATED LINKS</span></span>

