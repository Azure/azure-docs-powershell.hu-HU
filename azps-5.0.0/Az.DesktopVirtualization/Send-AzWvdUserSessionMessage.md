---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 047ede26246c31b17fbeb49fca4353b2cb17594c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296966"
---
# <span data-ttu-id="eea45-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="eea45-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="eea45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eea45-102">SYNOPSIS</span></span>
<span data-ttu-id="eea45-103">Üzenet küldése egy felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="eea45-103">Send a message to a user.</span></span>

## <span data-ttu-id="eea45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eea45-104">SYNTAX</span></span>

### <span data-ttu-id="eea45-105">SendExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eea45-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eea45-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eea45-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eea45-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eea45-107">DESCRIPTION</span></span>
<span data-ttu-id="eea45-108">Üzenet küldése egy felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="eea45-108">Send a message to a user.</span></span>

## <span data-ttu-id="eea45-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eea45-109">EXAMPLES</span></span>

### <span data-ttu-id="eea45-110">1. példa: üzenet küldése az UserSession-ra</span><span class="sxs-lookup"><span data-stu-id="eea45-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="eea45-111">Ez a parancs üzenetet küld egy UserSession.</span><span class="sxs-lookup"><span data-stu-id="eea45-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="eea45-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eea45-112">PARAMETERS</span></span>

### <span data-ttu-id="eea45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea45-113">-DefaultProfile</span></span>
<span data-ttu-id="eea45-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eea45-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea45-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="eea45-115">-HostPoolName</span></span>
<span data-ttu-id="eea45-116">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="eea45-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea45-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eea45-117">-InputObject</span></span>
<span data-ttu-id="eea45-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eea45-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eea45-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="eea45-119">-MessageBody</span></span>
<span data-ttu-id="eea45-120">Az üzenet törzsébe.</span><span class="sxs-lookup"><span data-stu-id="eea45-120">Body of message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea45-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="eea45-121">-MessageTitle</span></span>
<span data-ttu-id="eea45-122">Az üzenet címe.</span><span class="sxs-lookup"><span data-stu-id="eea45-122">Title of message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea45-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eea45-123">-PassThru</span></span>
<span data-ttu-id="eea45-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="eea45-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eea45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea45-125">-ResourceGroupName</span></span>
<span data-ttu-id="eea45-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eea45-126">The name of the resource group.</span></span>
<span data-ttu-id="eea45-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="eea45-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea45-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="eea45-128">-SessionHostName</span></span>
<span data-ttu-id="eea45-129">A megadott alkalmazáskészleten belüli munkamenet-állomás neve</span><span class="sxs-lookup"><span data-stu-id="eea45-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea45-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eea45-130">-SubscriptionId</span></span>
<span data-ttu-id="eea45-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eea45-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea45-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="eea45-132">-UserSessionId</span></span>
<span data-ttu-id="eea45-133">A felhasználó munkamenetének neve a megadott munkamenet-állomáson belül</span><span class="sxs-lookup"><span data-stu-id="eea45-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea45-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eea45-134">-Confirm</span></span>
<span data-ttu-id="eea45-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eea45-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea45-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea45-136">-WhatIf</span></span>
<span data-ttu-id="eea45-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eea45-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea45-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eea45-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea45-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea45-139">CommonParameters</span></span>
<span data-ttu-id="eea45-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eea45-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea45-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eea45-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea45-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eea45-142">INPUTS</span></span>

### <span data-ttu-id="eea45-143">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="eea45-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="eea45-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eea45-144">OUTPUTS</span></span>

### <span data-ttu-id="eea45-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eea45-145">System.Boolean</span></span>

## <span data-ttu-id="eea45-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eea45-146">NOTES</span></span>

<span data-ttu-id="eea45-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eea45-147">ALIASES</span></span>

<span data-ttu-id="eea45-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="eea45-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eea45-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="eea45-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eea45-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="eea45-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eea45-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="eea45-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eea45-152">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="eea45-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="eea45-153">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="eea45-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="eea45-154">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="eea45-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="eea45-155">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="eea45-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="eea45-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="eea45-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eea45-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eea45-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="eea45-158">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="eea45-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="eea45-159">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="eea45-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="eea45-160">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eea45-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="eea45-161">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="eea45-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="eea45-162">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="eea45-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="eea45-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eea45-163">RELATED LINKS</span></span>

