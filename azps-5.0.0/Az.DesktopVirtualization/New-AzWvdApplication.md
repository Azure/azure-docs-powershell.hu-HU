---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297047"
---
# <span data-ttu-id="5fe9c-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="5fe9c-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="5fe9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fe9c-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe9c-103">Alkalmazás létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="5fe9c-103">Create or update an application.</span></span>

## <span data-ttu-id="5fe9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fe9c-104">SYNTAX</span></span>

### <span data-ttu-id="5fe9c-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5fe9c-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5fe9c-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="5fe9c-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5fe9c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fe9c-107">DESCRIPTION</span></span>
<span data-ttu-id="5fe9c-108">Alkalmazás létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="5fe9c-108">Create or update an application.</span></span>

## <span data-ttu-id="5fe9c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5fe9c-109">EXAMPLES</span></span>

### <span data-ttu-id="5fe9c-110">Példa 1: Windows virtuális asztali alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fe9c-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
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

<span data-ttu-id="5fe9c-111">Ez a parancs egy Windows virtuális asztali alkalmazást hoz létre egy alkalmazás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="5fe9c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fe9c-112">PARAMETERS</span></span>

### <span data-ttu-id="5fe9c-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="5fe9c-113">-AppAlias</span></span>
<span data-ttu-id="5fe9c-114">Az App alias a Start menüből</span><span class="sxs-lookup"><span data-stu-id="5fe9c-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="5fe9c-115">-CommandLineArgument</span></span>
<span data-ttu-id="5fe9c-116">Az alkalmazás parancssori argumentumai.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-116">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="5fe9c-117">-CommandLineSetting</span></span>
<span data-ttu-id="5fe9c-118">Megadja, hogy ez a közzétett alkalmazás indítható-e el parancssori argumentumokkal az ügyfél által megadott parancssori argumentumokkal, vagy a parancssori argumentumokat egyáltalán nem.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe9c-119">-DefaultProfile</span></span>
<span data-ttu-id="5fe9c-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe9c-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5fe9c-121">-Description</span></span>
<span data-ttu-id="5fe9c-122">Az alkalmazás leírása.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-122">Description of Application.</span></span>

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

### <span data-ttu-id="5fe9c-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5fe9c-123">-FilePath</span></span>
<span data-ttu-id="5fe9c-124">Az alkalmazás végrehajtható fájljának elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-124">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-125">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="5fe9c-125">-FriendlyName</span></span>
<span data-ttu-id="5fe9c-126">Az alkalmazás rövid neve.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="5fe9c-127">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="5fe9c-127">-GroupName</span></span>
<span data-ttu-id="5fe9c-128">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="5fe9c-128">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="5fe9c-129">-IconIndex</span></span>
<span data-ttu-id="5fe9c-130">Az ikon indexe.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-130">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="5fe9c-131">-IconPath</span></span>
<span data-ttu-id="5fe9c-132">Elérési út ikon.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-132">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5fe9c-133">-Name</span></span>
<span data-ttu-id="5fe9c-134">Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="5fe9c-134">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe9c-135">-ResourceGroupName</span></span>
<span data-ttu-id="5fe9c-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-136">The name of the resource group.</span></span>
<span data-ttu-id="5fe9c-137">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-137">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="5fe9c-138">-ShowInPortal</span></span>
<span data-ttu-id="5fe9c-139">Itt adhatja meg, hogy a RemoteApp program megjelenjen-e a RemoteApp-és a webes Access-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="5fe9c-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fe9c-140">-SubscriptionId</span></span>
<span data-ttu-id="5fe9c-141">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-141">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9c-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5fe9c-142">-Confirm</span></span>
<span data-ttu-id="5fe9c-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fe9c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe9c-144">-WhatIf</span></span>
<span data-ttu-id="5fe9c-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe9c-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fe9c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe9c-147">CommonParameters</span></span>
<span data-ttu-id="5fe9c-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fe9c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe9c-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5fe9c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe9c-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fe9c-150">INPUTS</span></span>

## <span data-ttu-id="5fe9c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fe9c-151">OUTPUTS</span></span>

### <span data-ttu-id="5fe9c-152">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. sikertelen IApplication</span><span class="sxs-lookup"><span data-stu-id="5fe9c-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="5fe9c-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fe9c-153">NOTES</span></span>

<span data-ttu-id="5fe9c-154">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5fe9c-154">ALIASES</span></span>

## <span data-ttu-id="5fe9c-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fe9c-155">RELATED LINKS</span></span>

