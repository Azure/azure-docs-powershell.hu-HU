---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181991"
---
# <span data-ttu-id="c05df-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="c05df-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="c05df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c05df-102">SYNOPSIS</span></span>
<span data-ttu-id="c05df-103">A megadott előfizetés, erőforráscsoport és erőforrás nevében az SAP-monitor tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="c05df-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="c05df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c05df-104">SYNTAX</span></span>

### <span data-ttu-id="c05df-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c05df-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c05df-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c05df-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c05df-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c05df-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c05df-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c05df-108">DESCRIPTION</span></span>
<span data-ttu-id="c05df-109">A megadott előfizetés, erőforráscsoport és erőforrás nevében az SAP-monitor tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="c05df-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="c05df-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c05df-110">EXAMPLES</span></span>

### <span data-ttu-id="c05df-111">Példa 1: az összes SAP-monitor lekérése az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="c05df-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="c05df-112">Ez a parancs az SAP-monitorokat az előfizetés alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="c05df-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="c05df-113">2. példa: SAP-monitor beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="c05df-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="c05df-114">Ez a parancs név szerint kapja meg az SAP-monitort.</span><span class="sxs-lookup"><span data-stu-id="c05df-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="c05df-115">3. példa: SAP-monitor lekérése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="c05df-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="c05df-116">Ez a parancs objektum szerint SAP-monitort kap.</span><span class="sxs-lookup"><span data-stu-id="c05df-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="c05df-117">Példa 4: SAP-monitor beszerzése csővezetéken</span><span class="sxs-lookup"><span data-stu-id="c05df-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="c05df-118">Ez a parancs csővezetéken keresztül SAP-monitort kap.</span><span class="sxs-lookup"><span data-stu-id="c05df-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="c05df-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c05df-119">PARAMETERS</span></span>

### <span data-ttu-id="c05df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05df-120">-DefaultProfile</span></span>
<span data-ttu-id="c05df-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c05df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c05df-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c05df-122">-InputObject</span></span>
<span data-ttu-id="c05df-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c05df-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c05df-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c05df-124">-Name</span></span>
<span data-ttu-id="c05df-125">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c05df-125">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="c05df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05df-126">-ResourceGroupName</span></span>
<span data-ttu-id="c05df-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c05df-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="c05df-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c05df-128">-SubscriptionId</span></span>
<span data-ttu-id="c05df-129">Előfizetési azonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="c05df-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c05df-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c05df-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c05df-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05df-131">CommonParameters</span></span>
<span data-ttu-id="c05df-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c05df-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05df-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c05df-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05df-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c05df-134">INPUTS</span></span>

### <span data-ttu-id="c05df-135">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="c05df-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="c05df-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c05df-136">OUTPUTS</span></span>

### <span data-ttu-id="c05df-137">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. modellek. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="c05df-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="c05df-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c05df-138">NOTES</span></span>

<span data-ttu-id="c05df-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c05df-139">ALIASES</span></span>

<span data-ttu-id="c05df-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c05df-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c05df-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c05df-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c05df-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c05df-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c05df-143">INPUTOBJECT <IHanaOnAzureIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c05df-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c05df-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c05df-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c05df-145">`[Location <String>]`: A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="c05df-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="c05df-146">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="c05df-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="c05df-147">`[ProviderInstanceName <String>]`: A szolgáltató példányának neve.</span><span class="sxs-lookup"><span data-stu-id="c05df-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="c05df-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c05df-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c05df-149">`[ResourceName <String>]`: Az identitás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c05df-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="c05df-150">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c05df-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="c05df-151">`[Scope <String>]`: Az erőforrás-szolgáltató hatóköre.</span><span class="sxs-lookup"><span data-stu-id="c05df-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="c05df-152">A fölérendelt erőforrás a felügyelt identitások segítségével meghosszabbodik.</span><span class="sxs-lookup"><span data-stu-id="c05df-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="c05df-153">`[SubscriptionId <String>]`: Az előfizetés azonosítója, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="c05df-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c05df-154">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c05df-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c05df-155">`[VaultName <String>]`: A boltozat neve</span><span class="sxs-lookup"><span data-stu-id="c05df-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="c05df-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c05df-156">RELATED LINKS</span></span>

