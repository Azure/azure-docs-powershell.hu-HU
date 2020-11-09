---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: f7bad3a88f4d182407a90a2484daed3d538e3a69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296990"
---
# <span data-ttu-id="4f811-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="4f811-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="4f811-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f811-102">SYNOPSIS</span></span>
<span data-ttu-id="4f811-103">Távolítson el egy SessionHost.</span><span class="sxs-lookup"><span data-stu-id="4f811-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="4f811-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f811-104">SYNTAX</span></span>

### <span data-ttu-id="4f811-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f811-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4f811-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f811-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4f811-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f811-107">DESCRIPTION</span></span>
<span data-ttu-id="4f811-108">Távolítson el egy SessionHost.</span><span class="sxs-lookup"><span data-stu-id="4f811-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="4f811-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4f811-109">EXAMPLES</span></span>

### <span data-ttu-id="4f811-110">Példa 1: a Windows virtuális asztali SessionHost törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="4f811-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="4f811-111">Ez a parancs törli a Windows virtuális asztali SessionHost egy állomás-készletben.</span><span class="sxs-lookup"><span data-stu-id="4f811-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="4f811-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f811-112">PARAMETERS</span></span>

### <span data-ttu-id="4f811-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f811-113">-DefaultProfile</span></span>
<span data-ttu-id="4f811-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f811-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f811-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4f811-115">-Force</span></span>
<span data-ttu-id="4f811-116">Kényszerített jelölő: a sessionHost törlésének kényszerítése akkor is, ha a userSession létezik.</span><span class="sxs-lookup"><span data-stu-id="4f811-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="4f811-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4f811-117">-HostPoolName</span></span>
<span data-ttu-id="4f811-118">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="4f811-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="4f811-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f811-119">-InputObject</span></span>
<span data-ttu-id="4f811-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f811-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f811-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4f811-121">-Name</span></span>
<span data-ttu-id="4f811-122">A megadott alkalmazáskészleten belüli munkamenet-állomás neve</span><span class="sxs-lookup"><span data-stu-id="4f811-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f811-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f811-123">-PassThru</span></span>
<span data-ttu-id="4f811-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="4f811-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4f811-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f811-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f811-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4f811-126">The name of the resource group.</span></span>
<span data-ttu-id="4f811-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="4f811-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4f811-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f811-128">-SubscriptionId</span></span>
<span data-ttu-id="4f811-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4f811-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4f811-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f811-130">-Confirm</span></span>
<span data-ttu-id="4f811-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f811-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f811-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f811-132">-WhatIf</span></span>
<span data-ttu-id="4f811-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f811-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f811-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f811-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f811-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f811-135">CommonParameters</span></span>
<span data-ttu-id="4f811-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f811-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f811-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f811-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f811-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f811-138">INPUTS</span></span>

### <span data-ttu-id="4f811-139">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4f811-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4f811-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f811-140">OUTPUTS</span></span>

### <span data-ttu-id="4f811-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f811-141">System.Boolean</span></span>

## <span data-ttu-id="4f811-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f811-142">NOTES</span></span>

<span data-ttu-id="4f811-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4f811-143">ALIASES</span></span>

<span data-ttu-id="4f811-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="4f811-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f811-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4f811-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f811-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4f811-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f811-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="4f811-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f811-148">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="4f811-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4f811-149">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="4f811-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4f811-150">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="4f811-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4f811-151">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="4f811-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4f811-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4f811-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f811-153">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4f811-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4f811-154">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="4f811-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="4f811-155">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="4f811-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4f811-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4f811-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4f811-157">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="4f811-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4f811-158">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="4f811-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4f811-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f811-159">RELATED LINKS</span></span>

