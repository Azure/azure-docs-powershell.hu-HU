---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 30c0734656b79f532c56b47b64e9d7e918f92fa8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017789"
---
# <span data-ttu-id="5b3d5-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="5b3d5-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="5b3d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3d5-103">Munkaterület frissítése</span><span class="sxs-lookup"><span data-stu-id="5b3d5-103">Update a workspace.</span></span>

## <span data-ttu-id="5b3d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b3d5-104">SYNTAX</span></span>

### <span data-ttu-id="5b3d5-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b3d5-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5b3d5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5b3d5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b3d5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b3d5-107">DESCRIPTION</span></span>
<span data-ttu-id="5b3d5-108">Munkaterület frissítése</span><span class="sxs-lookup"><span data-stu-id="5b3d5-108">Update a workspace.</span></span>

## <span data-ttu-id="5b3d5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5b3d5-109">EXAMPLES</span></span>

### <span data-ttu-id="5b3d5-110">Példa 1: a Windows virtuális asztali Worksapce frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="5b3d5-110">Example 1: Update a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="5b3d5-111">Ez a parancs frissíti egy Windows virtuális asztali munkaterületet egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="5b3d5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b3d5-112">PARAMETERS</span></span>

### <span data-ttu-id="5b3d5-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="5b3d5-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="5b3d5-114">A applicationGroup hivatkozásainak listája</span><span class="sxs-lookup"><span data-stu-id="5b3d5-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3d5-115">-DefaultProfile</span></span>
<span data-ttu-id="5b3d5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b3d5-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5b3d5-117">-Description</span></span>
<span data-ttu-id="5b3d5-118">A munkaterület leírása.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-118">Description of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3d5-119">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="5b3d5-119">-FriendlyName</span></span>
<span data-ttu-id="5b3d5-120">A munkaterület rövid neve.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-120">Friendly name of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b3d5-121">-InputObject</span></span>
<span data-ttu-id="5b3d5-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3d5-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b3d5-123">-Name</span></span>
<span data-ttu-id="5b3d5-124">A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="5b3d5-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b3d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b3d5-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-126">The name of the resource group.</span></span>
<span data-ttu-id="5b3d5-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3d5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b3d5-128">-SubscriptionId</span></span>
<span data-ttu-id="5b3d5-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3d5-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="5b3d5-130">-Tag</span></span>
<span data-ttu-id="5b3d5-131">frissítendő Címkék</span><span class="sxs-lookup"><span data-stu-id="5b3d5-131">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3d5-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b3d5-132">-Confirm</span></span>
<span data-ttu-id="5b3d5-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b3d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b3d5-134">-WhatIf</span></span>
<span data-ttu-id="5b3d5-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b3d5-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b3d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3d5-137">CommonParameters</span></span>
<span data-ttu-id="5b3d5-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b3d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3d5-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3d5-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b3d5-140">INPUTS</span></span>

### <span data-ttu-id="5b3d5-141">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5b3d5-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5b3d5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b3d5-142">OUTPUTS</span></span>

### <span data-ttu-id="5b3d5-143">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="5b3d5-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="5b3d5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b3d5-144">NOTES</span></span>

<span data-ttu-id="5b3d5-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5b3d5-145">ALIASES</span></span>

<span data-ttu-id="5b3d5-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="5b3d5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b3d5-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b3d5-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b3d5-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5b3d5-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b3d5-150">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="5b3d5-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5b3d5-151">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="5b3d5-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5b3d5-152">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="5b3d5-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5b3d5-153">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="5b3d5-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5b3d5-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5b3d5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b3d5-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5b3d5-156">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="5b3d5-157">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="5b3d5-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5b3d5-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5b3d5-159">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="5b3d5-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5b3d5-160">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="5b3d5-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5b3d5-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b3d5-161">RELATED LINKS</span></span>

