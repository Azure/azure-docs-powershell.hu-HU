---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185342"
---
# <span data-ttu-id="0ed20-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="0ed20-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="0ed20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ed20-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed20-103">A megadott előfizetéshez, erőforrás csoporthoz, SapMonitor és erőforrás nevéhez tartozó szolgáltatói példány tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ed20-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="0ed20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ed20-104">SYNTAX</span></span>

### <span data-ttu-id="0ed20-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ed20-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ed20-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="0ed20-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ed20-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ed20-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ed20-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ed20-108">DESCRIPTION</span></span>
<span data-ttu-id="0ed20-109">A megadott előfizetéshez, erőforrás csoporthoz, SapMonitor és erőforrás nevéhez tartozó szolgáltatói példány tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ed20-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="0ed20-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0ed20-110">EXAMPLES</span></span>

### <span data-ttu-id="0ed20-111">Példa 1: az összes példány beolvasása az SAP-monitor alatt</span><span class="sxs-lookup"><span data-stu-id="0ed20-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="0ed20-112">Ez a parancs egy SAP-monitor alatt minden példányt beolvas.</span><span class="sxs-lookup"><span data-stu-id="0ed20-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="0ed20-113">2. példa: SAP-monitor példányainak beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="0ed20-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="0ed20-114">Ez a parancs a SAP-figyelés példányait név szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="0ed20-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="0ed20-115">3. példa: az SAP-monitor példányának beszerzése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="0ed20-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="0ed20-116">Ez a parancs az SAP-monitor objektum szerinti példányait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ed20-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="0ed20-117">Példa 4: az SAP-monitorok példányának beszerzése csővezetéken</span><span class="sxs-lookup"><span data-stu-id="0ed20-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="0ed20-118">Ez a parancs csővezetéken keresztüli SAP-monitor példányait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ed20-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="0ed20-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ed20-119">PARAMETERS</span></span>

### <span data-ttu-id="0ed20-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed20-120">-DefaultProfile</span></span>
<span data-ttu-id="0ed20-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ed20-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ed20-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ed20-122">-InputObject</span></span>
<span data-ttu-id="0ed20-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0ed20-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ed20-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ed20-124">-Name</span></span>
<span data-ttu-id="0ed20-125">A szolgáltató példányának neve.</span><span class="sxs-lookup"><span data-stu-id="0ed20-125">Name of the provider instance.</span></span>

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

### <span data-ttu-id="0ed20-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed20-126">-ResourceGroupName</span></span>
<span data-ttu-id="0ed20-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ed20-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="0ed20-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="0ed20-128">-SapMonitorName</span></span>
<span data-ttu-id="0ed20-129">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0ed20-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="0ed20-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ed20-130">-SubscriptionId</span></span>
<span data-ttu-id="0ed20-131">Előfizetési azonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0ed20-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0ed20-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0ed20-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0ed20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed20-133">CommonParameters</span></span>
<span data-ttu-id="0ed20-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ed20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed20-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0ed20-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed20-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ed20-136">INPUTS</span></span>

### <span data-ttu-id="0ed20-137">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="0ed20-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="0ed20-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ed20-138">OUTPUTS</span></span>

### <span data-ttu-id="0ed20-139">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. modellek. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="0ed20-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="0ed20-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ed20-140">NOTES</span></span>

<span data-ttu-id="0ed20-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0ed20-141">ALIASES</span></span>

<span data-ttu-id="0ed20-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="0ed20-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ed20-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0ed20-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ed20-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="0ed20-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ed20-145">INPUTOBJECT <IHanaOnAzureIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="0ed20-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ed20-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0ed20-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ed20-147">`[Location <String>]`: A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="0ed20-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="0ed20-148">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="0ed20-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="0ed20-149">`[ProviderInstanceName <String>]`: A szolgáltató példányának neve.</span><span class="sxs-lookup"><span data-stu-id="0ed20-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="0ed20-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ed20-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0ed20-151">`[ResourceName <String>]`: Az identitás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0ed20-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="0ed20-152">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0ed20-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="0ed20-153">`[Scope <String>]`: Az erőforrás-szolgáltató hatóköre.</span><span class="sxs-lookup"><span data-stu-id="0ed20-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="0ed20-154">A fölérendelt erőforrás a felügyelt identitások segítségével meghosszabbodik.</span><span class="sxs-lookup"><span data-stu-id="0ed20-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="0ed20-155">`[SubscriptionId <String>]`: Az előfizetés azonosítója, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0ed20-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0ed20-156">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0ed20-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0ed20-157">`[VaultName <String>]`: A boltozat neve</span><span class="sxs-lookup"><span data-stu-id="0ed20-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="0ed20-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ed20-158">RELATED LINKS</span></span>

