---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187066"
---
# <span data-ttu-id="a1c16-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="a1c16-101">New-AzHost</span></span>

## <span data-ttu-id="a1c16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1c16-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c16-103">Egy állomást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a1c16-103">Creates a  host.</span></span>

## <span data-ttu-id="a1c16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1c16-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1c16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1c16-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c16-106">Ez a parancsmag létrehoz egy állomást.</span><span class="sxs-lookup"><span data-stu-id="a1c16-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="a1c16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a1c16-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c16-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a1c16-108">Example 1</span></span>
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

<span data-ttu-id="a1c16-109">Ezzel a paranccsal létrehozhatja a megadott SKU egy állomását a megadott Host-csoportban és az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="a1c16-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="a1c16-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1c16-110">PARAMETERS</span></span>

### <span data-ttu-id="a1c16-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1c16-111">-AsJob</span></span>
<span data-ttu-id="a1c16-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a1c16-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1c16-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="a1c16-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="a1c16-114">Annak megadása, hogy az állomást meghibásodás esetén automatikusan kell-e cserélni.</span><span class="sxs-lookup"><span data-stu-id="a1c16-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="a1c16-115">Az érték alapértelmezés szerint "true", ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="a1c16-115">The value is defaulted to 'true' when not provided.</span></span>

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

### <span data-ttu-id="a1c16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c16-116">-DefaultProfile</span></span>
<span data-ttu-id="a1c16-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1c16-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1c16-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c16-118">-HostGroupName</span></span>
<span data-ttu-id="a1c16-119">A Host csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1c16-119">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="a1c16-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a1c16-120">-LicenseType</span></span>
<span data-ttu-id="a1c16-121">Azt a szoftverlicenc-típust adja meg, amelyet az állomáson telepített VMs-szolgáltatónál alkalmazni fog.</span><span class="sxs-lookup"><span data-stu-id="a1c16-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="a1c16-122">Lehetséges értékek: nincs, Windows_Server_Hybrid és Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="a1c16-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="a1c16-123">Az alapértelmezett érték a nincs.</span><span class="sxs-lookup"><span data-stu-id="a1c16-123">Default value is None.</span></span>

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

### <span data-ttu-id="a1c16-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="a1c16-124">-Location</span></span>
<span data-ttu-id="a1c16-125">A helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1c16-125">Specifies the location.</span></span>

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

### <span data-ttu-id="a1c16-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1c16-126">-Name</span></span>
<span data-ttu-id="a1c16-127">Az állomás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1c16-127">Specifies the name of the host.</span></span>

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

### <span data-ttu-id="a1c16-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="a1c16-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="a1c16-129">Az állomás platform-meghibásodási tartományának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1c16-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="a1c16-130">Ezután a minimális érték 0, a maximális érték pedig 2.</span><span class="sxs-lookup"><span data-stu-id="a1c16-130">Then minimum value is 0 and the maximum value is 2.</span></span>

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

### <span data-ttu-id="a1c16-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c16-131">-ResourceGroupName</span></span>
<span data-ttu-id="a1c16-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a1c16-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1c16-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="a1c16-133">-Sku</span></span>
<span data-ttu-id="a1c16-134">A SKU nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1c16-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="a1c16-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="a1c16-135">-Tag</span></span>
<span data-ttu-id="a1c16-136">Címkéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="a1c16-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="a1c16-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1c16-137">-Confirm</span></span>
<span data-ttu-id="a1c16-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1c16-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1c16-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c16-139">-WhatIf</span></span>
<span data-ttu-id="a1c16-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1c16-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1c16-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1c16-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1c16-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c16-142">CommonParameters</span></span>
<span data-ttu-id="a1c16-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1c16-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c16-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1c16-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c16-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1c16-145">INPUTS</span></span>

### <span data-ttu-id="a1c16-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a1c16-146">System.String</span></span>

## <span data-ttu-id="a1c16-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1c16-147">OUTPUTS</span></span>

### <span data-ttu-id="a1c16-148">Microsoft. Azure. commands. számítási. Automation. models. PSHost</span><span class="sxs-lookup"><span data-stu-id="a1c16-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="a1c16-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1c16-149">NOTES</span></span>

## <span data-ttu-id="a1c16-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1c16-150">RELATED LINKS</span></span>