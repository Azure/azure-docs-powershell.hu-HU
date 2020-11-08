---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017116"
---
# <span data-ttu-id="ef49d-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="ef49d-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="ef49d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef49d-102">SYNOPSIS</span></span>
<span data-ttu-id="ef49d-103">Kvóta beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="ef49d-103">Get a quota by name.</span></span>

## <span data-ttu-id="ef49d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef49d-104">SYNTAX</span></span>

### <span data-ttu-id="ef49d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef49d-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ef49d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="ef49d-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ef49d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ef49d-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="ef49d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef49d-108">DESCRIPTION</span></span>
<span data-ttu-id="ef49d-109">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="ef49d-109">List all quotas.</span></span>
<span data-ttu-id="ef49d-110">A lista korlátozása név vagy szűrő elküldésével.</span><span class="sxs-lookup"><span data-stu-id="ef49d-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="ef49d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ef49d-111">EXAMPLES</span></span>

### <span data-ttu-id="ef49d-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef49d-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="ef49d-113">Felsorolja az összes hálózati kvótát.</span><span class="sxs-lookup"><span data-stu-id="ef49d-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="ef49d-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef49d-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="ef49d-115">A megadott hálózati kvótát kapja.</span><span class="sxs-lookup"><span data-stu-id="ef49d-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="ef49d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef49d-116">PARAMETERS</span></span>

### <span data-ttu-id="ef49d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef49d-117">-DefaultProfile</span></span>
<span data-ttu-id="ef49d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef49d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef49d-119">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="ef49d-119">-Filter</span></span>
<span data-ttu-id="ef49d-120">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="ef49d-120">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ef49d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef49d-121">-InputObject</span></span>
<span data-ttu-id="ef49d-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef49d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ef49d-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="ef49d-123">-Location</span></span>
<span data-ttu-id="ef49d-124">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ef49d-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ef49d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef49d-125">-Name</span></span>
<span data-ttu-id="ef49d-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ef49d-126">Name of the resource.</span></span>

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

### <span data-ttu-id="ef49d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef49d-127">-PassThru</span></span>
<span data-ttu-id="ef49d-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="ef49d-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ef49d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef49d-129">-SubscriptionId</span></span>
<span data-ttu-id="ef49d-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ef49d-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef49d-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ef49d-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef49d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef49d-132">CommonParameters</span></span>
<span data-ttu-id="ef49d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef49d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef49d-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef49d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef49d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef49d-135">INPUTS</span></span>

### <span data-ttu-id="ef49d-136">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ef49d-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="ef49d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef49d-137">OUTPUTS</span></span>

### <span data-ttu-id="ef49d-138">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="ef49d-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="ef49d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef49d-139">NOTES</span></span>

<span data-ttu-id="ef49d-140">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ef49d-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef49d-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ef49d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ef49d-142">INPUTOBJECT <INetworkAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="ef49d-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef49d-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ef49d-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef49d-144">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ef49d-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ef49d-145">`[ResourceName <String>]`: Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ef49d-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="ef49d-146">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ef49d-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ef49d-147">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ef49d-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ef49d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef49d-148">RELATED LINKS</span></span>

