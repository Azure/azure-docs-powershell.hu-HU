---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182273"
---
# <span data-ttu-id="daa56-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="daa56-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="daa56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="daa56-102">SYNOPSIS</span></span>
<span data-ttu-id="daa56-103">Beszerezhet egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="daa56-103">Get an application.</span></span>

## <span data-ttu-id="daa56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="daa56-104">SYNTAX</span></span>

### <span data-ttu-id="daa56-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="daa56-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="daa56-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="daa56-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="daa56-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="daa56-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="daa56-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="daa56-108">DESCRIPTION</span></span>
<span data-ttu-id="daa56-109">Beszerezhet egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="daa56-109">Get an application.</span></span>

## <span data-ttu-id="daa56-110">Példák</span><span class="sxs-lookup"><span data-stu-id="daa56-110">EXAMPLES</span></span>

### <span data-ttu-id="daa56-111">Példa 1: a Windows virtuális asztali alkalmazás beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="daa56-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="daa56-112">Ez a parancs a Windows virtuális asztali alkalmazást egy alkalmazás-csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="daa56-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="daa56-113">2. példa: a Windows virtuális asztali alkalmazásainak listája</span><span class="sxs-lookup"><span data-stu-id="daa56-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="daa56-114">Ez a parancs felsorolja a Windows virtuális asztali alkalmazásokat egy alkalmazás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="daa56-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="daa56-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="daa56-115">PARAMETERS</span></span>

### <span data-ttu-id="daa56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa56-116">-DefaultProfile</span></span>
<span data-ttu-id="daa56-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="daa56-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa56-118">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="daa56-118">-GroupName</span></span>
<span data-ttu-id="daa56-119">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="daa56-119">The name of the application group</span></span>

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

### <span data-ttu-id="daa56-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daa56-120">-InputObject</span></span>
<span data-ttu-id="daa56-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="daa56-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="daa56-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="daa56-122">-Name</span></span>
<span data-ttu-id="daa56-123">Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="daa56-123">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="daa56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa56-124">-ResourceGroupName</span></span>
<span data-ttu-id="daa56-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="daa56-125">The name of the resource group.</span></span>
<span data-ttu-id="daa56-126">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="daa56-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="daa56-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="daa56-127">-SubscriptionId</span></span>
<span data-ttu-id="daa56-128">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="daa56-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="daa56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa56-129">CommonParameters</span></span>
<span data-ttu-id="daa56-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="daa56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa56-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="daa56-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa56-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="daa56-132">INPUTS</span></span>

### <span data-ttu-id="daa56-133">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="daa56-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="daa56-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="daa56-134">OUTPUTS</span></span>

### <span data-ttu-id="daa56-135">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. sikertelen IApplication</span><span class="sxs-lookup"><span data-stu-id="daa56-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="daa56-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="daa56-136">NOTES</span></span>

<span data-ttu-id="daa56-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="daa56-137">ALIASES</span></span>

<span data-ttu-id="daa56-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="daa56-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="daa56-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="daa56-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="daa56-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="daa56-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="daa56-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="daa56-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="daa56-142">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="daa56-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="daa56-143">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="daa56-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="daa56-144">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="daa56-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="daa56-145">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="daa56-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="daa56-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="daa56-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="daa56-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="daa56-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="daa56-148">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="daa56-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="daa56-149">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="daa56-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="daa56-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="daa56-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="daa56-151">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="daa56-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="daa56-152">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="daa56-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="daa56-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="daa56-153">RELATED LINKS</span></span>

