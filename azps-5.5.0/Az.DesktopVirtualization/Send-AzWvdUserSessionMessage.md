---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 5b5e5ba314bee8d6260985c65f46d372cce94258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153267"
---
# <span data-ttu-id="62344-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="62344-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="62344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62344-102">SYNOPSIS</span></span>
<span data-ttu-id="62344-103">Küldjön egy üzenetet egy felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="62344-103">Send a message to a user.</span></span>

## <span data-ttu-id="62344-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62344-104">SYNTAX</span></span>

### <span data-ttu-id="62344-105">SendExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62344-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62344-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="62344-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62344-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62344-107">DESCRIPTION</span></span>
<span data-ttu-id="62344-108">Küldjön egy üzenetet egy felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="62344-108">Send a message to a user.</span></span>

## <span data-ttu-id="62344-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62344-109">EXAMPLES</span></span>

### <span data-ttu-id="62344-110">1. példa: Üzenet küldése a UserSession rendszernek</span><span class="sxs-lookup"><span data-stu-id="62344-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="62344-111">Ez a parancs üzenetet küld a UserSession felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="62344-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="62344-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62344-112">PARAMETERS</span></span>

### <span data-ttu-id="62344-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62344-113">-DefaultProfile</span></span>
<span data-ttu-id="62344-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62344-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62344-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="62344-115">-HostPoolName</span></span>
<span data-ttu-id="62344-116">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="62344-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62344-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62344-117">-InputObject</span></span>
<span data-ttu-id="62344-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="62344-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62344-119">-Message Minden</span><span class="sxs-lookup"><span data-stu-id="62344-119">-MessageBody</span></span>
<span data-ttu-id="62344-120">Üzenet törzse.</span><span class="sxs-lookup"><span data-stu-id="62344-120">Body of message.</span></span>

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

### <span data-ttu-id="62344-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="62344-121">-MessageTitle</span></span>
<span data-ttu-id="62344-122">Az üzenet címe.</span><span class="sxs-lookup"><span data-stu-id="62344-122">Title of message.</span></span>

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

### <span data-ttu-id="62344-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62344-123">-PassThru</span></span>
<span data-ttu-id="62344-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="62344-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="62344-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62344-125">-ResourceGroupName</span></span>
<span data-ttu-id="62344-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="62344-126">The name of the resource group.</span></span>
<span data-ttu-id="62344-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="62344-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62344-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="62344-128">-SessionHostName</span></span>
<span data-ttu-id="62344-129">A munkamenetgazda neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="62344-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62344-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62344-130">-SubscriptionId</span></span>
<span data-ttu-id="62344-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62344-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62344-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="62344-132">-UserSessionId</span></span>
<span data-ttu-id="62344-133">A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="62344-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62344-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62344-134">-Confirm</span></span>
<span data-ttu-id="62344-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="62344-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62344-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62344-136">-WhatIf</span></span>
<span data-ttu-id="62344-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="62344-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62344-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62344-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62344-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62344-139">CommonParameters</span></span>
<span data-ttu-id="62344-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62344-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62344-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62344-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62344-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62344-142">INPUTS</span></span>

### <span data-ttu-id="62344-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="62344-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="62344-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62344-144">OUTPUTS</span></span>

### <span data-ttu-id="62344-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62344-145">System.Boolean</span></span>

## <span data-ttu-id="62344-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62344-146">NOTES</span></span>

<span data-ttu-id="62344-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="62344-147">ALIASES</span></span>

<span data-ttu-id="62344-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="62344-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62344-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="62344-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62344-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62344-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62344-151">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="62344-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62344-152">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="62344-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="62344-153">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="62344-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="62344-154">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="62344-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="62344-155">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="62344-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="62344-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="62344-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62344-157">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="62344-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="62344-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="62344-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="62344-159">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="62344-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="62344-160">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="62344-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="62344-161">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62344-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="62344-162">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="62344-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="62344-163">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="62344-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="62344-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62344-164">RELATED LINKS</span></span>

