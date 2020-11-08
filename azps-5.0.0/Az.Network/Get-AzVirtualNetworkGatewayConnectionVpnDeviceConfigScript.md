---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187276"
---
# <span data-ttu-id="16dd5-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="16dd5-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="16dd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="16dd5-103">Ez a parancsmagot átveszi a kapcsolati erőforrást, a VPN-eszköz márkáját, a modellt, a firmware-verziót, és visszaadja a megfelelő konfigurációs parancsfájlt, amelyet az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközökön.</span><span class="sxs-lookup"><span data-stu-id="16dd5-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="16dd5-104">A parancsfájl követi a kijelölt eszköz szintaxisát, és adja meg a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagokat, a VPN-alagút előre megosztott kulcsát stb.</span><span class="sxs-lookup"><span data-stu-id="16dd5-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="16dd5-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16dd5-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16dd5-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="16dd5-106">DESCRIPTION</span></span>
<span data-ttu-id="16dd5-107">Ez a parancsmagot átveszi a kapcsolati erőforrást, a VPN-eszköz márkáját, a modellt, a firmware-verziót, és visszaadja a megfelelő konfigurációs parancsfájlt, amelyet az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközökön.</span><span class="sxs-lookup"><span data-stu-id="16dd5-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="16dd5-108">A parancsfájl követi a kijelölt eszköz szintaxisát, és adja meg a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagokat, a VPN-alagút előre megosztott kulcsát stb.</span><span class="sxs-lookup"><span data-stu-id="16dd5-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="16dd5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="16dd5-109">EXAMPLES</span></span>

### <span data-ttu-id="16dd5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="16dd5-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="16dd5-111">A fenti példa a Get-AzVirtualNetworkGatewaySupportedVpnDevice használatával támogatja a támogatott VPN-eszközök márkáit, modelljeit és firmware-verzióit.</span><span class="sxs-lookup"><span data-stu-id="16dd5-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="16dd5-112">Ezután a kapott modellek egyikét használja a virtuális magánhálózati eszközök konfigurációs parancsfájljának a "TestConnection" VirtualNetworkGatewayConnection való generálásához.</span><span class="sxs-lookup"><span data-stu-id="16dd5-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="16dd5-113">Az ebben a példában használt eszköz "IOS-teszt", DeviceVendor "Cisco-teszt" és FirmwareVersion 20 DeviceFamily tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="16dd5-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="16dd5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16dd5-114">PARAMETERS</span></span>

### <span data-ttu-id="16dd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dd5-115">-DefaultProfile</span></span>
<span data-ttu-id="16dd5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16dd5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16dd5-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="16dd5-117">-DeviceFamily</span></span>
<span data-ttu-id="16dd5-118">A VPN-eszköz modelljének/családjának neve.</span><span class="sxs-lookup"><span data-stu-id="16dd5-118">Name of the VPN device model/family.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16dd5-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="16dd5-119">-DeviceVendor</span></span>
<span data-ttu-id="16dd5-120">A VPN-eszköz szállítójának neve</span><span class="sxs-lookup"><span data-stu-id="16dd5-120">Name of the VPN device vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16dd5-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="16dd5-121">-FirmwareVersion</span></span>
<span data-ttu-id="16dd5-122">A VPN-eszköz firmware-verziója.</span><span class="sxs-lookup"><span data-stu-id="16dd5-122">Firmware version of the VPN device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16dd5-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="16dd5-123">-Name</span></span>
<span data-ttu-id="16dd5-124">Annak a kapcsolatnak az erőforrás neve, amelyhez a konfigurációt létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="16dd5-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16dd5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16dd5-125">-ResourceGroupName</span></span>
<span data-ttu-id="16dd5-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="16dd5-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16dd5-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="16dd5-127">-Confirm</span></span>
<span data-ttu-id="16dd5-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="16dd5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16dd5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16dd5-129">-WhatIf</span></span>
<span data-ttu-id="16dd5-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="16dd5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16dd5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16dd5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16dd5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dd5-132">CommonParameters</span></span>
<span data-ttu-id="16dd5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16dd5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dd5-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="16dd5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dd5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16dd5-135">INPUTS</span></span>

### <span data-ttu-id="16dd5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="16dd5-136">System.String</span></span>

## <span data-ttu-id="16dd5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16dd5-137">OUTPUTS</span></span>

### <span data-ttu-id="16dd5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="16dd5-138">System.String</span></span>

## <span data-ttu-id="16dd5-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16dd5-139">NOTES</span></span>

## <span data-ttu-id="16dd5-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16dd5-140">RELATED LINKS</span></span>