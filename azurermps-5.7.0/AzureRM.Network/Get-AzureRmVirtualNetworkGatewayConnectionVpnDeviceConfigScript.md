---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 3fb557f29203971d54674f0f18476e249644eeb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505447"
---
# <span data-ttu-id="9a6a3-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="9a6a3-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="9a6a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6a3-103">Ez a parancsmagot átveszi a kapcsolati erőforrást, a VPN-eszköz márkáját, a modellt, a firmware-verziót, és visszaadja a megfelelő konfigurációs parancsfájlt, amelyet az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközökön.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="9a6a3-104">A parancsfájl követi a kijelölt eszköz szintaxisát, és adja meg a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagokat, a VPN-alagút előre megosztott kulcsát stb.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a6a3-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a6a3-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a6a3-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a6a3-106">DESCRIPTION</span></span>
<span data-ttu-id="9a6a3-107">Ez a parancsmagot átveszi a kapcsolati erőforrást, a VPN-eszköz márkáját, a modellt, a firmware-verziót, és visszaadja a megfelelő konfigurációs parancsfájlt, amelyet az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközökön.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="9a6a3-108">A parancsfájl követi a kijelölt eszköz szintaxisát, és adja meg a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagokat, a VPN-alagút előre megosztott kulcsát stb.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="9a6a3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9a6a3-109">EXAMPLES</span></span>

### <span data-ttu-id="9a6a3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9a6a3-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="9a6a3-111">A fenti példa a Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice használatával támogatja a támogatott VPN-eszközök márkáit, modelljeit és firmware-verzióit.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="9a6a3-112">Ezután a kapott modellek egyikét használja a virtuális magánhálózati eszközök konfigurációs parancsfájljának a "TestConnection" VirtualNetworkGatewayConnection való generálásához.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="9a6a3-113">Az ebben a példában használt eszköz "IOS-teszt", DeviceVendor "Cisco-teszt" és FirmwareVersion 20 DeviceFamily tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="9a6a3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a6a3-114">PARAMETERS</span></span>

### <span data-ttu-id="9a6a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6a3-115">-DefaultProfile</span></span>
<span data-ttu-id="9a6a3-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a3-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="9a6a3-117">-DeviceFamily</span></span>
<span data-ttu-id="9a6a3-118">A VPN-eszköz modelljének/családjának neve.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-118">Name of the VPN device model/family.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a3-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="9a6a3-119">-DeviceVendor</span></span>
<span data-ttu-id="9a6a3-120">A VPN-eszköz szállítójának neve</span><span class="sxs-lookup"><span data-stu-id="9a6a3-120">Name of the VPN device vendor.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a3-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="9a6a3-121">-FirmwareVersion</span></span>
<span data-ttu-id="9a6a3-122">A VPN-eszköz firmware-verziója.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-122">Firmware version of the VPN device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a3-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a6a3-123">-Name</span></span>
<span data-ttu-id="9a6a3-124">Annak a kapcsolatnak az erőforrás neve, amelyhez a konfigurációt létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a6a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="9a6a3-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a3-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a6a3-127">-Confirm</span></span>
<span data-ttu-id="9a6a3-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a6a3-129">-WhatIf</span></span>
<span data-ttu-id="9a6a3-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a6a3-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6a3-132">CommonParameters</span></span>
<span data-ttu-id="9a6a3-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a6a3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6a3-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a6a3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6a3-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a6a3-135">INPUTS</span></span>

### <span data-ttu-id="9a6a3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9a6a3-136">System.String</span></span>

## <span data-ttu-id="9a6a3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a6a3-137">OUTPUTS</span></span>

### <span data-ttu-id="9a6a3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9a6a3-138">System.String</span></span>

## <span data-ttu-id="9a6a3-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a6a3-139">NOTES</span></span>

## <span data-ttu-id="9a6a3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a6a3-140">RELATED LINKS</span></span>

