---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 38eff375baa948098ac66c8e2b3c3fe1849f3bc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670505"
---
# <span data-ttu-id="1275b-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1275b-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="1275b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1275b-102">SYNOPSIS</span></span>
<span data-ttu-id="1275b-103">Nyilvános IP-címet kap.</span><span class="sxs-lookup"><span data-stu-id="1275b-103">Gets a public IP address.</span></span>

## <span data-ttu-id="1275b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1275b-104">SYNTAX</span></span>

### <span data-ttu-id="1275b-105">NoExpandStandAloneIp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1275b-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1275b-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="1275b-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1275b-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="1275b-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1275b-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="1275b-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1275b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1275b-109">DESCRIPTION</span></span>
<span data-ttu-id="1275b-110">A **Get-AzPublicIPAddress** parancsmag egy vagy több nyilvános IP-címet kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="1275b-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="1275b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1275b-111">EXAMPLES</span></span>

### <span data-ttu-id="1275b-112">1: nyilvános IP-erőforrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="1275b-112">1: Get a public IP resource</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="1275b-113">Ez a parancs a myPublicIp nevű nyilvános IP-cím erőforrást kapja meg az erőforráscsoport myRg.</span><span class="sxs-lookup"><span data-stu-id="1275b-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="1275b-114">2: a nyilvános IP-források szűréssel való beszerzése</span><span class="sxs-lookup"><span data-stu-id="1275b-114">2: Get public IP resources using filtering</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="1275b-115">Ez a parancs minden nyilvános IP-cím típusú erőforrást beolvas, amelynek a neve myPublicIp-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="1275b-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="1275b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1275b-116">PARAMETERS</span></span>

### <span data-ttu-id="1275b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1275b-117">-DefaultProfile</span></span>
<span data-ttu-id="1275b-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1275b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1275b-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1275b-119">-ExpandResource</span></span>
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

### <span data-ttu-id="1275b-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1275b-120">-IpConfigurationName</span></span>
<span data-ttu-id="1275b-121">Hálózati kapcsolat IP-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="1275b-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="1275b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1275b-122">-Name</span></span>
<span data-ttu-id="1275b-123">Annak a nyilvános IP-címnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="1275b-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1275b-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="1275b-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="1275b-125">Virtuális gép hálózati felületének neve.</span><span class="sxs-lookup"><span data-stu-id="1275b-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="1275b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1275b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1275b-127">Annak a csoportnak a neve, amely a parancsmag által beolvasott nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1275b-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1275b-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="1275b-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="1275b-129">Virtuális gép indexe.</span><span class="sxs-lookup"><span data-stu-id="1275b-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="1275b-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1275b-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="1275b-131">Virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="1275b-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="1275b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1275b-132">CommonParameters</span></span>
<span data-ttu-id="1275b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1275b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1275b-134">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1275b-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1275b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1275b-135">INPUTS</span></span>

### <span data-ttu-id="1275b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1275b-136">System.String</span></span>

## <span data-ttu-id="1275b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1275b-137">OUTPUTS</span></span>

### <span data-ttu-id="1275b-138">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1275b-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="1275b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1275b-139">NOTES</span></span>

## <span data-ttu-id="1275b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1275b-140">RELATED LINKS</span></span>

[<span data-ttu-id="1275b-141">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1275b-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="1275b-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1275b-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="1275b-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1275b-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


