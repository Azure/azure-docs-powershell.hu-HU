---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015195"
---
# <span data-ttu-id="8b1d9-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="8b1d9-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="8b1d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8b1d9-103">A név alapján megtudhatja, hogy hol található a frissítés.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-103">Get an update location based on name.</span></span>

## <span data-ttu-id="8b1d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b1d9-104">SYNTAX</span></span>

### <span data-ttu-id="8b1d9-105">Get (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b1d9-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8b1d9-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8b1d9-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8b1d9-107">Lista</span><span class="sxs-lookup"><span data-stu-id="8b1d9-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b1d9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b1d9-108">DESCRIPTION</span></span>
<span data-ttu-id="8b1d9-109">A név alapján megtudhatja, hogy hol található a frissítés.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-109">Get an update location based on name.</span></span>

## <span data-ttu-id="8b1d9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8b1d9-110">EXAMPLES</span></span>

### <span data-ttu-id="8b1d9-111">Példa 1: az összes frissítés helyének beszerzése</span><span class="sxs-lookup"><span data-stu-id="8b1d9-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="8b1d9-112">Paraméterek nélkül ez a parancsmagot az összes frissítési helyet visszanyeri.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="8b1d9-113">2. példa: az összes frissítés helyének beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="8b1d9-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="8b1d9-114">Beolvassa az összes olyan frissítési helyet, amely megfelel a megadott name paraméternek.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="8b1d9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b1d9-115">PARAMETERS</span></span>

### <span data-ttu-id="8b1d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b1d9-116">-DefaultProfile</span></span>
<span data-ttu-id="8b1d9-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b1d9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b1d9-118">-InputObject</span></span>
<span data-ttu-id="8b1d9-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8b1d9-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b1d9-120">-Name</span></span>
<span data-ttu-id="8b1d9-121">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8b1d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b1d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b1d9-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8b1d9-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b1d9-124">-SubscriptionId</span></span>
<span data-ttu-id="8b1d9-125">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b1d9-126">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8b1d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b1d9-127">CommonParameters</span></span>
<span data-ttu-id="8b1d9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b1d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b1d9-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b1d9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b1d9-130">INPUTS</span></span>

### <span data-ttu-id="8b1d9-131">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8b1d9-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="8b1d9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b1d9-132">OUTPUTS</span></span>

### <span data-ttu-id="8b1d9-133">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. modellek. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="8b1d9-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="8b1d9-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b1d9-134">NOTES</span></span>

<span data-ttu-id="8b1d9-135">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b1d9-136">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8b1d9-137">INPUTOBJECT <IUpdateAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="8b1d9-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8b1d9-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8b1d9-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8b1d9-139">`[ResourceGroupName <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="8b1d9-140">`[RunName <String>]`: Update Run Identifier.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="8b1d9-141">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="8b1d9-142">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8b1d9-143">`[UpdateLocation <String>]`: A frissítés helyének neve.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="8b1d9-144">`[UpdateName <String>]`: A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="8b1d9-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b1d9-145">RELATED LINKS</span></span>

