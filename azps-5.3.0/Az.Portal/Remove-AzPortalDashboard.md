---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467273"
---
# <span data-ttu-id="6cce0-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="6cce0-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="6cce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cce0-102">SYNOPSIS</span></span>
<span data-ttu-id="6cce0-103">Törli az irányítópultot.</span><span class="sxs-lookup"><span data-stu-id="6cce0-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="6cce0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cce0-104">SYNTAX</span></span>

### <span data-ttu-id="6cce0-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cce0-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6cce0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6cce0-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cce0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cce0-107">DESCRIPTION</span></span>
<span data-ttu-id="6cce0-108">Törli az irányítópultot.</span><span class="sxs-lookup"><span data-stu-id="6cce0-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="6cce0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cce0-109">EXAMPLES</span></span>

### <span data-ttu-id="6cce0-110">1. példa: Irányítópult eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6cce0-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="6cce0-111">Szaggatottszó eltávolítása az erőforráscsoport és az irányítópult nevével.</span><span class="sxs-lookup"><span data-stu-id="6cce0-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="6cce0-112">2. példa: Irányítópult eltávolítása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="6cce0-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="6cce0-113">Távolítsa el a visszaküldött irányítópultot egy Get-AzDashboard hívásból.</span><span class="sxs-lookup"><span data-stu-id="6cce0-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="6cce0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cce0-114">PARAMETERS</span></span>

### <span data-ttu-id="6cce0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cce0-115">-DefaultProfile</span></span>
<span data-ttu-id="6cce0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cce0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cce0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cce0-117">-InputObject</span></span>
<span data-ttu-id="6cce0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6cce0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6cce0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6cce0-119">-Name</span></span>
<span data-ttu-id="6cce0-120">Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="6cce0-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="6cce0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cce0-121">-PassThru</span></span>
<span data-ttu-id="6cce0-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="6cce0-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6cce0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cce0-123">-ResourceGroupName</span></span>
<span data-ttu-id="6cce0-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cce0-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cce0-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cce0-125">-SubscriptionId</span></span>
<span data-ttu-id="6cce0-126">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cce0-126">The Azure subscription ID.</span></span>
<span data-ttu-id="6cce0-127">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="6cce0-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6cce0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cce0-128">-Confirm</span></span>
<span data-ttu-id="6cce0-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cce0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cce0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cce0-130">-WhatIf</span></span>
<span data-ttu-id="6cce0-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6cce0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cce0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cce0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cce0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cce0-133">CommonParameters</span></span>
<span data-ttu-id="6cce0-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cce0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cce0-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cce0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cce0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cce0-136">INPUTS</span></span>

### <span data-ttu-id="6cce0-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="6cce0-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="6cce0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cce0-138">OUTPUTS</span></span>

### <span data-ttu-id="6cce0-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6cce0-139">System.Boolean</span></span>

## <span data-ttu-id="6cce0-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cce0-140">NOTES</span></span>

<span data-ttu-id="6cce0-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6cce0-141">ALIASES</span></span>

<span data-ttu-id="6cce0-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6cce0-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cce0-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6cce0-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cce0-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cce0-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cce0-145">INPUTOBJECT: <IPortalIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6cce0-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cce0-146">`[DashboardName <String>]`: Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="6cce0-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="6cce0-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6cce0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cce0-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cce0-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6cce0-149">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cce0-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6cce0-150">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="6cce0-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6cce0-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cce0-151">RELATED LINKS</span></span>

