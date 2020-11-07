---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840958"
---
# <span data-ttu-id="a6e55-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="a6e55-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="a6e55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6e55-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e55-103">Frissítsen egy bizonyos frissítést egy frissítési helyen.</span><span class="sxs-lookup"><span data-stu-id="a6e55-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="a6e55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6e55-104">SYNTAX</span></span>

### <span data-ttu-id="a6e55-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6e55-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a6e55-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a6e55-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a6e55-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6e55-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a6e55-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6e55-108">DESCRIPTION</span></span>
<span data-ttu-id="a6e55-109">Frissítsen egy bizonyos frissítést egy frissítési helyen.</span><span class="sxs-lookup"><span data-stu-id="a6e55-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="a6e55-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a6e55-110">EXAMPLES</span></span>

### <span data-ttu-id="a6e55-111">Példa 1: az összes frissítés beszerzése</span><span class="sxs-lookup"><span data-stu-id="a6e55-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="a6e55-112">Paraméterek nélkül a Get-AzsUpdate felsorolja a bélyegző által felfedezhető összes frissítést</span><span class="sxs-lookup"><span data-stu-id="a6e55-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="a6e55-113">2. példa: a frissítés kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="a6e55-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="a6e55-114">A megadott névhez tartozó összes frissítés visszakeresése</span><span class="sxs-lookup"><span data-stu-id="a6e55-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="a6e55-115">3. példa: a frissítések hely szerinti lekérése</span><span class="sxs-lookup"><span data-stu-id="a6e55-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="a6e55-116">A megadott helyen lévő összes frissítést lekéri.</span><span class="sxs-lookup"><span data-stu-id="a6e55-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="a6e55-117">Jelenleg csak egy hely támogatott, ezért ez a beállítás csak a megfelelő Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="a6e55-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="a6e55-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6e55-118">PARAMETERS</span></span>

### <span data-ttu-id="a6e55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e55-119">-DefaultProfile</span></span>
<span data-ttu-id="a6e55-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6e55-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6e55-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6e55-121">-InputObject</span></span>
<span data-ttu-id="a6e55-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a6e55-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6e55-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="a6e55-123">-Location</span></span>
<span data-ttu-id="a6e55-124">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="a6e55-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a6e55-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6e55-125">-Name</span></span>
<span data-ttu-id="a6e55-126">A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="a6e55-126">Name of the update.</span></span>

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

### <span data-ttu-id="a6e55-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e55-127">-ResourceGroupName</span></span>
<span data-ttu-id="a6e55-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a6e55-128">Resource group name.</span></span>

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

### <span data-ttu-id="a6e55-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6e55-129">-SubscriptionId</span></span>
<span data-ttu-id="a6e55-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a6e55-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a6e55-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a6e55-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a6e55-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e55-132">CommonParameters</span></span>
<span data-ttu-id="a6e55-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6e55-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e55-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a6e55-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e55-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6e55-135">INPUTS</span></span>

### <span data-ttu-id="a6e55-136">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a6e55-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="a6e55-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6e55-137">OUTPUTS</span></span>

### <span data-ttu-id="a6e55-138">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. modellek. Api20160501. IUpdate</span><span class="sxs-lookup"><span data-stu-id="a6e55-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="a6e55-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6e55-139">NOTES</span></span>

<span data-ttu-id="a6e55-140">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a6e55-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6e55-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a6e55-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a6e55-142">INPUTOBJECT <IUpdateAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a6e55-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6e55-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a6e55-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6e55-144">`[ResourceGroupName <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a6e55-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="a6e55-145">`[RunName <String>]`: Update Run Identifier.</span><span class="sxs-lookup"><span data-stu-id="a6e55-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="a6e55-146">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a6e55-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="a6e55-147">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a6e55-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a6e55-148">`[UpdateLocation <String>]`: A frissítés helyének neve.</span><span class="sxs-lookup"><span data-stu-id="a6e55-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="a6e55-149">`[UpdateName <String>]`: A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="a6e55-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="a6e55-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6e55-150">RELATED LINKS</span></span>

