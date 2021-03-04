---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: f552c8e21703d64efa2ac65f47461daa963fc1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934402"
---
# <span data-ttu-id="6a18a-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="6a18a-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="6a18a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a18a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a18a-103">Frissítsen egy MSIX-csomagot.</span><span class="sxs-lookup"><span data-stu-id="6a18a-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="6a18a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a18a-104">SYNTAX</span></span>

### <span data-ttu-id="6a18a-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a18a-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a18a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a18a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a18a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a18a-107">DESCRIPTION</span></span>
<span data-ttu-id="6a18a-108">Frissítsen egy MSIX-csomagot.</span><span class="sxs-lookup"><span data-stu-id="6a18a-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="6a18a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a18a-109">EXAMPLES</span></span>

### <span data-ttu-id="6a18a-110">1. példa: MSIX-csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="6a18a-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="6a18a-111">Ez a parancs frissíti az MSIX-csomagot a HostPoolban.</span><span class="sxs-lookup"><span data-stu-id="6a18a-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="6a18a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a18a-112">PARAMETERS</span></span>

### <span data-ttu-id="6a18a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a18a-113">-DefaultProfile</span></span>
<span data-ttu-id="6a18a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a18a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a18a-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6a18a-115">-DisplayName</span></span>
<span data-ttu-id="6a18a-116">Az MSIX-csomag megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="6a18a-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="6a18a-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="6a18a-117">-FullName</span></span>
<span data-ttu-id="6a18a-118">Az MSIX-csomag teljes neve a megadott állomáskészleten belül</span><span class="sxs-lookup"><span data-stu-id="6a18a-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a18a-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="6a18a-119">-HostPoolName</span></span>
<span data-ttu-id="6a18a-120">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="6a18a-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="6a18a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a18a-121">-InputObject</span></span>
<span data-ttu-id="6a18a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6a18a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a18a-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="6a18a-123">-IsActive</span></span>
<span data-ttu-id="6a18a-124">Állítsa be, hogy a csomag egy verziója aktív legyen a hostpoolban.</span><span class="sxs-lookup"><span data-stu-id="6a18a-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="6a18a-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="6a18a-125">-IsRegularRegistration</span></span>
<span data-ttu-id="6a18a-126">Regisztrációs mód beállítása</span><span class="sxs-lookup"><span data-stu-id="6a18a-126">Set Registration mode.</span></span>
<span data-ttu-id="6a18a-127">Normál vagy késleltetett.</span><span class="sxs-lookup"><span data-stu-id="6a18a-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="6a18a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a18a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a18a-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6a18a-129">The name of the resource group.</span></span>
<span data-ttu-id="6a18a-130">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6a18a-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6a18a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a18a-131">-SubscriptionId</span></span>
<span data-ttu-id="6a18a-132">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a18a-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6a18a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a18a-133">-Confirm</span></span>
<span data-ttu-id="6a18a-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6a18a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a18a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a18a-135">-WhatIf</span></span>
<span data-ttu-id="6a18a-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6a18a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a18a-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a18a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a18a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a18a-138">CommonParameters</span></span>
<span data-ttu-id="6a18a-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a18a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a18a-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a18a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a18a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a18a-141">INPUTS</span></span>

### <span data-ttu-id="6a18a-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6a18a-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6a18a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a18a-143">OUTPUTS</span></span>

### <span data-ttu-id="6a18a-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="6a18a-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="6a18a-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a18a-145">NOTES</span></span>

<span data-ttu-id="6a18a-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6a18a-146">ALIASES</span></span>

<span data-ttu-id="6a18a-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6a18a-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a18a-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6a18a-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a18a-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a18a-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a18a-150">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6a18a-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a18a-151">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6a18a-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6a18a-152">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="6a18a-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6a18a-153">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="6a18a-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6a18a-154">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="6a18a-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6a18a-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6a18a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a18a-156">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="6a18a-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="6a18a-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6a18a-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6a18a-158">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6a18a-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="6a18a-159">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="6a18a-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6a18a-160">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a18a-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6a18a-161">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="6a18a-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6a18a-162">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="6a18a-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6a18a-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a18a-163">RELATED LINKS</span></span>

