---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357263"
---
# <span data-ttu-id="ab88f-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="ab88f-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="ab88f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab88f-102">SYNOPSIS</span></span>
<span data-ttu-id="ab88f-103">Egy SAP-monitor tulajdonságait kapja meg a megadott előfizetéshez, erőforráscsoporthoz és erőforrásnévhez.</span><span class="sxs-lookup"><span data-stu-id="ab88f-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="ab88f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab88f-104">SYNTAX</span></span>

### <span data-ttu-id="ab88f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab88f-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab88f-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="ab88f-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab88f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ab88f-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ab88f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab88f-108">DESCRIPTION</span></span>
<span data-ttu-id="ab88f-109">Egy SAP-monitor tulajdonságait kapja meg a megadott előfizetéshez, erőforráscsoporthoz és erőforrásnévhez.</span><span class="sxs-lookup"><span data-stu-id="ab88f-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="ab88f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab88f-110">EXAMPLES</span></span>

### <span data-ttu-id="ab88f-111">1. példa: Az összes SAP-monitor lekérte az előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="ab88f-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ab88f-112">Ez a parancs az SAP-monitorokat egy előfizetés alá kapja.</span><span class="sxs-lookup"><span data-stu-id="ab88f-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="ab88f-113">2. példa: SAP-monitor lekért név szerint</span><span class="sxs-lookup"><span data-stu-id="ab88f-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ab88f-114">Ez a parancs név szerint SAP-monitort kap.</span><span class="sxs-lookup"><span data-stu-id="ab88f-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="ab88f-115">3. példa: SAP-monitor lekérte objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="ab88f-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ab88f-116">Ez a parancs egy SAP-monitort kap objektumról-objektumra.</span><span class="sxs-lookup"><span data-stu-id="ab88f-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="ab88f-117">4. példa: SAP-monitor lekérte folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="ab88f-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ab88f-118">Ez a parancs egy SAP-monitort kap folyamat alapján.</span><span class="sxs-lookup"><span data-stu-id="ab88f-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="ab88f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab88f-119">PARAMETERS</span></span>

### <span data-ttu-id="ab88f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab88f-120">-DefaultProfile</span></span>
<span data-ttu-id="ab88f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab88f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab88f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab88f-122">-InputObject</span></span>
<span data-ttu-id="ab88f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ab88f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab88f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ab88f-124">-Name</span></span>
<span data-ttu-id="ab88f-125">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ab88f-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab88f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab88f-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab88f-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ab88f-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="ab88f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab88f-128">-SubscriptionId</span></span>
<span data-ttu-id="ab88f-129">Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ab88f-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ab88f-130">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ab88f-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab88f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab88f-131">CommonParameters</span></span>
<span data-ttu-id="ab88f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab88f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab88f-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab88f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab88f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab88f-134">INPUTS</span></span>

### <span data-ttu-id="ab88f-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="ab88f-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="ab88f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab88f-136">OUTPUTS</span></span>

### <span data-ttu-id="ab88f-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="ab88f-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="ab88f-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab88f-138">NOTES</span></span>

<span data-ttu-id="ab88f-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ab88f-139">ALIASES</span></span>

<span data-ttu-id="ab88f-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ab88f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab88f-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ab88f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab88f-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab88f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab88f-143">INPUTOBJECT: <IHanaOnAzureIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ab88f-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab88f-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ab88f-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab88f-145">`[Location <String>]`: A törölt tároló helye.</span><span class="sxs-lookup"><span data-stu-id="ab88f-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="ab88f-146">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="ab88f-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="ab88f-147">`[ProviderInstanceName <String>]`: A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="ab88f-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="ab88f-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ab88f-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ab88f-149">`[ResourceName <String>]`: Az identitáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ab88f-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="ab88f-150">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ab88f-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="ab88f-151">`[Scope <String>]`: Az erőforrás erőforrás-szolgáltatójának hatóköre.</span><span class="sxs-lookup"><span data-stu-id="ab88f-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="ab88f-152">Felügyelt identitásokkal bővített szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="ab88f-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="ab88f-153">`[SubscriptionId <String>]`: Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ab88f-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ab88f-154">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ab88f-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ab88f-155">`[VaultName <String>]`: A tároló neve</span><span class="sxs-lookup"><span data-stu-id="ab88f-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="ab88f-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab88f-156">RELATED LINKS</span></span>

