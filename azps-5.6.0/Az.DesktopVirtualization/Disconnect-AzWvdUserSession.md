---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 61e1eb1f5ae3846ce2f0cf7ad82d17d613d27e0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925714"
---
# <span data-ttu-id="ef4ff-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="ef4ff-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="ef4ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4ff-103">Felhasználó leválasztása</span><span class="sxs-lookup"><span data-stu-id="ef4ff-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="ef4ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef4ff-104">SYNTAX</span></span>

### <span data-ttu-id="ef4ff-105">Kapcsolat bontása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef4ff-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ef4ff-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ef4ff-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef4ff-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef4ff-107">DESCRIPTION</span></span>
<span data-ttu-id="ef4ff-108">Felhasználó leválasztása</span><span class="sxs-lookup"><span data-stu-id="ef4ff-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="ef4ff-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef4ff-109">EXAMPLES</span></span>

### <span data-ttu-id="ef4ff-110">1. példa: A Windows virtuális asztali felhasználói fiókok leválasztása név szerint</span><span class="sxs-lookup"><span data-stu-id="ef4ff-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="ef4ff-111">Ez a parancs megszakítja a Windows virtuális asztali felhasználós munkamenetének munkamenetgazdában való csatlakozását.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="ef4ff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef4ff-112">PARAMETERS</span></span>

### <span data-ttu-id="ef4ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4ff-113">-DefaultProfile</span></span>
<span data-ttu-id="ef4ff-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4ff-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ef4ff-115">-HostPoolName</span></span>
<span data-ttu-id="ef4ff-116">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="ef4ff-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ff-117">-Id</span><span class="sxs-lookup"><span data-stu-id="ef4ff-117">-Id</span></span>
<span data-ttu-id="ef4ff-118">A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="ef4ff-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ff-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef4ff-119">-InputObject</span></span>
<span data-ttu-id="ef4ff-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ff-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef4ff-121">-PassThru</span></span>
<span data-ttu-id="ef4ff-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="ef4ff-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ef4ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef4ff-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-124">The name of the resource group.</span></span>
<span data-ttu-id="ef4ff-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ef4ff-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ff-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="ef4ff-126">-SessionHostName</span></span>
<span data-ttu-id="ef4ff-127">A munkamenetgazda neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="ef4ff-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ff-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef4ff-128">-SubscriptionId</span></span>
<span data-ttu-id="ef4ff-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ff-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef4ff-130">-Confirm</span></span>
<span data-ttu-id="ef4ff-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef4ff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef4ff-132">-WhatIf</span></span>
<span data-ttu-id="ef4ff-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef4ff-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef4ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4ff-135">CommonParameters</span></span>
<span data-ttu-id="ef4ff-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4ff-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef4ff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4ff-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef4ff-138">INPUTS</span></span>

### <span data-ttu-id="ef4ff-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ef4ff-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ef4ff-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef4ff-140">OUTPUTS</span></span>

### <span data-ttu-id="ef4ff-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef4ff-141">System.Boolean</span></span>

## <span data-ttu-id="ef4ff-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef4ff-142">NOTES</span></span>

<span data-ttu-id="ef4ff-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ef4ff-143">ALIASES</span></span>

<span data-ttu-id="ef4ff-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ef4ff-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef4ff-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef4ff-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef4ff-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ef4ff-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef4ff-148">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ef4ff-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ef4ff-149">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="ef4ff-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ef4ff-150">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="ef4ff-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ef4ff-151">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="ef4ff-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ef4ff-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ef4ff-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef4ff-153">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="ef4ff-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ef4ff-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ef4ff-155">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ef4ff-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="ef4ff-156">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="ef4ff-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ef4ff-157">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ef4ff-158">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="ef4ff-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ef4ff-159">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="ef4ff-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ef4ff-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef4ff-160">RELATED LINKS</span></span>

