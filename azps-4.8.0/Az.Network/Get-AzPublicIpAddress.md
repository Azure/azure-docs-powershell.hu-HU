---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 9df5cdd2a601977b453cb8242a9241cede3d4539
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180546"
---
# <span data-ttu-id="bc0f8-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc0f8-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="bc0f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0f8-103">Nyilvános IP-címet kap.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-103">Gets a public IP address.</span></span>

## <span data-ttu-id="bc0f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc0f8-104">SYNTAX</span></span>

### <span data-ttu-id="bc0f8-105">NoExpandStandAloneIp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc0f8-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc0f8-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="bc0f8-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc0f8-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="bc0f8-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc0f8-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="bc0f8-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc0f8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc0f8-109">DESCRIPTION</span></span>
<span data-ttu-id="bc0f8-110">A **Get-AzPublicIPAddress** parancsmag egy vagy több nyilvános IP-címet kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="bc0f8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bc0f8-111">EXAMPLES</span></span>

### <span data-ttu-id="bc0f8-112">Példa 1: nyilvános IP-erőforrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="bc0f8-112">Example 1: Get a public IP resource</span></span>
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="bc0f8-113">Ez a parancs a myPublicIp nevű nyilvános IP-cím erőforrást kapja meg az erőforráscsoport myRg.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="bc0f8-114">2. példa: a nyilvános IP-források szűréssel történő beszerzése</span><span class="sxs-lookup"><span data-stu-id="bc0f8-114">Example 2: Get public IP resources using filtering</span></span>
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="bc0f8-115">Ez a parancs minden nyilvános IP-cím típusú erőforrást beolvas, amelynek a neve myPublicIp-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="bc0f8-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc0f8-116">PARAMETERS</span></span>

### <span data-ttu-id="bc0f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0f8-117">-DefaultProfile</span></span>
<span data-ttu-id="bc0f8-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc0f8-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="bc0f8-119">-ExpandResource</span></span>
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

### <span data-ttu-id="bc0f8-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bc0f8-120">-IpConfigurationName</span></span>
<span data-ttu-id="bc0f8-121">Hálózati kapcsolat IP-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="bc0f8-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="bc0f8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc0f8-122">-Name</span></span>
<span data-ttu-id="bc0f8-123">Annak a nyilvános IP-címnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bc0f8-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="bc0f8-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="bc0f8-125">Virtuális gép hálózati felületének neve.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="bc0f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc0f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc0f8-127">Annak a csoportnak a neve, amely a parancsmag által beolvasott nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bc0f8-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="bc0f8-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="bc0f8-129">Virtuális gép indexe.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="bc0f8-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bc0f8-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="bc0f8-131">Virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="bc0f8-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="bc0f8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0f8-132">CommonParameters</span></span>
<span data-ttu-id="bc0f8-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc0f8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0f8-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0f8-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc0f8-135">INPUTS</span></span>

### <span data-ttu-id="bc0f8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bc0f8-136">System.String</span></span>

## <span data-ttu-id="bc0f8-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc0f8-137">OUTPUTS</span></span>

### <span data-ttu-id="bc0f8-138">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc0f8-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="bc0f8-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc0f8-139">NOTES</span></span>

## <span data-ttu-id="bc0f8-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc0f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="bc0f8-141">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc0f8-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="bc0f8-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc0f8-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="bc0f8-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc0f8-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


