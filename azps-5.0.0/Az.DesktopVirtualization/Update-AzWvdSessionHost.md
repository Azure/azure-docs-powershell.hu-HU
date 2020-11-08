---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185572"
---
# <span data-ttu-id="78024-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="78024-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="78024-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78024-102">SYNOPSIS</span></span>
<span data-ttu-id="78024-103">Munkamenet-állomás frissítése</span><span class="sxs-lookup"><span data-stu-id="78024-103">Update a session host.</span></span>

## <span data-ttu-id="78024-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78024-104">SYNTAX</span></span>

### <span data-ttu-id="78024-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78024-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="78024-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="78024-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78024-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="78024-107">DESCRIPTION</span></span>
<span data-ttu-id="78024-108">Munkamenet-állomás frissítése</span><span class="sxs-lookup"><span data-stu-id="78024-108">Update a session host.</span></span>

## <span data-ttu-id="78024-109">Példák</span><span class="sxs-lookup"><span data-stu-id="78024-109">EXAMPLES</span></span>

### <span data-ttu-id="78024-110">Példa 1: a Windows virtuális asztali SessionHost frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="78024-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="78024-111">Ez a parancs frissíti a Windows virtuális asztali SessionHost egy alkalmazáskészletben.</span><span class="sxs-lookup"><span data-stu-id="78024-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="78024-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78024-112">PARAMETERS</span></span>

### <span data-ttu-id="78024-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="78024-113">-AllowNewSession</span></span>
<span data-ttu-id="78024-114">Új munkamenet engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="78024-114">Allow a new session.</span></span>

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

### <span data-ttu-id="78024-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="78024-115">-AssignedUser</span></span>
<span data-ttu-id="78024-116">Felhasználó a SessionHost-hoz rendelve.</span><span class="sxs-lookup"><span data-stu-id="78024-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="78024-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78024-117">-DefaultProfile</span></span>
<span data-ttu-id="78024-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78024-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78024-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="78024-119">-HostPoolName</span></span>
<span data-ttu-id="78024-120">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="78024-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="78024-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78024-121">-InputObject</span></span>
<span data-ttu-id="78024-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78024-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="78024-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78024-123">-Name</span></span>
<span data-ttu-id="78024-124">A megadott alkalmazáskészleten belüli munkamenet-állomás neve</span><span class="sxs-lookup"><span data-stu-id="78024-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78024-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78024-125">-ResourceGroupName</span></span>
<span data-ttu-id="78024-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="78024-126">The name of the resource group.</span></span>
<span data-ttu-id="78024-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="78024-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="78024-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78024-128">-SubscriptionId</span></span>
<span data-ttu-id="78024-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="78024-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="78024-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78024-130">-Confirm</span></span>
<span data-ttu-id="78024-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78024-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78024-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78024-132">-WhatIf</span></span>
<span data-ttu-id="78024-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78024-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78024-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78024-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78024-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78024-135">CommonParameters</span></span>
<span data-ttu-id="78024-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78024-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78024-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78024-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78024-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78024-138">INPUTS</span></span>

### <span data-ttu-id="78024-139">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="78024-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="78024-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78024-140">OUTPUTS</span></span>

### <span data-ttu-id="78024-141">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="78024-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="78024-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78024-142">NOTES</span></span>

<span data-ttu-id="78024-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="78024-143">ALIASES</span></span>

<span data-ttu-id="78024-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="78024-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78024-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="78024-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78024-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="78024-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78024-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="78024-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78024-148">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="78024-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="78024-149">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="78024-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="78024-150">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="78024-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="78024-151">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="78024-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="78024-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="78024-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78024-153">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="78024-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="78024-154">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="78024-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="78024-155">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="78024-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="78024-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="78024-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="78024-157">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="78024-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="78024-158">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="78024-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="78024-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78024-159">RELATED LINKS</span></span>

