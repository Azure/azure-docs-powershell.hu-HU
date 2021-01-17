---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: 9e2f111c97299cbdb9f8058d2c4e737529025b62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348149"
---
# <span data-ttu-id="766e4-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="766e4-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="766e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766e4-102">SYNOPSIS</span></span>
<span data-ttu-id="766e4-103">Alkalmazás lekérte.</span><span class="sxs-lookup"><span data-stu-id="766e4-103">Get an application.</span></span>

## <span data-ttu-id="766e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="766e4-104">SYNTAX</span></span>

### <span data-ttu-id="766e4-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="766e4-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="766e4-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="766e4-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="766e4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="766e4-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="766e4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="766e4-108">DESCRIPTION</span></span>
<span data-ttu-id="766e4-109">Alkalmazás lekérte.</span><span class="sxs-lookup"><span data-stu-id="766e4-109">Get an application.</span></span>

## <span data-ttu-id="766e4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="766e4-110">EXAMPLES</span></span>

### <span data-ttu-id="766e4-111">1. példa: Windows virtuális asztali alkalmazás lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="766e4-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="766e4-112">Ez a parancs egy windowsos virtuális asztali alkalmazást kap egy aplicaton groupban.</span><span class="sxs-lookup"><span data-stu-id="766e4-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="766e4-113">2. példa: Windows virtuális asztali alkalmazások felsorolása</span><span class="sxs-lookup"><span data-stu-id="766e4-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="766e4-114">Ez a parancs felsorolja a Windows virtuális asztali alkalmazásokat egy applicaton-csoportban.</span><span class="sxs-lookup"><span data-stu-id="766e4-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="766e4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="766e4-115">PARAMETERS</span></span>

### <span data-ttu-id="766e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766e4-116">-DefaultProfile</span></span>
<span data-ttu-id="766e4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="766e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="766e4-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="766e4-118">-GroupName</span></span>
<span data-ttu-id="766e4-119">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="766e4-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="766e4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="766e4-120">-InputObject</span></span>
<span data-ttu-id="766e4-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="766e4-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="766e4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="766e4-122">-Name</span></span>
<span data-ttu-id="766e4-123">Az alkalmazás neve a megadott alkalmazáscsoportban</span><span class="sxs-lookup"><span data-stu-id="766e4-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="766e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="766e4-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="766e4-125">The name of the resource group.</span></span>
<span data-ttu-id="766e4-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="766e4-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="766e4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="766e4-127">-SubscriptionId</span></span>
<span data-ttu-id="766e4-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="766e4-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="766e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766e4-129">CommonParameters</span></span>
<span data-ttu-id="766e4-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="766e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766e4-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="766e4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766e4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="766e4-132">INPUTS</span></span>

### <span data-ttu-id="766e4-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="766e4-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="766e4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="766e4-134">OUTPUTS</span></span>

### <span data-ttu-id="766e4-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="766e4-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span></span>

## <span data-ttu-id="766e4-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="766e4-136">NOTES</span></span>

<span data-ttu-id="766e4-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="766e4-137">ALIASES</span></span>

<span data-ttu-id="766e4-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="766e4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="766e4-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="766e4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="766e4-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="766e4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="766e4-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="766e4-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="766e4-142">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="766e4-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="766e4-143">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="766e4-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="766e4-144">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="766e4-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="766e4-145">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="766e4-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="766e4-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="766e4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="766e4-147">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="766e4-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="766e4-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="766e4-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="766e4-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="766e4-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="766e4-150">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="766e4-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="766e4-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="766e4-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="766e4-152">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="766e4-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="766e4-153">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="766e4-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="766e4-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="766e4-154">RELATED LINKS</span></span>

