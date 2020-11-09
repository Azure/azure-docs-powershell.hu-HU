---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 6c885f4962734bf1034256843258f4755a9b3b44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296999"
---
# <span data-ttu-id="59b61-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="59b61-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="59b61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59b61-102">SYNOPSIS</span></span>
<span data-ttu-id="59b61-103">Távolítson el egy applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="59b61-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="59b61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59b61-104">SYNTAX</span></span>

### <span data-ttu-id="59b61-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59b61-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="59b61-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="59b61-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59b61-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="59b61-107">DESCRIPTION</span></span>
<span data-ttu-id="59b61-108">Távolítson el egy applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="59b61-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="59b61-109">Példák</span><span class="sxs-lookup"><span data-stu-id="59b61-109">EXAMPLES</span></span>

### <span data-ttu-id="59b61-110">Példa 1: a Windows virtuális asztali ApplicationGroup törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="59b61-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="59b61-111">Ez a parancs törli a Windows virtuális asztali ApplicationGroup egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="59b61-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="59b61-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59b61-112">PARAMETERS</span></span>

### <span data-ttu-id="59b61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b61-113">-DefaultProfile</span></span>
<span data-ttu-id="59b61-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59b61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59b61-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59b61-115">-InputObject</span></span>
<span data-ttu-id="59b61-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="59b61-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="59b61-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59b61-117">-Name</span></span>
<span data-ttu-id="59b61-118">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="59b61-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b61-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59b61-119">-PassThru</span></span>
<span data-ttu-id="59b61-120">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="59b61-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="59b61-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b61-121">-ResourceGroupName</span></span>
<span data-ttu-id="59b61-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="59b61-122">The name of the resource group.</span></span>
<span data-ttu-id="59b61-123">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="59b61-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="59b61-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59b61-124">-SubscriptionId</span></span>
<span data-ttu-id="59b61-125">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="59b61-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="59b61-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59b61-126">-Confirm</span></span>
<span data-ttu-id="59b61-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59b61-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b61-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b61-128">-WhatIf</span></span>
<span data-ttu-id="59b61-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59b61-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59b61-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59b61-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b61-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b61-131">CommonParameters</span></span>
<span data-ttu-id="59b61-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59b61-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b61-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="59b61-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b61-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59b61-134">INPUTS</span></span>

### <span data-ttu-id="59b61-135">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="59b61-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="59b61-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59b61-136">OUTPUTS</span></span>

### <span data-ttu-id="59b61-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59b61-137">System.Boolean</span></span>

## <span data-ttu-id="59b61-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59b61-138">NOTES</span></span>

<span data-ttu-id="59b61-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="59b61-139">ALIASES</span></span>

<span data-ttu-id="59b61-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="59b61-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="59b61-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="59b61-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59b61-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="59b61-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="59b61-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="59b61-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="59b61-144">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="59b61-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="59b61-145">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="59b61-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="59b61-146">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="59b61-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="59b61-147">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="59b61-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="59b61-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="59b61-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="59b61-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="59b61-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="59b61-150">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="59b61-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="59b61-151">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="59b61-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="59b61-152">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="59b61-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="59b61-153">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="59b61-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="59b61-154">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="59b61-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="59b61-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59b61-155">RELATED LINKS</span></span>

