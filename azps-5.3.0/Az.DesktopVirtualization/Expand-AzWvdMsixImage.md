---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387308"
---
# <span data-ttu-id="8c4c4-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="8c4c4-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="8c4c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4c4-103">Kibontja és listázza az MSIX-csomagokat egy képben, a kép elérési útját figyelembeve.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="8c4c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c4c4-104">SYNTAX</span></span>

### <span data-ttu-id="8c4c4-105">ExpandExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c4c4-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c4c4-106">Kibontás</span><span class="sxs-lookup"><span data-stu-id="8c4c4-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c4c4-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8c4c4-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c4c4-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8c4c4-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c4c4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c4c4-109">DESCRIPTION</span></span>
<span data-ttu-id="8c4c4-110">Kibontja és listázza az MSIX-csomagokat egy képben, a kép elérési útját figyelembeve.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="8c4c4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c4c4-111">EXAMPLES</span></span>

### <span data-ttu-id="8c4c4-112">1. példa: Kibővíti a megadott kép elérési útját, és beolvassa a csomag metaadatait a AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="8c4c4-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="8c4c4-113">Ez a parancs a megadott kép elérési útban található MSIX-csomag metaadatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="8c4c4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c4c4-114">PARAMETERS</span></span>

### <span data-ttu-id="8c4c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4c4-115">-DefaultProfile</span></span>
<span data-ttu-id="8c4c4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c4c4-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8c4c4-117">-HostPoolName</span></span>
<span data-ttu-id="8c4c4-118">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="8c4c4-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c4c4-119">-InputObject</span></span>
<span data-ttu-id="8c4c4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c4-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="8c4c4-121">-MsixImageUri</span></span>
<span data-ttu-id="8c4c4-122">Az MSIX Image To construct (Létrehozva) URI azonosítót jelöli, lásd az MSIXIMAGEURI tulajdonságok MEGJEGYZÉSEK szakaszát, és hozzon létre egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c4c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c4c4-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-124">The name of the resource group.</span></span>
<span data-ttu-id="8c4c4-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="8c4c4-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c4c4-126">-SubscriptionId</span></span>
<span data-ttu-id="8c4c4-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c4-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="8c4c4-128">-Uri</span></span>
<span data-ttu-id="8c4c4-129">URI –Kép</span><span class="sxs-lookup"><span data-stu-id="8c4c4-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c4c4-130">-Confirm</span></span>
<span data-ttu-id="8c4c4-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4c4-132">-WhatIf</span></span>
<span data-ttu-id="8c4c4-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4c4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4c4-135">CommonParameters</span></span>
<span data-ttu-id="8c4c4-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4c4-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c4c4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4c4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c4c4-138">INPUTS</span></span>

### <span data-ttu-id="8c4c4-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="8c4c4-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="8c4c4-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8c4c4-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8c4c4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c4c4-141">OUTPUTS</span></span>

### <span data-ttu-id="8c4c4-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="8c4c4-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="8c4c4-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c4c4-143">NOTES</span></span>

<span data-ttu-id="8c4c4-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8c4c4-144">ALIASES</span></span>

<span data-ttu-id="8c4c4-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8c4c4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c4c4-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c4c4-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c4c4-148">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="8c4c4-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c4c4-149">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8c4c4-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8c4c4-150">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="8c4c4-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8c4c4-151">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="8c4c4-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8c4c4-152">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="8c4c4-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8c4c4-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8c4c4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c4c4-154">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="8c4c4-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8c4c4-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8c4c4-156">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="8c4c4-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="8c4c4-157">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="8c4c4-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8c4c4-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8c4c4-159">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="8c4c4-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8c4c4-160">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="8c4c4-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="8c4c4-161">MSIXIMAGEURI: <IMsixImageUri> Az MSIX-képre hivatkozó URI</span><span class="sxs-lookup"><span data-stu-id="8c4c4-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="8c4c4-162">`[Uri <String>]`: URI –Kép</span><span class="sxs-lookup"><span data-stu-id="8c4c4-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="8c4c4-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c4c4-163">RELATED LINKS</span></span>

