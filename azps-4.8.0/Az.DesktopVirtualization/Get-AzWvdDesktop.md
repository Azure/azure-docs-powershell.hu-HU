---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025381"
---
# <span data-ttu-id="b6622-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="b6622-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="b6622-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6622-102">SYNOPSIS</span></span>
<span data-ttu-id="b6622-103">Szerezzen be egy asztalt.</span><span class="sxs-lookup"><span data-stu-id="b6622-103">Get a desktop.</span></span>

## <span data-ttu-id="b6622-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6622-104">SYNTAX</span></span>

### <span data-ttu-id="b6622-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6622-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6622-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b6622-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6622-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6622-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6622-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6622-108">DESCRIPTION</span></span>
<span data-ttu-id="b6622-109">Szerezzen be egy asztalt.</span><span class="sxs-lookup"><span data-stu-id="b6622-109">Get a desktop.</span></span>

## <span data-ttu-id="b6622-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b6622-110">EXAMPLES</span></span>

### <span data-ttu-id="b6622-111">Példa 1: a Windows virtuális asztali asztal beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="b6622-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="b6622-112">Ez a parancs egy asztali Windows rendszerű asztali alkalmazás-csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="b6622-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="b6622-113">2. példa: a Windows virtuális asztali asztali verzióinak listája</span><span class="sxs-lookup"><span data-stu-id="b6622-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="b6622-114">Ez a parancs egy alkalmazás-csoportban listsWindows a virtuális asztali asztalokat.</span><span class="sxs-lookup"><span data-stu-id="b6622-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="b6622-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6622-115">PARAMETERS</span></span>

### <span data-ttu-id="b6622-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="b6622-116">-ApplicationGroupName</span></span>
<span data-ttu-id="b6622-117">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="b6622-117">The name of the application group</span></span>

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

### <span data-ttu-id="b6622-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6622-118">-DefaultProfile</span></span>
<span data-ttu-id="b6622-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6622-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6622-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6622-120">-InputObject</span></span>
<span data-ttu-id="b6622-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6622-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6622-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6622-122">-Name</span></span>
<span data-ttu-id="b6622-123">A megadott asztali csoporton belüli asztal neve</span><span class="sxs-lookup"><span data-stu-id="b6622-123">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="b6622-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6622-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6622-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6622-125">The name of the resource group.</span></span>
<span data-ttu-id="b6622-126">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="b6622-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b6622-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6622-127">-SubscriptionId</span></span>
<span data-ttu-id="b6622-128">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b6622-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b6622-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6622-129">CommonParameters</span></span>
<span data-ttu-id="b6622-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6622-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6622-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6622-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6622-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6622-132">INPUTS</span></span>

### <span data-ttu-id="b6622-133">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b6622-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b6622-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6622-134">OUTPUTS</span></span>

### <span data-ttu-id="b6622-135">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="b6622-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="b6622-136">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="b6622-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="b6622-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6622-137">NOTES</span></span>

<span data-ttu-id="b6622-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b6622-138">ALIASES</span></span>

<span data-ttu-id="b6622-139">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="b6622-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6622-140">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b6622-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6622-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b6622-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6622-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b6622-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6622-143">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="b6622-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b6622-144">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="b6622-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b6622-145">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="b6622-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b6622-146">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="b6622-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b6622-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b6622-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6622-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6622-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b6622-149">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="b6622-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b6622-150">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="b6622-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b6622-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b6622-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b6622-152">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="b6622-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b6622-153">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="b6622-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b6622-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6622-154">RELATED LINKS</span></span>

