---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296987"
---
# <span data-ttu-id="89607-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="89607-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="89607-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89607-102">SYNOPSIS</span></span>
<span data-ttu-id="89607-103">Távolítson el egy userSession.</span><span class="sxs-lookup"><span data-stu-id="89607-103">Remove a userSession.</span></span>

## <span data-ttu-id="89607-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89607-104">SYNTAX</span></span>

### <span data-ttu-id="89607-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89607-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="89607-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="89607-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89607-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="89607-107">DESCRIPTION</span></span>
<span data-ttu-id="89607-108">Távolítson el egy userSession.</span><span class="sxs-lookup"><span data-stu-id="89607-108">Remove a userSession.</span></span>

## <span data-ttu-id="89607-109">Példák</span><span class="sxs-lookup"><span data-stu-id="89607-109">EXAMPLES</span></span>

### <span data-ttu-id="89607-110">Példa 1: a Windows virtuális asztali UserSession törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="89607-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="89607-111">Ez a parancs törli a Windows virtuális asztali UserSession a munkamenet-állomáson.</span><span class="sxs-lookup"><span data-stu-id="89607-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="89607-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89607-112">PARAMETERS</span></span>

### <span data-ttu-id="89607-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89607-113">-DefaultProfile</span></span>
<span data-ttu-id="89607-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89607-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89607-115">-Force</span><span class="sxs-lookup"><span data-stu-id="89607-115">-Force</span></span>
<span data-ttu-id="89607-116">A userSession kikapcsolásához kényszerítse a jelölőt.</span><span class="sxs-lookup"><span data-stu-id="89607-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="89607-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="89607-117">-HostPoolName</span></span>
<span data-ttu-id="89607-118">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="89607-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="89607-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="89607-119">-Id</span></span>
<span data-ttu-id="89607-120">A felhasználó munkamenetének neve a megadott munkamenet-állomáson belül</span><span class="sxs-lookup"><span data-stu-id="89607-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89607-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89607-121">-InputObject</span></span>
<span data-ttu-id="89607-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89607-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="89607-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89607-123">-PassThru</span></span>
<span data-ttu-id="89607-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="89607-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="89607-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89607-125">-ResourceGroupName</span></span>
<span data-ttu-id="89607-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89607-126">The name of the resource group.</span></span>
<span data-ttu-id="89607-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="89607-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="89607-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="89607-128">-SessionHostName</span></span>
<span data-ttu-id="89607-129">A megadott alkalmazáskészleten belüli munkamenet-állomás neve</span><span class="sxs-lookup"><span data-stu-id="89607-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="89607-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89607-130">-SubscriptionId</span></span>
<span data-ttu-id="89607-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89607-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="89607-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89607-132">-Confirm</span></span>
<span data-ttu-id="89607-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89607-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89607-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89607-134">-WhatIf</span></span>
<span data-ttu-id="89607-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89607-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89607-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89607-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89607-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89607-137">CommonParameters</span></span>
<span data-ttu-id="89607-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89607-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89607-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89607-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89607-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89607-140">INPUTS</span></span>

### <span data-ttu-id="89607-141">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="89607-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="89607-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89607-142">OUTPUTS</span></span>

### <span data-ttu-id="89607-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89607-143">System.Boolean</span></span>

## <span data-ttu-id="89607-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89607-144">NOTES</span></span>

<span data-ttu-id="89607-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="89607-145">ALIASES</span></span>

<span data-ttu-id="89607-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="89607-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89607-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="89607-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89607-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="89607-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89607-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="89607-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89607-150">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="89607-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="89607-151">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="89607-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="89607-152">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="89607-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="89607-153">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="89607-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="89607-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="89607-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89607-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89607-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="89607-156">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="89607-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="89607-157">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="89607-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="89607-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89607-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="89607-159">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="89607-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="89607-160">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="89607-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="89607-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89607-161">RELATED LINKS</span></span>

