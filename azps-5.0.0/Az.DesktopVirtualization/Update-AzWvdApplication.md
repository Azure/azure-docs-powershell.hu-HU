---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187488"
---
# <span data-ttu-id="ef586-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="ef586-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="ef586-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef586-102">SYNOPSIS</span></span>
<span data-ttu-id="ef586-103">Frissítheti az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="ef586-103">Update an application.</span></span>

## <span data-ttu-id="ef586-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef586-104">SYNTAX</span></span>

### <span data-ttu-id="ef586-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef586-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ef586-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ef586-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef586-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef586-107">DESCRIPTION</span></span>
<span data-ttu-id="ef586-108">Frissítheti az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="ef586-108">Update an application.</span></span>

## <span data-ttu-id="ef586-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef586-109">EXAMPLES</span></span>

### <span data-ttu-id="ef586-110">Példa 1: a Windows virtuális asztali alkalmazás frissítése</span><span class="sxs-lookup"><span data-stu-id="ef586-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="ef586-111">Ez a parancs frissíti a Windows Virtual Desktop alkalmazást egy alkalmazás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="ef586-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="ef586-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef586-112">PARAMETERS</span></span>

### <span data-ttu-id="ef586-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="ef586-113">-CommandLineArgument</span></span>
<span data-ttu-id="ef586-114">Az alkalmazás parancssori argumentumai.</span><span class="sxs-lookup"><span data-stu-id="ef586-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="ef586-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="ef586-115">-CommandLineSetting</span></span>
<span data-ttu-id="ef586-116">Megadja, hogy ez a közzétett alkalmazás indítható-e el parancssori argumentumokkal az ügyfél által megadott parancssori argumentumokkal, vagy a parancssori argumentumokat egyáltalán nem.</span><span class="sxs-lookup"><span data-stu-id="ef586-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef586-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef586-117">-DefaultProfile</span></span>
<span data-ttu-id="ef586-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef586-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef586-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ef586-119">-Description</span></span>
<span data-ttu-id="ef586-120">Az alkalmazás leírása.</span><span class="sxs-lookup"><span data-stu-id="ef586-120">Description of Application.</span></span>

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

### <span data-ttu-id="ef586-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="ef586-121">-FilePath</span></span>
<span data-ttu-id="ef586-122">Az alkalmazás végrehajtható fájljának elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef586-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="ef586-123">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="ef586-123">-FriendlyName</span></span>
<span data-ttu-id="ef586-124">Az alkalmazás rövid neve.</span><span class="sxs-lookup"><span data-stu-id="ef586-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="ef586-125">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="ef586-125">-GroupName</span></span>
<span data-ttu-id="ef586-126">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="ef586-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef586-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="ef586-127">-IconIndex</span></span>
<span data-ttu-id="ef586-128">Az ikon indexe.</span><span class="sxs-lookup"><span data-stu-id="ef586-128">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef586-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="ef586-129">-IconPath</span></span>
<span data-ttu-id="ef586-130">Elérési út ikon.</span><span class="sxs-lookup"><span data-stu-id="ef586-130">Path to icon.</span></span>

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

### <span data-ttu-id="ef586-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef586-131">-InputObject</span></span>
<span data-ttu-id="ef586-132">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef586-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef586-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef586-133">-Name</span></span>
<span data-ttu-id="ef586-134">Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="ef586-134">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef586-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef586-135">-ResourceGroupName</span></span>
<span data-ttu-id="ef586-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef586-136">The name of the resource group.</span></span>
<span data-ttu-id="ef586-137">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ef586-137">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef586-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="ef586-138">-ShowInPortal</span></span>
<span data-ttu-id="ef586-139">Itt adhatja meg, hogy a RemoteApp program megjelenjen-e a RemoteApp-és a webes Access-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ef586-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="ef586-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef586-140">-SubscriptionId</span></span>
<span data-ttu-id="ef586-141">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef586-141">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef586-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="ef586-142">-Tag</span></span>
<span data-ttu-id="ef586-143">frissítendő Címkék</span><span class="sxs-lookup"><span data-stu-id="ef586-143">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef586-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef586-144">-Confirm</span></span>
<span data-ttu-id="ef586-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef586-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef586-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef586-146">-WhatIf</span></span>
<span data-ttu-id="ef586-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef586-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef586-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef586-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef586-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef586-149">CommonParameters</span></span>
<span data-ttu-id="ef586-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef586-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef586-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef586-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef586-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef586-152">INPUTS</span></span>

### <span data-ttu-id="ef586-153">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ef586-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ef586-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef586-154">OUTPUTS</span></span>

### <span data-ttu-id="ef586-155">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. sikertelen IApplication</span><span class="sxs-lookup"><span data-stu-id="ef586-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="ef586-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef586-156">NOTES</span></span>

<span data-ttu-id="ef586-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ef586-157">ALIASES</span></span>

<span data-ttu-id="ef586-158">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="ef586-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef586-159">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ef586-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef586-160">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ef586-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef586-161">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="ef586-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef586-162">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="ef586-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ef586-163">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="ef586-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ef586-164">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="ef586-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ef586-165">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="ef586-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ef586-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ef586-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef586-167">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef586-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ef586-168">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ef586-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="ef586-169">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="ef586-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ef586-170">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef586-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ef586-171">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="ef586-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ef586-172">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="ef586-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ef586-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef586-173">RELATED LINKS</span></span>

