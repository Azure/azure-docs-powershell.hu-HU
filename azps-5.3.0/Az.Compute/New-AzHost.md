---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480825"
---
# <span data-ttu-id="a84ed-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="a84ed-101">New-AzHost</span></span>

## <span data-ttu-id="a84ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a84ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a84ed-103">Létrehoz egy állomást.</span><span class="sxs-lookup"><span data-stu-id="a84ed-103">Creates a  host.</span></span>

## <span data-ttu-id="a84ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a84ed-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a84ed-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a84ed-105">DESCRIPTION</span></span>
<span data-ttu-id="a84ed-106">Ez a parancsmag létrehoz egy állomást.</span><span class="sxs-lookup"><span data-stu-id="a84ed-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="a84ed-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a84ed-107">EXAMPLES</span></span>

### <span data-ttu-id="a84ed-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a84ed-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="a84ed-109">Ez a parancs létrehozza a megadott termékváltozat állomását az adott gazdacsoportban és a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="a84ed-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="a84ed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a84ed-110">PARAMETERS</span></span>

### <span data-ttu-id="a84ed-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a84ed-111">-AsJob</span></span>
<span data-ttu-id="a84ed-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a84ed-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a84ed-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="a84ed-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="a84ed-114">Azt adja meg, hogy hiba esetén az állomást automatikusan cserélje-e le a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a84ed-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="a84ed-115">Ha nincs megjelölve, az érték alapértelmezés szerint "igaz" lesz.</span><span class="sxs-lookup"><span data-stu-id="a84ed-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84ed-116">-DefaultProfile</span></span>
<span data-ttu-id="a84ed-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a84ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="a84ed-118">-HostGroupName</span></span>
<span data-ttu-id="a84ed-119">A gazdacsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a84ed-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a84ed-120">-LicenseType</span></span>
<span data-ttu-id="a84ed-121">Azt a szoftverlicenc-típust adja meg, amely az állomáson telepített virtuális gépekre fog vonatkozni.</span><span class="sxs-lookup"><span data-stu-id="a84ed-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="a84ed-122">Lehetséges értékek: Nincs, Windows_Server_Hybrid és Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="a84ed-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="a84ed-123">Az alapértelmezett érték a Nincs.</span><span class="sxs-lookup"><span data-stu-id="a84ed-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-124">-Location</span><span class="sxs-lookup"><span data-stu-id="a84ed-124">-Location</span></span>
<span data-ttu-id="a84ed-125">Megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="a84ed-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a84ed-126">-Name</span></span>
<span data-ttu-id="a84ed-127">Az állomás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a84ed-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="a84ed-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="a84ed-129">Az állomás platformhiba-tartományának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a84ed-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="a84ed-130">Ezután a minimális érték 0, a maximális érték pedig 2.</span><span class="sxs-lookup"><span data-stu-id="a84ed-130">Then minimum value is 0 and the maximum value is 2.</span></span>

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

### <span data-ttu-id="a84ed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a84ed-131">-ResourceGroupName</span></span>
<span data-ttu-id="a84ed-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a84ed-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="a84ed-133">-Sku</span></span>
<span data-ttu-id="a84ed-134">A termékváltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a84ed-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="a84ed-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a84ed-135">-Tag</span></span>
<span data-ttu-id="a84ed-136">Címkéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="a84ed-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="a84ed-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a84ed-137">-Confirm</span></span>
<span data-ttu-id="a84ed-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a84ed-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a84ed-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a84ed-139">-WhatIf</span></span>
<span data-ttu-id="a84ed-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a84ed-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a84ed-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a84ed-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a84ed-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84ed-142">CommonParameters</span></span>
<span data-ttu-id="a84ed-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84ed-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84ed-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a84ed-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84ed-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a84ed-145">INPUTS</span></span>

### <span data-ttu-id="a84ed-146">System.String</span><span class="sxs-lookup"><span data-stu-id="a84ed-146">System.String</span></span>

## <span data-ttu-id="a84ed-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a84ed-147">OUTPUTS</span></span>

### <span data-ttu-id="a84ed-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="a84ed-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="a84ed-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a84ed-149">NOTES</span></span>

## <span data-ttu-id="a84ed-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a84ed-150">RELATED LINKS</span></span>
