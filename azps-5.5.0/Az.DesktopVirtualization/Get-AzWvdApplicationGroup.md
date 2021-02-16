---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 5f2ccffd0b0ba82b215db018ee15f4e495704f15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148050"
---
# <span data-ttu-id="c23d7-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c23d7-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c23d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c23d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c23d7-103">Alkalmazáscsoport lekérte</span><span class="sxs-lookup"><span data-stu-id="c23d7-103">Get an application group.</span></span>

## <span data-ttu-id="c23d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c23d7-104">SYNTAX</span></span>

### <span data-ttu-id="c23d7-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c23d7-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c23d7-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="c23d7-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c23d7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c23d7-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c23d7-108">Lista</span><span class="sxs-lookup"><span data-stu-id="c23d7-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c23d7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c23d7-109">DESCRIPTION</span></span>
<span data-ttu-id="c23d7-110">Alkalmazáscsoport lekérte</span><span class="sxs-lookup"><span data-stu-id="c23d7-110">Get an application group.</span></span>

## <span data-ttu-id="c23d7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c23d7-111">EXAMPLES</span></span>

### <span data-ttu-id="c23d7-112">1. példa: Windows Virtual Desktop ApplicationGroup név alapján</span><span class="sxs-lookup"><span data-stu-id="c23d7-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="c23d7-113">Ez a parancs egy Windows virtuális asztali alkalmazáscsoportot kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c23d7-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="c23d7-114">2. példa: A Windows virtuális asztali alkalmazáscsoportjainak listája</span><span class="sxs-lookup"><span data-stu-id="c23d7-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="c23d7-115">Ez a parancs felsorolja egy erőforráscsoport Windows virtuális asztali alkalmazáscsoportját.</span><span class="sxs-lookup"><span data-stu-id="c23d7-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="c23d7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c23d7-116">PARAMETERS</span></span>

### <span data-ttu-id="c23d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c23d7-117">-DefaultProfile</span></span>
<span data-ttu-id="c23d7-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c23d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c23d7-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="c23d7-119">-Filter</span></span>
<span data-ttu-id="c23d7-120">OData-szűrőkifejezés.</span><span class="sxs-lookup"><span data-stu-id="c23d7-120">OData filter expression.</span></span>
<span data-ttu-id="c23d7-121">A szűrés érvényes tulajdonságai az applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="c23d7-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23d7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c23d7-122">-InputObject</span></span>
<span data-ttu-id="c23d7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c23d7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c23d7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c23d7-124">-Name</span></span>
<span data-ttu-id="c23d7-125">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c23d7-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c23d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="c23d7-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c23d7-127">The name of the resource group.</span></span>
<span data-ttu-id="c23d7-128">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c23d7-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c23d7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c23d7-129">-SubscriptionId</span></span>
<span data-ttu-id="c23d7-130">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c23d7-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c23d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23d7-131">CommonParameters</span></span>
<span data-ttu-id="c23d7-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23d7-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c23d7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23d7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c23d7-134">INPUTS</span></span>

### <span data-ttu-id="c23d7-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c23d7-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c23d7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c23d7-136">OUTPUTS</span></span>

### <span data-ttu-id="c23d7-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c23d7-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="c23d7-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c23d7-138">NOTES</span></span>

<span data-ttu-id="c23d7-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c23d7-139">ALIASES</span></span>

<span data-ttu-id="c23d7-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c23d7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c23d7-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c23d7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c23d7-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c23d7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c23d7-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c23d7-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c23d7-144">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c23d7-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c23d7-145">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="c23d7-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c23d7-146">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="c23d7-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c23d7-147">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="c23d7-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c23d7-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c23d7-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c23d7-149">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="c23d7-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c23d7-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c23d7-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c23d7-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c23d7-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="c23d7-152">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="c23d7-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c23d7-153">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c23d7-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c23d7-154">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="c23d7-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c23d7-155">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="c23d7-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c23d7-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c23d7-156">RELATED LINKS</span></span>

