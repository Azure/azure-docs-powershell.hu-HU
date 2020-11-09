---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: f4156fdc52ffaf01caad49517229ebf63d960fc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297110"
---
# <span data-ttu-id="f0ebe-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="f0ebe-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="f0ebe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ebe-103">UserSession leválasztása</span><span class="sxs-lookup"><span data-stu-id="f0ebe-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="f0ebe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0ebe-104">SYNTAX</span></span>

### <span data-ttu-id="f0ebe-105">Disconnect (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0ebe-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f0ebe-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0ebe-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0ebe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0ebe-107">DESCRIPTION</span></span>
<span data-ttu-id="f0ebe-108">UserSession leválasztása</span><span class="sxs-lookup"><span data-stu-id="f0ebe-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="f0ebe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f0ebe-109">EXAMPLES</span></span>

### <span data-ttu-id="f0ebe-110">Példa 1: a Windows virtuális asztali UserSession leválasztása név szerint</span><span class="sxs-lookup"><span data-stu-id="f0ebe-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="f0ebe-111">Ez a parancs leválasztja a Windows virtuális asztali UserSession a munkamenet-állomáson.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="f0ebe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0ebe-112">PARAMETERS</span></span>

### <span data-ttu-id="f0ebe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ebe-113">-DefaultProfile</span></span>
<span data-ttu-id="f0ebe-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ebe-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f0ebe-115">-HostPoolName</span></span>
<span data-ttu-id="f0ebe-116">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="f0ebe-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ebe-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f0ebe-117">-Id</span></span>
<span data-ttu-id="f0ebe-118">A felhasználó munkamenetének neve a megadott munkamenet-állomáson belül</span><span class="sxs-lookup"><span data-stu-id="f0ebe-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ebe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0ebe-119">-InputObject</span></span>
<span data-ttu-id="f0ebe-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ebe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0ebe-121">-PassThru</span></span>
<span data-ttu-id="f0ebe-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="f0ebe-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f0ebe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ebe-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0ebe-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-124">The name of the resource group.</span></span>
<span data-ttu-id="f0ebe-125">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ebe-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="f0ebe-126">-SessionHostName</span></span>
<span data-ttu-id="f0ebe-127">A megadott alkalmazáskészleten belüli munkamenet-állomás neve</span><span class="sxs-lookup"><span data-stu-id="f0ebe-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ebe-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0ebe-128">-SubscriptionId</span></span>
<span data-ttu-id="f0ebe-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ebe-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0ebe-130">-Confirm</span></span>
<span data-ttu-id="f0ebe-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ebe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ebe-132">-WhatIf</span></span>
<span data-ttu-id="f0ebe-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ebe-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ebe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ebe-135">CommonParameters</span></span>
<span data-ttu-id="f0ebe-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0ebe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ebe-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ebe-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0ebe-138">INPUTS</span></span>

### <span data-ttu-id="f0ebe-139">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f0ebe-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f0ebe-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0ebe-140">OUTPUTS</span></span>

### <span data-ttu-id="f0ebe-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0ebe-141">System.Boolean</span></span>

## <span data-ttu-id="f0ebe-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0ebe-142">NOTES</span></span>

<span data-ttu-id="f0ebe-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f0ebe-143">ALIASES</span></span>

<span data-ttu-id="f0ebe-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f0ebe-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0ebe-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0ebe-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0ebe-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f0ebe-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0ebe-148">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="f0ebe-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f0ebe-149">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="f0ebe-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f0ebe-150">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="f0ebe-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f0ebe-151">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="f0ebe-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f0ebe-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f0ebe-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0ebe-153">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f0ebe-154">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="f0ebe-155">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="f0ebe-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f0ebe-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f0ebe-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f0ebe-157">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="f0ebe-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f0ebe-158">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="f0ebe-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f0ebe-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0ebe-159">RELATED LINKS</span></span>

