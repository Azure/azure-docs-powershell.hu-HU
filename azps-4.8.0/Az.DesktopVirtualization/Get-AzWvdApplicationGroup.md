---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024031"
---
# <span data-ttu-id="d0d2a-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="d0d2a-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="d0d2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d2a-103">Alkalmazások csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d0d2a-103">Get an application group.</span></span>

## <span data-ttu-id="d0d2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0d2a-104">SYNTAX</span></span>

### <span data-ttu-id="d0d2a-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0d2a-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0d2a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d0d2a-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d0d2a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d0d2a-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0d2a-108">Lista</span><span class="sxs-lookup"><span data-stu-id="d0d2a-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d0d2a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0d2a-109">DESCRIPTION</span></span>
<span data-ttu-id="d0d2a-110">Alkalmazások csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d0d2a-110">Get an application group.</span></span>

## <span data-ttu-id="d0d2a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d0d2a-111">EXAMPLES</span></span>

### <span data-ttu-id="d0d2a-112">Példa 1: a Windows virtuális asztali ApplicationGroup beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="d0d2a-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="d0d2a-113">Ez a parancs egy erőforráscsoport Windows virtuális asztali ApplicationGroup kap.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="d0d2a-114">2. példa: a Windows virtuális asztali ApplicationGroups listája</span><span class="sxs-lookup"><span data-stu-id="d0d2a-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="d0d2a-115">Ez a parancs egy erőforráscsoport Windows virtuális asztali ApplicationGroups sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="d0d2a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0d2a-116">PARAMETERS</span></span>

### <span data-ttu-id="d0d2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d2a-117">-DefaultProfile</span></span>
<span data-ttu-id="d0d2a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0d2a-119">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="d0d2a-119">-Filter</span></span>
<span data-ttu-id="d0d2a-120">OData-szűrési kifejezés</span><span class="sxs-lookup"><span data-stu-id="d0d2a-120">OData filter expression.</span></span>
<span data-ttu-id="d0d2a-121">A szűréshez érvényes tulajdonságok a applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="d0d2a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0d2a-122">-InputObject</span></span>
<span data-ttu-id="d0d2a-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d0d2a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0d2a-124">-Name</span></span>
<span data-ttu-id="d0d2a-125">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="d0d2a-125">The name of the application group</span></span>

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

### <span data-ttu-id="d0d2a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0d2a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0d2a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-127">The name of the resource group.</span></span>
<span data-ttu-id="d0d2a-128">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d0d2a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0d2a-129">-SubscriptionId</span></span>
<span data-ttu-id="d0d2a-130">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d0d2a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d2a-131">CommonParameters</span></span>
<span data-ttu-id="d0d2a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0d2a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d2a-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d2a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0d2a-134">INPUTS</span></span>

### <span data-ttu-id="d0d2a-135">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d0d2a-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d0d2a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0d2a-136">OUTPUTS</span></span>

### <span data-ttu-id="d0d2a-137">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="d0d2a-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="d0d2a-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0d2a-138">NOTES</span></span>

<span data-ttu-id="d0d2a-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d0d2a-139">ALIASES</span></span>

<span data-ttu-id="d0d2a-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d0d2a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d0d2a-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0d2a-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d0d2a-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d0d2a-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0d2a-144">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="d0d2a-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d0d2a-145">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="d0d2a-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d0d2a-146">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="d0d2a-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d0d2a-147">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="d0d2a-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d0d2a-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d0d2a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0d2a-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d0d2a-150">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="d0d2a-151">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="d0d2a-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d0d2a-152">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d0d2a-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d0d2a-153">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="d0d2a-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d0d2a-154">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="d0d2a-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d0d2a-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0d2a-155">RELATED LINKS</span></span>

