---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 3fa80fc69679346e3462a96340f4af9fc6a251d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387280"
---
# <span data-ttu-id="28d88-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="28d88-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="28d88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28d88-102">SYNOPSIS</span></span>
<span data-ttu-id="28d88-103">Munkaterületet is biztosítunk.</span><span class="sxs-lookup"><span data-stu-id="28d88-103">Get a workspace.</span></span>

## <span data-ttu-id="28d88-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28d88-104">SYNTAX</span></span>

### <span data-ttu-id="28d88-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28d88-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="28d88-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="28d88-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="28d88-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="28d88-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="28d88-108">Lista</span><span class="sxs-lookup"><span data-stu-id="28d88-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="28d88-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28d88-109">DESCRIPTION</span></span>
<span data-ttu-id="28d88-110">Munkaterületet is biztosítunk.</span><span class="sxs-lookup"><span data-stu-id="28d88-110">Get a workspace.</span></span>

## <span data-ttu-id="28d88-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28d88-111">EXAMPLES</span></span>

### <span data-ttu-id="28d88-112">1. példa: Virtuális asztali Windows-munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="28d88-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="28d88-113">Ez a parancs egy Windows virtuális asztali munkaterületet kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="28d88-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="28d88-114">2. példa: A Windows virtuális asztali munkaterületek listájának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="28d88-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="28d88-115">Ez a parancs felsorolja egy erőforráscsoport Windows virtuális asztal-munkaterületét.</span><span class="sxs-lookup"><span data-stu-id="28d88-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="28d88-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28d88-116">PARAMETERS</span></span>

### <span data-ttu-id="28d88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d88-117">-DefaultProfile</span></span>
<span data-ttu-id="28d88-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28d88-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28d88-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28d88-119">-InputObject</span></span>
<span data-ttu-id="28d88-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="28d88-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="28d88-121">-Name</span><span class="sxs-lookup"><span data-stu-id="28d88-121">-Name</span></span>
<span data-ttu-id="28d88-122">A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="28d88-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d88-123">-ResourceGroupName</span></span>
<span data-ttu-id="28d88-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="28d88-124">The name of the resource group.</span></span>
<span data-ttu-id="28d88-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="28d88-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="28d88-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28d88-126">-SubscriptionId</span></span>
<span data-ttu-id="28d88-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="28d88-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d88-128">CommonParameters</span></span>
<span data-ttu-id="28d88-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28d88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d88-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28d88-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d88-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28d88-131">INPUTS</span></span>

### <span data-ttu-id="28d88-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="28d88-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="28d88-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28d88-133">OUTPUTS</span></span>

### <span data-ttu-id="28d88-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="28d88-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="28d88-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28d88-135">NOTES</span></span>

<span data-ttu-id="28d88-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="28d88-136">ALIASES</span></span>

<span data-ttu-id="28d88-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="28d88-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28d88-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="28d88-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28d88-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28d88-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28d88-140">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="28d88-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="28d88-141">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="28d88-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="28d88-142">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="28d88-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="28d88-143">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="28d88-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="28d88-144">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="28d88-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="28d88-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="28d88-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28d88-146">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="28d88-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="28d88-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="28d88-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="28d88-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="28d88-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="28d88-149">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="28d88-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="28d88-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="28d88-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="28d88-151">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="28d88-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="28d88-152">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="28d88-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="28d88-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28d88-153">RELATED LINKS</span></span>

