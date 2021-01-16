---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357586"
---
# <span data-ttu-id="c30a0-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c30a0-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="c30a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c30a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c30a0-103">Nyilvános IP-címet kap.</span><span class="sxs-lookup"><span data-stu-id="c30a0-103">Gets a public IP address.</span></span>

## <span data-ttu-id="c30a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c30a0-104">SYNTAX</span></span>

### <span data-ttu-id="c30a0-105">NoExpandStandAloneIp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c30a0-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c30a0-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="c30a0-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c30a0-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="c30a0-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c30a0-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="c30a0-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c30a0-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c30a0-109">DESCRIPTION</span></span>
<span data-ttu-id="c30a0-110">A **Get-AzPublicIPAddress** parancsmag egy vagy több nyilvános IP-címet kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c30a0-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="c30a0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c30a0-111">EXAMPLES</span></span>

### <span data-ttu-id="c30a0-112">1. példa: Nyilvános IP-erőforrás lekérte</span><span class="sxs-lookup"><span data-stu-id="c30a0-112">Example 1: Get a public IP resource</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic", 
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="c30a0-113">Ez a parancs egy nyilvános IP-cím típusú erőforrást kap, a myPublicIp névvel a myRg erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c30a0-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="c30a0-114">2. példa: Nyilvános IP-erőforrások behozása szűréssel</span><span class="sxs-lookup"><span data-stu-id="c30a0-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="c30a0-115">Ez a parancs az összes olyan nyilvános IP-címforrást megkapja, amelynek a neve a SajátPublicIp nevével kezdődik.</span><span class="sxs-lookup"><span data-stu-id="c30a0-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="c30a0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c30a0-116">PARAMETERS</span></span>

### <span data-ttu-id="c30a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30a0-117">-DefaultProfile</span></span>
<span data-ttu-id="c30a0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c30a0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c30a0-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c30a0-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30a0-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c30a0-120">-IpConfigurationName</span></span>
<span data-ttu-id="c30a0-121">Hálózati felület IP-konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="c30a0-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30a0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c30a0-122">-Name</span></span>
<span data-ttu-id="c30a0-123">A parancsmag által bekért nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="c30a0-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c30a0-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c30a0-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="c30a0-125">Virtual Machine Network Interface Name (Virtuálisgép-hálózati felület neve).</span><span class="sxs-lookup"><span data-stu-id="c30a0-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="c30a0-127">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag nyilvános IP-címét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c30a0-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c30a0-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="c30a0-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="c30a0-129">Virtuális gépi index.</span><span class="sxs-lookup"><span data-stu-id="c30a0-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30a0-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c30a0-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="c30a0-131">Virtuálisgép-méretarány-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="c30a0-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30a0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30a0-132">CommonParameters</span></span>
<span data-ttu-id="c30a0-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c30a0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30a0-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c30a0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30a0-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c30a0-135">INPUTS</span></span>

### <span data-ttu-id="c30a0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c30a0-136">System.String</span></span>

## <span data-ttu-id="c30a0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c30a0-137">OUTPUTS</span></span>

### <span data-ttu-id="c30a0-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c30a0-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="c30a0-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c30a0-139">NOTES</span></span>

## <span data-ttu-id="c30a0-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c30a0-140">RELATED LINKS</span></span>

[<span data-ttu-id="c30a0-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c30a0-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="c30a0-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c30a0-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="c30a0-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c30a0-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


