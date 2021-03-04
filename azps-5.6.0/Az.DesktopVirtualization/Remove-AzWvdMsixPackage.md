---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: e0bc6fc07f03727295bc3a6babf204eaf405ae74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925625"
---
# <span data-ttu-id="af1a2-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="af1a2-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="af1a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="af1a2-103">MSIX-csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af1a2-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="af1a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="af1a2-104">SYNTAX</span></span>

### <span data-ttu-id="af1a2-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af1a2-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="af1a2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="af1a2-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af1a2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="af1a2-107">DESCRIPTION</span></span>
<span data-ttu-id="af1a2-108">MSIX-csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af1a2-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="af1a2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="af1a2-109">EXAMPLES</span></span>

### <span data-ttu-id="af1a2-110">1. példa: Az MSIX-csomag törlése teljes név szerint</span><span class="sxs-lookup"><span data-stu-id="af1a2-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="af1a2-111">Ez a parancs törli az MSIX-csomagot a HostPoolban</span><span class="sxs-lookup"><span data-stu-id="af1a2-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="af1a2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af1a2-112">PARAMETERS</span></span>

### <span data-ttu-id="af1a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af1a2-113">-DefaultProfile</span></span>
<span data-ttu-id="af1a2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af1a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af1a2-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="af1a2-115">-FullName</span></span>
<span data-ttu-id="af1a2-116">Az MSIX-csomag teljes neve a megadott állomáskészleten belül</span><span class="sxs-lookup"><span data-stu-id="af1a2-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="af1a2-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="af1a2-117">-HostPoolName</span></span>
<span data-ttu-id="af1a2-118">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="af1a2-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="af1a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af1a2-119">-InputObject</span></span>
<span data-ttu-id="af1a2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="af1a2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="af1a2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af1a2-121">-PassThru</span></span>
<span data-ttu-id="af1a2-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="af1a2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="af1a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af1a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="af1a2-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="af1a2-124">The name of the resource group.</span></span>
<span data-ttu-id="af1a2-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="af1a2-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="af1a2-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af1a2-126">-SubscriptionId</span></span>
<span data-ttu-id="af1a2-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="af1a2-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="af1a2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af1a2-128">-Confirm</span></span>
<span data-ttu-id="af1a2-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="af1a2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af1a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af1a2-130">-WhatIf</span></span>
<span data-ttu-id="af1a2-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="af1a2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af1a2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af1a2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af1a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af1a2-133">CommonParameters</span></span>
<span data-ttu-id="af1a2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af1a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af1a2-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af1a2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af1a2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af1a2-136">INPUTS</span></span>

### <span data-ttu-id="af1a2-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="af1a2-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="af1a2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af1a2-138">OUTPUTS</span></span>

### <span data-ttu-id="af1a2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af1a2-139">System.Boolean</span></span>

## <span data-ttu-id="af1a2-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="af1a2-140">NOTES</span></span>

<span data-ttu-id="af1a2-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="af1a2-141">ALIASES</span></span>

<span data-ttu-id="af1a2-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="af1a2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af1a2-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="af1a2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af1a2-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="af1a2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af1a2-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="af1a2-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af1a2-146">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="af1a2-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="af1a2-147">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="af1a2-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="af1a2-148">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="af1a2-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="af1a2-149">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="af1a2-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="af1a2-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="af1a2-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af1a2-151">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="af1a2-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="af1a2-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="af1a2-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="af1a2-153">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="af1a2-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="af1a2-154">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="af1a2-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="af1a2-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="af1a2-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="af1a2-156">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="af1a2-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="af1a2-157">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="af1a2-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="af1a2-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af1a2-158">RELATED LINKS</span></span>

