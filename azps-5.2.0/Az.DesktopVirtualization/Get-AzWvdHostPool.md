---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 815f7280564d01077de99c4ec9b4003d4996d019
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330930"
---
# <span data-ttu-id="492f6-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="492f6-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="492f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="492f6-102">SYNOPSIS</span></span>
<span data-ttu-id="492f6-103">Állomáskészletet fog kapni.</span><span class="sxs-lookup"><span data-stu-id="492f6-103">Get a host pool.</span></span>

## <span data-ttu-id="492f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="492f6-104">SYNTAX</span></span>

### <span data-ttu-id="492f6-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="492f6-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="492f6-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="492f6-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="492f6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="492f6-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="492f6-108">Lista</span><span class="sxs-lookup"><span data-stu-id="492f6-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="492f6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="492f6-109">DESCRIPTION</span></span>
<span data-ttu-id="492f6-110">Állomáskészletet fog kapni.</span><span class="sxs-lookup"><span data-stu-id="492f6-110">Get a host pool.</span></span>

## <span data-ttu-id="492f6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="492f6-111">EXAMPLES</span></span>

### <span data-ttu-id="492f6-112">1. példa: Windows Virtual Desktop HostPool létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="492f6-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="492f6-113">Ez a parancs egy Windows Virtual Desktop HostPool-t kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="492f6-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="492f6-114">2. példa: A Windows virtuális asztali hostpools listájának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="492f6-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="492f6-115">Ez a parancs felsorolja az erőforráscsoportok windowsos virtuális asztali állomássorát.</span><span class="sxs-lookup"><span data-stu-id="492f6-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="492f6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="492f6-116">PARAMETERS</span></span>

### <span data-ttu-id="492f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492f6-117">-DefaultProfile</span></span>
<span data-ttu-id="492f6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="492f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="492f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="492f6-119">-InputObject</span></span>
<span data-ttu-id="492f6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="492f6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="492f6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="492f6-121">-Name</span></span>
<span data-ttu-id="492f6-122">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="492f6-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="492f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="492f6-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="492f6-124">The name of the resource group.</span></span>
<span data-ttu-id="492f6-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="492f6-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="492f6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="492f6-126">-SubscriptionId</span></span>
<span data-ttu-id="492f6-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="492f6-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="492f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492f6-128">CommonParameters</span></span>
<span data-ttu-id="492f6-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="492f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492f6-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="492f6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492f6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="492f6-131">INPUTS</span></span>

### <span data-ttu-id="492f6-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="492f6-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="492f6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="492f6-133">OUTPUTS</span></span>

### <span data-ttu-id="492f6-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.iHostPool</span><span class="sxs-lookup"><span data-stu-id="492f6-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="492f6-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="492f6-135">NOTES</span></span>

<span data-ttu-id="492f6-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="492f6-136">ALIASES</span></span>

<span data-ttu-id="492f6-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="492f6-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="492f6-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="492f6-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="492f6-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="492f6-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="492f6-140">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="492f6-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="492f6-141">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="492f6-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="492f6-142">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="492f6-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="492f6-143">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="492f6-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="492f6-144">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="492f6-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="492f6-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="492f6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="492f6-146">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="492f6-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="492f6-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="492f6-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="492f6-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="492f6-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="492f6-149">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="492f6-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="492f6-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="492f6-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="492f6-151">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="492f6-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="492f6-152">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="492f6-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="492f6-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="492f6-153">RELATED LINKS</span></span>

