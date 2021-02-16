---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153258"
---
# <span data-ttu-id="47a81-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="47a81-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="47a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47a81-102">SYNOPSIS</span></span>
<span data-ttu-id="47a81-103">Frissítsen egy MSIX-csomagot.</span><span class="sxs-lookup"><span data-stu-id="47a81-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="47a81-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47a81-104">SYNTAX</span></span>

### <span data-ttu-id="47a81-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47a81-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47a81-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="47a81-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47a81-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47a81-107">DESCRIPTION</span></span>
<span data-ttu-id="47a81-108">Frissítsen egy MSIX-csomagot.</span><span class="sxs-lookup"><span data-stu-id="47a81-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="47a81-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47a81-109">EXAMPLES</span></span>

### <span data-ttu-id="47a81-110">1. példa: MSIX-csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="47a81-110">Example 1: Update a MSIX Package</span></span> 
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

<span data-ttu-id="47a81-111">Ez a parancs frissíti az MSIX-csomagot a HostPoolban.</span><span class="sxs-lookup"><span data-stu-id="47a81-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="47a81-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47a81-112">PARAMETERS</span></span>

### <span data-ttu-id="47a81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a81-113">-DefaultProfile</span></span>
<span data-ttu-id="47a81-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47a81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a81-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="47a81-115">-DisplayName</span></span>
<span data-ttu-id="47a81-116">Az MSIX-csomag megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="47a81-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="47a81-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="47a81-117">-FullName</span></span>
<span data-ttu-id="47a81-118">A verzióspecifikus csomag teljes neve az MSIX-csomagnak a megadott állomássoron belül</span><span class="sxs-lookup"><span data-stu-id="47a81-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="47a81-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="47a81-119">-HostPoolName</span></span>
<span data-ttu-id="47a81-120">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="47a81-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="47a81-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47a81-121">-InputObject</span></span>
<span data-ttu-id="47a81-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="47a81-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47a81-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="47a81-123">-IsActive</span></span>
<span data-ttu-id="47a81-124">Állítsa be, hogy a csomag egy verziója aktív legyen a hostpoolban.</span><span class="sxs-lookup"><span data-stu-id="47a81-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="47a81-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="47a81-125">-IsRegularRegistration</span></span>
<span data-ttu-id="47a81-126">Regisztrációs mód beállítása</span><span class="sxs-lookup"><span data-stu-id="47a81-126">Set Registration mode.</span></span>
<span data-ttu-id="47a81-127">Normál vagy késleltetett.</span><span class="sxs-lookup"><span data-stu-id="47a81-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="47a81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47a81-128">-ResourceGroupName</span></span>
<span data-ttu-id="47a81-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="47a81-129">The name of the resource group.</span></span>
<span data-ttu-id="47a81-130">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="47a81-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="47a81-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47a81-131">-SubscriptionId</span></span>
<span data-ttu-id="47a81-132">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="47a81-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="47a81-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47a81-133">-Confirm</span></span>
<span data-ttu-id="47a81-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="47a81-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a81-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a81-135">-WhatIf</span></span>
<span data-ttu-id="47a81-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="47a81-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a81-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47a81-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a81-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a81-138">CommonParameters</span></span>
<span data-ttu-id="47a81-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a81-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a81-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47a81-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a81-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47a81-141">INPUTS</span></span>

### <span data-ttu-id="47a81-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="47a81-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="47a81-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47a81-143">OUTPUTS</span></span>

### <span data-ttu-id="47a81-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="47a81-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="47a81-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47a81-145">NOTES</span></span>

<span data-ttu-id="47a81-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="47a81-146">ALIASES</span></span>

<span data-ttu-id="47a81-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="47a81-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47a81-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="47a81-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47a81-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47a81-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47a81-150">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="47a81-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47a81-151">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="47a81-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="47a81-152">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="47a81-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="47a81-153">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="47a81-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="47a81-154">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="47a81-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="47a81-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="47a81-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47a81-156">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="47a81-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="47a81-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="47a81-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="47a81-158">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="47a81-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="47a81-159">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="47a81-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="47a81-160">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="47a81-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="47a81-161">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="47a81-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="47a81-162">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="47a81-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="47a81-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47a81-163">RELATED LINKS</span></span>

