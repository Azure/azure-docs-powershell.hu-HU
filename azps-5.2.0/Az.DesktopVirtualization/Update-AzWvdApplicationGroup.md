---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: 239d1a5a38d2eb344f584e006d465598b43dd546
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341093"
---
# <span data-ttu-id="c26ec-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c26ec-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c26ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c26ec-103">Frissítsen egy alkalmazáscsoportot.</span><span class="sxs-lookup"><span data-stu-id="c26ec-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="c26ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c26ec-104">SYNTAX</span></span>

### <span data-ttu-id="c26ec-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c26ec-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c26ec-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c26ec-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c26ec-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c26ec-107">DESCRIPTION</span></span>
<span data-ttu-id="c26ec-108">Frissítsen egy alkalmazáscsoportot.</span><span class="sxs-lookup"><span data-stu-id="c26ec-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="c26ec-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c26ec-109">EXAMPLES</span></span>

### <span data-ttu-id="c26ec-110">1. példa: Windows Virtuális asztali alkalmazáscsoport létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="c26ec-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="c26ec-111">Ez a parancs létrehoz egy Windows virtuális asztali alkalmazáscsoportot egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c26ec-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="c26ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c26ec-112">PARAMETERS</span></span>

### <span data-ttu-id="c26ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26ec-113">-DefaultProfile</span></span>
<span data-ttu-id="c26ec-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c26ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c26ec-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c26ec-115">-Description</span></span>
<span data-ttu-id="c26ec-116">Az ApplicationGroup leírása.</span><span class="sxs-lookup"><span data-stu-id="c26ec-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="c26ec-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c26ec-117">-FriendlyName</span></span>
<span data-ttu-id="c26ec-118">Az ApplicationGroup rövid neve.</span><span class="sxs-lookup"><span data-stu-id="c26ec-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="c26ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c26ec-119">-InputObject</span></span>
<span data-ttu-id="c26ec-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c26ec-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c26ec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c26ec-121">-Name</span></span>
<span data-ttu-id="c26ec-122">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c26ec-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c26ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="c26ec-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c26ec-124">The name of the resource group.</span></span>
<span data-ttu-id="c26ec-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c26ec-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c26ec-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c26ec-126">-SubscriptionId</span></span>
<span data-ttu-id="c26ec-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c26ec-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c26ec-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="c26ec-128">-Tag</span></span>
<span data-ttu-id="c26ec-129">frissítend kell a címkéket</span><span class="sxs-lookup"><span data-stu-id="c26ec-129">tags to be updated</span></span>

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

### <span data-ttu-id="c26ec-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c26ec-130">-Confirm</span></span>
<span data-ttu-id="c26ec-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c26ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c26ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c26ec-132">-WhatIf</span></span>
<span data-ttu-id="c26ec-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c26ec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c26ec-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c26ec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c26ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26ec-135">CommonParameters</span></span>
<span data-ttu-id="c26ec-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c26ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26ec-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c26ec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26ec-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c26ec-138">INPUTS</span></span>

### <span data-ttu-id="c26ec-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c26ec-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c26ec-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c26ec-140">OUTPUTS</span></span>

### <span data-ttu-id="c26ec-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c26ec-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="c26ec-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c26ec-142">NOTES</span></span>

<span data-ttu-id="c26ec-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c26ec-143">ALIASES</span></span>

<span data-ttu-id="c26ec-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c26ec-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c26ec-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c26ec-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c26ec-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c26ec-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c26ec-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c26ec-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c26ec-148">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c26ec-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c26ec-149">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="c26ec-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c26ec-150">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="c26ec-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c26ec-151">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="c26ec-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c26ec-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c26ec-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c26ec-153">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="c26ec-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c26ec-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c26ec-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c26ec-155">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c26ec-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="c26ec-156">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="c26ec-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c26ec-157">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c26ec-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c26ec-158">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="c26ec-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c26ec-159">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="c26ec-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c26ec-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c26ec-160">RELATED LINKS</span></span>

