---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469917"
---
# <span data-ttu-id="b8e39-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="b8e39-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="b8e39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8e39-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e39-103">MSIX-csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b8e39-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="b8e39-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8e39-104">SYNTAX</span></span>

### <span data-ttu-id="b8e39-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8e39-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8e39-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8e39-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8e39-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8e39-107">DESCRIPTION</span></span>
<span data-ttu-id="b8e39-108">MSIX-csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b8e39-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="b8e39-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8e39-109">EXAMPLES</span></span>

### <span data-ttu-id="b8e39-110">1. példa: Az MSIX-csomag törlése teljes név szerint</span><span class="sxs-lookup"><span data-stu-id="b8e39-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="b8e39-111">Ez a parancs törli az MSIX-csomagot a HostPoolban</span><span class="sxs-lookup"><span data-stu-id="b8e39-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="b8e39-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8e39-112">PARAMETERS</span></span>

### <span data-ttu-id="b8e39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e39-113">-DefaultProfile</span></span>
<span data-ttu-id="b8e39-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8e39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8e39-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="b8e39-115">-FullName</span></span>
<span data-ttu-id="b8e39-116">Az MSIX-csomag teljes neve a megadott állomáskészleten belül</span><span class="sxs-lookup"><span data-stu-id="b8e39-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e39-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b8e39-117">-HostPoolName</span></span>
<span data-ttu-id="b8e39-118">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="b8e39-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b8e39-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8e39-119">-InputObject</span></span>
<span data-ttu-id="b8e39-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b8e39-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8e39-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8e39-121">-PassThru</span></span>
<span data-ttu-id="b8e39-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="b8e39-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b8e39-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e39-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8e39-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8e39-124">The name of the resource group.</span></span>
<span data-ttu-id="b8e39-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b8e39-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b8e39-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8e39-126">-SubscriptionId</span></span>
<span data-ttu-id="b8e39-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b8e39-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b8e39-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8e39-128">-Confirm</span></span>
<span data-ttu-id="b8e39-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b8e39-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e39-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e39-130">-WhatIf</span></span>
<span data-ttu-id="b8e39-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b8e39-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e39-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8e39-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e39-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e39-133">CommonParameters</span></span>
<span data-ttu-id="b8e39-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8e39-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e39-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8e39-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e39-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8e39-136">INPUTS</span></span>

### <span data-ttu-id="b8e39-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b8e39-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b8e39-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8e39-138">OUTPUTS</span></span>

### <span data-ttu-id="b8e39-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8e39-139">System.Boolean</span></span>

## <span data-ttu-id="b8e39-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8e39-140">NOTES</span></span>

<span data-ttu-id="b8e39-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b8e39-141">ALIASES</span></span>

<span data-ttu-id="b8e39-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b8e39-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8e39-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b8e39-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8e39-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b8e39-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8e39-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b8e39-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8e39-146">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b8e39-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b8e39-147">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="b8e39-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b8e39-148">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="b8e39-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b8e39-149">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="b8e39-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b8e39-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b8e39-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8e39-151">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="b8e39-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b8e39-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8e39-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b8e39-153">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b8e39-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="b8e39-154">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="b8e39-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b8e39-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b8e39-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b8e39-156">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="b8e39-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b8e39-157">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="b8e39-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b8e39-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8e39-158">RELATED LINKS</span></span>

