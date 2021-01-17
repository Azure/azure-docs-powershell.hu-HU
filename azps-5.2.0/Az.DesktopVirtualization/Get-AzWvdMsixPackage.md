---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 559cff58ac8d6c3f3d8f116b6147d6f4c2a4378d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330942"
---
# <span data-ttu-id="ef112-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="ef112-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="ef112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef112-102">SYNOPSIS</span></span>
<span data-ttu-id="ef112-103">Szerezze be az msixpackage-t.</span><span class="sxs-lookup"><span data-stu-id="ef112-103">Get a msixpackage.</span></span>

## <span data-ttu-id="ef112-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef112-104">SYNTAX</span></span>

### <span data-ttu-id="ef112-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef112-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef112-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="ef112-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef112-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ef112-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef112-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef112-108">DESCRIPTION</span></span>
<span data-ttu-id="ef112-109">Szerezze be az msixpackage-t.</span><span class="sxs-lookup"><span data-stu-id="ef112-109">Get a msixpackage.</span></span>

## <span data-ttu-id="ef112-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef112-110">EXAMPLES</span></span>

### <span data-ttu-id="ef112-111">1. példa: MSIX-csomag lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="ef112-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="ef112-112">Ez a parancs MSIX-csomagot kap a HostPoolban.</span><span class="sxs-lookup"><span data-stu-id="ef112-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="ef112-113">2. példa: MSIX-csomagok felsorolása</span><span class="sxs-lookup"><span data-stu-id="ef112-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="ef112-114">Ez a parancs a HostPool MSIX-csomagjait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="ef112-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="ef112-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef112-115">PARAMETERS</span></span>

### <span data-ttu-id="ef112-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef112-116">-DefaultProfile</span></span>
<span data-ttu-id="ef112-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef112-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef112-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="ef112-118">-FullName</span></span>
<span data-ttu-id="ef112-119">Az MSIX-csomag teljes neve a megadott állomáskészleten belül</span><span class="sxs-lookup"><span data-stu-id="ef112-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef112-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ef112-120">-HostPoolName</span></span>
<span data-ttu-id="ef112-121">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="ef112-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ef112-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef112-122">-InputObject</span></span>
<span data-ttu-id="ef112-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ef112-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ef112-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef112-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef112-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef112-125">The name of the resource group.</span></span>
<span data-ttu-id="ef112-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ef112-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ef112-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef112-127">-SubscriptionId</span></span>
<span data-ttu-id="ef112-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef112-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ef112-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef112-129">CommonParameters</span></span>
<span data-ttu-id="ef112-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef112-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef112-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef112-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef112-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef112-132">INPUTS</span></span>

### <span data-ttu-id="ef112-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ef112-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ef112-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef112-134">OUTPUTS</span></span>

### <span data-ttu-id="ef112-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="ef112-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="ef112-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef112-136">NOTES</span></span>

<span data-ttu-id="ef112-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ef112-137">ALIASES</span></span>

<span data-ttu-id="ef112-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ef112-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef112-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ef112-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef112-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef112-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef112-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ef112-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef112-142">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ef112-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ef112-143">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="ef112-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ef112-144">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="ef112-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ef112-145">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="ef112-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ef112-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ef112-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef112-147">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="ef112-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ef112-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef112-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ef112-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ef112-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="ef112-150">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="ef112-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ef112-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef112-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ef112-152">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="ef112-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ef112-153">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="ef112-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ef112-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef112-154">RELATED LINKS</span></span>

