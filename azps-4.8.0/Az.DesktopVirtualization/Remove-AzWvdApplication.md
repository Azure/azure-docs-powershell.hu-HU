---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c2604531014283b3599adb94c4a12d70761e1533
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185009"
---
# <span data-ttu-id="99769-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="99769-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="99769-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99769-102">SYNOPSIS</span></span>
<span data-ttu-id="99769-103">Távolítson el egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="99769-103">Remove an application.</span></span>

## <span data-ttu-id="99769-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99769-104">SYNTAX</span></span>

### <span data-ttu-id="99769-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99769-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99769-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99769-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99769-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="99769-107">DESCRIPTION</span></span>
<span data-ttu-id="99769-108">Távolítson el egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="99769-108">Remove an application.</span></span>

## <span data-ttu-id="99769-109">Példák</span><span class="sxs-lookup"><span data-stu-id="99769-109">EXAMPLES</span></span>

### <span data-ttu-id="99769-110">Példa 1: a Windows virtuális asztali alkalmazás törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="99769-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="99769-111">Ez a parancs törli a Windows Virtual Desktop alkalmazást egy alkalmazás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="99769-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="99769-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99769-112">PARAMETERS</span></span>

### <span data-ttu-id="99769-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99769-113">-DefaultProfile</span></span>
<span data-ttu-id="99769-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99769-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99769-115">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="99769-115">-GroupName</span></span>
<span data-ttu-id="99769-116">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="99769-116">The name of the application group</span></span>

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

### <span data-ttu-id="99769-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99769-117">-InputObject</span></span>
<span data-ttu-id="99769-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99769-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99769-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99769-119">-Name</span></span>
<span data-ttu-id="99769-120">Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="99769-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99769-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99769-121">-PassThru</span></span>
<span data-ttu-id="99769-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="99769-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="99769-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99769-123">-ResourceGroupName</span></span>
<span data-ttu-id="99769-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="99769-124">The name of the resource group.</span></span>
<span data-ttu-id="99769-125">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="99769-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="99769-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99769-126">-SubscriptionId</span></span>
<span data-ttu-id="99769-127">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="99769-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="99769-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99769-128">-Confirm</span></span>
<span data-ttu-id="99769-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99769-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99769-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99769-130">-WhatIf</span></span>
<span data-ttu-id="99769-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99769-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99769-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99769-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99769-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99769-133">CommonParameters</span></span>
<span data-ttu-id="99769-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99769-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99769-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99769-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99769-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99769-136">INPUTS</span></span>

### <span data-ttu-id="99769-137">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="99769-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="99769-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99769-138">OUTPUTS</span></span>

### <span data-ttu-id="99769-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99769-139">System.Boolean</span></span>

## <span data-ttu-id="99769-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99769-140">NOTES</span></span>

<span data-ttu-id="99769-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="99769-141">ALIASES</span></span>

<span data-ttu-id="99769-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="99769-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99769-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="99769-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99769-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="99769-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99769-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="99769-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99769-146">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="99769-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="99769-147">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="99769-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="99769-148">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="99769-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="99769-149">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="99769-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="99769-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="99769-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99769-151">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="99769-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="99769-152">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="99769-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="99769-153">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="99769-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="99769-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="99769-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="99769-155">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="99769-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="99769-156">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="99769-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="99769-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99769-157">RELATED LINKS</span></span>

