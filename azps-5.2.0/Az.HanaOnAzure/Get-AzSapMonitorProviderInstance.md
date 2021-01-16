---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357613"
---
# <span data-ttu-id="640be-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="640be-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="640be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="640be-102">SYNOPSIS</span></span>
<span data-ttu-id="640be-103">Beveszi egy szolgáltatói példány tulajdonságait a megadott előfizetéshez, erőforráscsoporthoz, SapMonitor névhez és erőforrásnévhez.</span><span class="sxs-lookup"><span data-stu-id="640be-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="640be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="640be-104">SYNTAX</span></span>

### <span data-ttu-id="640be-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="640be-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="640be-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="640be-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="640be-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="640be-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="640be-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="640be-108">DESCRIPTION</span></span>
<span data-ttu-id="640be-109">Beveszi egy szolgáltatói példány tulajdonságait a megadott előfizetéshez, erőforráscsoporthoz, SapMonitor névhez és erőforrásnévhez.</span><span class="sxs-lookup"><span data-stu-id="640be-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="640be-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="640be-110">EXAMPLES</span></span>

### <span data-ttu-id="640be-111">1. példa: Az összes példány lekérte egy SAP-monitor alatt</span><span class="sxs-lookup"><span data-stu-id="640be-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="640be-112">Ez a parancs az SAP-monitor alá minden példányt bevesz.</span><span class="sxs-lookup"><span data-stu-id="640be-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="640be-113">2. példa: SAP-figyelő példányok lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="640be-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="640be-114">Ez a parancs név szerint sap-monitorpéldányokat kap.</span><span class="sxs-lookup"><span data-stu-id="640be-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="640be-115">3. példa: SAP-figyelő példányok lekérte objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="640be-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="640be-116">Ez a parancs az SAP-monitor objektumról-példányra jut.</span><span class="sxs-lookup"><span data-stu-id="640be-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="640be-117">4. példa: SAP-figyelő példányok lekérte folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="640be-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="640be-118">Ez a parancs sap-figyelő példányokat kap folyamat szerint.</span><span class="sxs-lookup"><span data-stu-id="640be-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="640be-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="640be-119">PARAMETERS</span></span>

### <span data-ttu-id="640be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640be-120">-DefaultProfile</span></span>
<span data-ttu-id="640be-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="640be-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="640be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="640be-122">-InputObject</span></span>
<span data-ttu-id="640be-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="640be-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="640be-124">-Name</span><span class="sxs-lookup"><span data-stu-id="640be-124">-Name</span></span>
<span data-ttu-id="640be-125">A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="640be-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="640be-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640be-126">-ResourceGroupName</span></span>
<span data-ttu-id="640be-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="640be-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="640be-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="640be-128">-SapMonitorName</span></span>
<span data-ttu-id="640be-129">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="640be-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="640be-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="640be-130">-SubscriptionId</span></span>
<span data-ttu-id="640be-131">Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="640be-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="640be-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="640be-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="640be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640be-133">CommonParameters</span></span>
<span data-ttu-id="640be-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640be-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="640be-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640be-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="640be-136">INPUTS</span></span>

### <span data-ttu-id="640be-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="640be-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="640be-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="640be-138">OUTPUTS</span></span>

### <span data-ttu-id="640be-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="640be-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="640be-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="640be-140">NOTES</span></span>

<span data-ttu-id="640be-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="640be-141">ALIASES</span></span>

<span data-ttu-id="640be-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="640be-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="640be-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="640be-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="640be-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="640be-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="640be-145">INPUTOBJECT: <IHanaOnAzureIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="640be-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="640be-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="640be-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="640be-147">`[Location <String>]`: A törölt tároló helye.</span><span class="sxs-lookup"><span data-stu-id="640be-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="640be-148">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="640be-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="640be-149">`[ProviderInstanceName <String>]`: A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="640be-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="640be-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="640be-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="640be-151">`[ResourceName <String>]`: Az identitáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="640be-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="640be-152">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="640be-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="640be-153">`[Scope <String>]`: Az erőforrás erőforrás-szolgáltatójának hatóköre.</span><span class="sxs-lookup"><span data-stu-id="640be-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="640be-154">Felügyelt identitásokkal bővített szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="640be-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="640be-155">`[SubscriptionId <String>]`: Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="640be-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="640be-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="640be-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="640be-157">`[VaultName <String>]`: A tároló neve</span><span class="sxs-lookup"><span data-stu-id="640be-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="640be-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="640be-158">RELATED LINKS</span></span>

