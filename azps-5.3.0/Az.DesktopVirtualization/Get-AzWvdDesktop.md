---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: de52995d5cda17e332c137966f58b349d64c01f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467914"
---
# <span data-ttu-id="0af3d-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="0af3d-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="0af3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0af3d-102">SYNOPSIS</span></span>
<span data-ttu-id="0af3d-103">Szerezze be az asztalt.</span><span class="sxs-lookup"><span data-stu-id="0af3d-103">Get a desktop.</span></span>

## <span data-ttu-id="0af3d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0af3d-104">SYNTAX</span></span>

### <span data-ttu-id="0af3d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0af3d-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0af3d-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="0af3d-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0af3d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0af3d-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0af3d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0af3d-108">DESCRIPTION</span></span>
<span data-ttu-id="0af3d-109">Szerezze be az asztalt.</span><span class="sxs-lookup"><span data-stu-id="0af3d-109">Get a desktop.</span></span>

## <span data-ttu-id="0af3d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0af3d-110">EXAMPLES</span></span>

### <span data-ttu-id="0af3d-111">1. példa: Windows Virtuális asztal létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="0af3d-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="0af3d-112">Ez a parancs egy Windows virtuális asztalt kap egy applicaton csoportban.</span><span class="sxs-lookup"><span data-stu-id="0af3d-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="0af3d-113">2. példa: Windows virtuális asztalok felsorolása</span><span class="sxs-lookup"><span data-stu-id="0af3d-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="0af3d-114">Ez a parancs felsorolja aWindows Virtual Desktops alkalmazást egy applicaton-csoportban.</span><span class="sxs-lookup"><span data-stu-id="0af3d-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="0af3d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0af3d-115">PARAMETERS</span></span>

### <span data-ttu-id="0af3d-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="0af3d-116">-ApplicationGroupName</span></span>
<span data-ttu-id="0af3d-117">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0af3d-117">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af3d-118">-DefaultProfile</span></span>
<span data-ttu-id="0af3d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0af3d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af3d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0af3d-120">-InputObject</span></span>
<span data-ttu-id="0af3d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0af3d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0af3d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0af3d-122">-Name</span></span>
<span data-ttu-id="0af3d-123">Az asztal neve a megadott asztali csoportban</span><span class="sxs-lookup"><span data-stu-id="0af3d-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0af3d-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0af3d-125">The name of the resource group.</span></span>
<span data-ttu-id="0af3d-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0af3d-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af3d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0af3d-127">-SubscriptionId</span></span>
<span data-ttu-id="0af3d-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0af3d-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af3d-129">CommonParameters</span></span>
<span data-ttu-id="0af3d-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af3d-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0af3d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af3d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0af3d-132">INPUTS</span></span>

### <span data-ttu-id="0af3d-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0af3d-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0af3d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0af3d-134">OUTPUTS</span></span>

### <span data-ttu-id="0af3d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="0af3d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="0af3d-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="0af3d-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="0af3d-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0af3d-137">NOTES</span></span>

<span data-ttu-id="0af3d-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0af3d-138">ALIASES</span></span>

<span data-ttu-id="0af3d-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0af3d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0af3d-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0af3d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0af3d-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0af3d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0af3d-142">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0af3d-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0af3d-143">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0af3d-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0af3d-144">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="0af3d-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0af3d-145">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="0af3d-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0af3d-146">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="0af3d-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0af3d-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0af3d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0af3d-148">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="0af3d-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="0af3d-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0af3d-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0af3d-150">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0af3d-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="0af3d-151">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="0af3d-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0af3d-152">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0af3d-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0af3d-153">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="0af3d-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0af3d-154">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="0af3d-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0af3d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0af3d-155">RELATED LINKS</span></span>

