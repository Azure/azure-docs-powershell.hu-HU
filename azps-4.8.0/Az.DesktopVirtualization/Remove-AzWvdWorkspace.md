---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 420a73dc1890db1b26cff5ca5289dc030666b038
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182258"
---
# <span data-ttu-id="2eaf8-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="2eaf8-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="2eaf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2eaf8-102">SYNOPSIS</span></span>
<span data-ttu-id="2eaf8-103">Munkaterület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2eaf8-103">Remove a workspace.</span></span>

## <span data-ttu-id="2eaf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2eaf8-104">SYNTAX</span></span>

### <span data-ttu-id="2eaf8-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2eaf8-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2eaf8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2eaf8-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2eaf8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2eaf8-107">DESCRIPTION</span></span>
<span data-ttu-id="2eaf8-108">Munkaterület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2eaf8-108">Remove a workspace.</span></span>

## <span data-ttu-id="2eaf8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2eaf8-109">EXAMPLES</span></span>

### <span data-ttu-id="2eaf8-110">Példa 1: a Windows virtuális asztali Worksapce törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="2eaf8-110">Example 1: Delete a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="2eaf8-111">Ez a parancs törli a Windows virtuális asztal munkaterületét egy erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="2eaf8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2eaf8-112">PARAMETERS</span></span>

### <span data-ttu-id="2eaf8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eaf8-113">-DefaultProfile</span></span>
<span data-ttu-id="2eaf8-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eaf8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eaf8-115">-InputObject</span></span>
<span data-ttu-id="2eaf8-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eaf8-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2eaf8-117">-Name</span></span>
<span data-ttu-id="2eaf8-118">A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="2eaf8-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eaf8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eaf8-119">-PassThru</span></span>
<span data-ttu-id="2eaf8-120">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="2eaf8-120">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eaf8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eaf8-121">-ResourceGroupName</span></span>
<span data-ttu-id="2eaf8-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-122">The name of the resource group.</span></span>
<span data-ttu-id="2eaf8-123">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eaf8-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2eaf8-124">-SubscriptionId</span></span>
<span data-ttu-id="2eaf8-125">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eaf8-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2eaf8-126">-Confirm</span></span>
<span data-ttu-id="2eaf8-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eaf8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eaf8-128">-WhatIf</span></span>
<span data-ttu-id="2eaf8-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eaf8-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eaf8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eaf8-131">CommonParameters</span></span>
<span data-ttu-id="2eaf8-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2eaf8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eaf8-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eaf8-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eaf8-134">INPUTS</span></span>

### <span data-ttu-id="2eaf8-135">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2eaf8-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2eaf8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eaf8-136">OUTPUTS</span></span>

### <span data-ttu-id="2eaf8-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2eaf8-137">System.Boolean</span></span>

## <span data-ttu-id="2eaf8-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2eaf8-138">NOTES</span></span>

<span data-ttu-id="2eaf8-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2eaf8-139">ALIASES</span></span>

<span data-ttu-id="2eaf8-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="2eaf8-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2eaf8-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2eaf8-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2eaf8-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="2eaf8-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2eaf8-144">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="2eaf8-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2eaf8-145">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="2eaf8-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2eaf8-146">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="2eaf8-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2eaf8-147">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="2eaf8-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2eaf8-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2eaf8-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2eaf8-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2eaf8-150">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="2eaf8-151">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="2eaf8-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2eaf8-152">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2eaf8-153">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="2eaf8-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2eaf8-154">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="2eaf8-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2eaf8-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2eaf8-155">RELATED LINKS</span></span>

