---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840957"
---
# <span data-ttu-id="1bae2-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="1bae2-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="1bae2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1bae2-102">SYNOPSIS</span></span>
<span data-ttu-id="1bae2-103">Adott frissítés alkalmazása a frissítés helyén</span><span class="sxs-lookup"><span data-stu-id="1bae2-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="1bae2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1bae2-104">SYNTAX</span></span>

### <span data-ttu-id="1bae2-105">Apply (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1bae2-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1bae2-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1bae2-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1bae2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1bae2-107">DESCRIPTION</span></span>
<span data-ttu-id="1bae2-108">Adott frissítés alkalmazása a frissítés helyén</span><span class="sxs-lookup"><span data-stu-id="1bae2-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="1bae2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1bae2-109">EXAMPLES</span></span>

### <span data-ttu-id="1bae2-110">Példa 1: Install-AzsUpdate név szerint</span><span class="sxs-lookup"><span data-stu-id="1bae2-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="1bae2-111">A parancsmagot lehetővé teszi bizonyos frissítések telepítését név szerint.</span><span class="sxs-lookup"><span data-stu-id="1bae2-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="1bae2-112">Felhívjuk a figyelmét arra, hogy a frissítés verziószáma szigorúan meghaladja az aktuális verziót.</span><span class="sxs-lookup"><span data-stu-id="1bae2-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="1bae2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1bae2-113">PARAMETERS</span></span>

### <span data-ttu-id="1bae2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bae2-114">-AsJob</span></span>
<span data-ttu-id="1bae2-115">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="1bae2-115">Run the command as a job</span></span>

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

### <span data-ttu-id="1bae2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bae2-116">-DefaultProfile</span></span>
<span data-ttu-id="1bae2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bae2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bae2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bae2-118">-InputObject</span></span>
<span data-ttu-id="1bae2-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1bae2-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1bae2-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="1bae2-120">-Location</span></span>
<span data-ttu-id="1bae2-121">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="1bae2-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1bae2-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1bae2-122">-Name</span></span>
<span data-ttu-id="1bae2-123">A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="1bae2-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1bae2-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="1bae2-124">-NoWait</span></span>
<span data-ttu-id="1bae2-125">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="1bae2-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1bae2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bae2-126">-ResourceGroupName</span></span>
<span data-ttu-id="1bae2-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1bae2-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1bae2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bae2-128">-SubscriptionId</span></span>
<span data-ttu-id="1bae2-129">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1bae2-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1bae2-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1bae2-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1bae2-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1bae2-131">-Confirm</span></span>
<span data-ttu-id="1bae2-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1bae2-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1bae2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bae2-133">-WhatIf</span></span>
<span data-ttu-id="1bae2-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1bae2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bae2-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1bae2-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1bae2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bae2-136">CommonParameters</span></span>
<span data-ttu-id="1bae2-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1bae2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bae2-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1bae2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bae2-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bae2-139">INPUTS</span></span>

### <span data-ttu-id="1bae2-140">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1bae2-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="1bae2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bae2-141">OUTPUTS</span></span>

### <span data-ttu-id="1bae2-142">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. modellek. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="1bae2-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="1bae2-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1bae2-143">NOTES</span></span>

<span data-ttu-id="1bae2-144">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1bae2-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1bae2-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1bae2-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1bae2-146">INPUTOBJECT <IUpdateAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1bae2-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1bae2-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1bae2-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1bae2-148">`[ResourceGroupName <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1bae2-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="1bae2-149">`[RunName <String>]`: Update Run Identifier.</span><span class="sxs-lookup"><span data-stu-id="1bae2-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="1bae2-150">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1bae2-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="1bae2-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1bae2-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1bae2-152">`[UpdateLocation <String>]`: A frissítés helyének neve.</span><span class="sxs-lookup"><span data-stu-id="1bae2-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="1bae2-153">`[UpdateName <String>]`: A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="1bae2-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="1bae2-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bae2-154">RELATED LINKS</span></span>

