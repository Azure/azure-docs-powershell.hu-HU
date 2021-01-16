---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328953"
---
# <span data-ttu-id="22cb1-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="22cb1-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="22cb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="22cb1-103">MSIX-csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="22cb1-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="22cb1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22cb1-104">SYNTAX</span></span>

### <span data-ttu-id="22cb1-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22cb1-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="22cb1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="22cb1-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="22cb1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22cb1-107">DESCRIPTION</span></span>
<span data-ttu-id="22cb1-108">MSIX-csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="22cb1-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="22cb1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22cb1-109">EXAMPLES</span></span>

### <span data-ttu-id="22cb1-110">1. példa: Az MSIX-csomag törlése teljes név szerint</span><span class="sxs-lookup"><span data-stu-id="22cb1-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="22cb1-111">Ez a parancs törli az MSIX-csomagot a HostPoolban</span><span class="sxs-lookup"><span data-stu-id="22cb1-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="22cb1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22cb1-112">PARAMETERS</span></span>

### <span data-ttu-id="22cb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cb1-113">-DefaultProfile</span></span>
<span data-ttu-id="22cb1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22cb1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cb1-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="22cb1-115">-FullName</span></span>
<span data-ttu-id="22cb1-116">A verzióspecifikus csomag teljes neve az MSIX-csomagnak a megadott állomássoron belül</span><span class="sxs-lookup"><span data-stu-id="22cb1-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="22cb1-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="22cb1-117">-HostPoolName</span></span>
<span data-ttu-id="22cb1-118">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="22cb1-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="22cb1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22cb1-119">-InputObject</span></span>
<span data-ttu-id="22cb1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="22cb1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="22cb1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22cb1-121">-PassThru</span></span>
<span data-ttu-id="22cb1-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="22cb1-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="22cb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="22cb1-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="22cb1-124">The name of the resource group.</span></span>
<span data-ttu-id="22cb1-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="22cb1-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="22cb1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22cb1-126">-SubscriptionId</span></span>
<span data-ttu-id="22cb1-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22cb1-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="22cb1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22cb1-128">-Confirm</span></span>
<span data-ttu-id="22cb1-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22cb1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22cb1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22cb1-130">-WhatIf</span></span>
<span data-ttu-id="22cb1-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22cb1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22cb1-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22cb1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22cb1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cb1-133">CommonParameters</span></span>
<span data-ttu-id="22cb1-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cb1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cb1-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22cb1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cb1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22cb1-136">INPUTS</span></span>

### <span data-ttu-id="22cb1-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="22cb1-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="22cb1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22cb1-138">OUTPUTS</span></span>

### <span data-ttu-id="22cb1-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22cb1-139">System.Boolean</span></span>

## <span data-ttu-id="22cb1-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22cb1-140">NOTES</span></span>

<span data-ttu-id="22cb1-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="22cb1-141">ALIASES</span></span>

<span data-ttu-id="22cb1-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="22cb1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="22cb1-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="22cb1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="22cb1-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="22cb1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="22cb1-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="22cb1-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="22cb1-146">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="22cb1-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="22cb1-147">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="22cb1-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="22cb1-148">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="22cb1-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="22cb1-149">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="22cb1-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="22cb1-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="22cb1-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="22cb1-151">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="22cb1-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="22cb1-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="22cb1-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="22cb1-153">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="22cb1-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="22cb1-154">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="22cb1-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="22cb1-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22cb1-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="22cb1-156">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="22cb1-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="22cb1-157">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="22cb1-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="22cb1-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22cb1-158">RELATED LINKS</span></span>

