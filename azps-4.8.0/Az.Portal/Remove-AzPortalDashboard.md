---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184279"
---
# <span data-ttu-id="906f2-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="906f2-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="906f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="906f2-102">SYNOPSIS</span></span>
<span data-ttu-id="906f2-103">Az irányítópult törlése</span><span class="sxs-lookup"><span data-stu-id="906f2-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="906f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="906f2-104">SYNTAX</span></span>

### <span data-ttu-id="906f2-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="906f2-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="906f2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="906f2-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="906f2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="906f2-107">DESCRIPTION</span></span>
<span data-ttu-id="906f2-108">Az irányítópult törlése</span><span class="sxs-lookup"><span data-stu-id="906f2-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="906f2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="906f2-109">EXAMPLES</span></span>

### <span data-ttu-id="906f2-110">1. példa: irányítópult eltávolítása</span><span class="sxs-lookup"><span data-stu-id="906f2-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="906f2-111">Dashbaord eltávolítása az erőforráscsoport neve és az irányítópult neve segítségével</span><span class="sxs-lookup"><span data-stu-id="906f2-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="906f2-112">2. példa: irányítópult eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="906f2-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="906f2-113">Get-AzDashboard hívásból visszaadott irányítópult eltávolítása</span><span class="sxs-lookup"><span data-stu-id="906f2-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="906f2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="906f2-114">PARAMETERS</span></span>

### <span data-ttu-id="906f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906f2-115">-DefaultProfile</span></span>
<span data-ttu-id="906f2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="906f2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="906f2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="906f2-117">-InputObject</span></span>
<span data-ttu-id="906f2-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="906f2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="906f2-119">-Name</span></span>
<span data-ttu-id="906f2-120">Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="906f2-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="906f2-121">-PassThru</span></span>
<span data-ttu-id="906f2-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="906f2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="906f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="906f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="906f2-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="906f2-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="906f2-125">-SubscriptionId</span></span>
<span data-ttu-id="906f2-126">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="906f2-126">The Azure subscription ID.</span></span>
<span data-ttu-id="906f2-127">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="906f2-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="906f2-128">-Confirm</span></span>
<span data-ttu-id="906f2-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="906f2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="906f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="906f2-130">-WhatIf</span></span>
<span data-ttu-id="906f2-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="906f2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="906f2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="906f2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="906f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906f2-133">CommonParameters</span></span>
<span data-ttu-id="906f2-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="906f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906f2-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="906f2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906f2-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="906f2-136">INPUTS</span></span>

### <span data-ttu-id="906f2-137">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="906f2-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="906f2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="906f2-138">OUTPUTS</span></span>

### <span data-ttu-id="906f2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="906f2-139">System.Boolean</span></span>

## <span data-ttu-id="906f2-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="906f2-140">NOTES</span></span>

<span data-ttu-id="906f2-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="906f2-141">ALIASES</span></span>

<span data-ttu-id="906f2-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="906f2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="906f2-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="906f2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="906f2-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="906f2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="906f2-145">INPUTOBJECT <IPortalIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="906f2-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="906f2-146">`[DashboardName <String>]`: Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="906f2-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="906f2-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="906f2-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="906f2-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="906f2-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="906f2-149">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="906f2-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="906f2-150">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="906f2-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="906f2-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="906f2-151">RELATED LINKS</span></span>

