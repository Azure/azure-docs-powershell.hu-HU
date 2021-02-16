---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163930"
---
# <span data-ttu-id="eb757-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="eb757-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="eb757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb757-102">SYNOPSIS</span></span>
<span data-ttu-id="eb757-103">A megadott hatókör exportálási hatókörének exportálási nevével történő lekért művelet.</span><span class="sxs-lookup"><span data-stu-id="eb757-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="eb757-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb757-104">SYNTAX</span></span>

### <span data-ttu-id="eb757-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb757-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb757-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="eb757-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb757-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eb757-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eb757-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb757-108">DESCRIPTION</span></span>
<span data-ttu-id="eb757-109">A megadott hatókör exportálási hatókörének exportálási nevével történő lekért művelet.</span><span class="sxs-lookup"><span data-stu-id="eb757-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="eb757-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb757-110">EXAMPLES</span></span>

### <span data-ttu-id="eb757-111">1. példa: AzCostManagementExports lekért hatóköre</span><span class="sxs-lookup"><span data-stu-id="eb757-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="eb757-112">AzCostManagementExports lekérte hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="eb757-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="eb757-113">2. példa: AzCostManagementExport be szerezni név és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="eb757-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="eb757-114">Get AzCostManagementExport by Name and scope</span><span class="sxs-lookup"><span data-stu-id="eb757-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="eb757-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb757-115">PARAMETERS</span></span>

### <span data-ttu-id="eb757-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb757-116">-DefaultProfile</span></span>
<span data-ttu-id="eb757-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb757-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb757-118">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="eb757-118">-Expand</span></span>
<span data-ttu-id="eb757-119">Az exportálás tulajdonságainak kibontásához használható.</span><span class="sxs-lookup"><span data-stu-id="eb757-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="eb757-120">Jelenleg csak a "runHistory" támogatott, és az exportálás legutóbbi 10 végrehajtásának adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="eb757-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="eb757-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb757-121">-InputObject</span></span>
<span data-ttu-id="eb757-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="eb757-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eb757-123">-Name</span><span class="sxs-lookup"><span data-stu-id="eb757-123">-Name</span></span>
<span data-ttu-id="eb757-124">Export Name (Név exportálása) gombra.</span><span class="sxs-lookup"><span data-stu-id="eb757-124">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb757-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="eb757-125">-Scope</span></span>
<span data-ttu-id="eb757-126">Ez a paraméter a költségmanagement hatókörét az "Előfizetés", az "Erőforráscsoport" és a "Szolgáltatás szolgáltatása" perspektívából határozza meg.</span><span class="sxs-lookup"><span data-stu-id="eb757-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb757-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb757-127">CommonParameters</span></span>
<span data-ttu-id="eb757-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb757-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb757-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb757-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb757-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb757-130">INPUTS</span></span>

### <span data-ttu-id="eb757-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="eb757-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="eb757-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb757-132">OUTPUTS</span></span>

### <span data-ttu-id="eb757-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="eb757-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="eb757-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb757-134">NOTES</span></span>

<span data-ttu-id="eb757-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eb757-135">ALIASES</span></span>

<span data-ttu-id="eb757-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="eb757-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb757-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="eb757-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb757-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb757-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb757-139">INPUTOBJECT: <ICostManagementIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="eb757-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eb757-140">`[AlertId <String>]`: Riasztásazonosító</span><span class="sxs-lookup"><span data-stu-id="eb757-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="eb757-141">`[ExportName <String>]`: Export Name.</span><span class="sxs-lookup"><span data-stu-id="eb757-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="eb757-142">`[ExternalCloudProviderId <String>]`: Ez lehet a csatolt fiók {externalSubscriptionId}, a dimenzióval és lekérdezési műveletekkel használt összesített fiók pedig {externalBillingAccountId}.</span><span class="sxs-lookup"><span data-stu-id="eb757-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="eb757-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: A dimenzióval/lekérdezéssel kapcsolatos műveletekhez társított külső felhőszolgáltató típusa.</span><span class="sxs-lookup"><span data-stu-id="eb757-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="eb757-144">Ide tartozik az összekapcsolt fiók "külsőSubscriptions" és a "externalBillingAccounts" az összesített fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="eb757-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="eb757-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="eb757-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eb757-146">`[Scope <String>]`: A nézetműveletekkel társított hatókör.</span><span class="sxs-lookup"><span data-stu-id="eb757-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="eb757-147">Ide tartozik az "előfizetések/{subscriptionId}" előfizetési hatókör, az "előfizetések/{subscriptionId}/resourceGroups/{resourceGroupName}" az erőforráscsoport hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' a Számlázási fiók hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" a részleg hatóköréhez, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" a EnrollmentAccount hatóköréhez, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' – Felügyeleti csoport hatóköre, "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" a külső számlázási fiók hatóköréhez, a "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" pedig a külső előfizetés hatóköréhez.</span><span class="sxs-lookup"><span data-stu-id="eb757-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="eb757-148">`[ViewName <String>]`: Nézet neve</span><span class="sxs-lookup"><span data-stu-id="eb757-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="eb757-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb757-149">RELATED LINKS</span></span>

