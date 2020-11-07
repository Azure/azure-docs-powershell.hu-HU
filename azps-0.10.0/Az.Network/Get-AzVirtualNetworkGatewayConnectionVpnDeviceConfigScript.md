---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 3d955b2133f4a262b69de1413c5a4bf4d8e719b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841490"
---
# <span data-ttu-id="e0162-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="e0162-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="e0162-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0162-102">SYNOPSIS</span></span>
<span data-ttu-id="e0162-103">Ez a parancsmagot átveszi a kapcsolati erőforrást, a VPN-eszköz márkáját, a modellt, a firmware-verziót, és visszaadja a megfelelő konfigurációs parancsfájlt, amelyet az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközökön.</span><span class="sxs-lookup"><span data-stu-id="e0162-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="e0162-104">A parancsfájl követi a kijelölt eszköz szintaxisát, és adja meg a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagokat, a VPN-alagút előre megosztott kulcsát stb.</span><span class="sxs-lookup"><span data-stu-id="e0162-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="e0162-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0162-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0162-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0162-106">DESCRIPTION</span></span>
<span data-ttu-id="e0162-107">Ez a parancsmagot átveszi a kapcsolati erőforrást, a VPN-eszköz márkáját, a modellt, a firmware-verziót, és visszaadja a megfelelő konfigurációs parancsfájlt, amelyet az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközökön.</span><span class="sxs-lookup"><span data-stu-id="e0162-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="e0162-108">A parancsfájl követi a kijelölt eszköz szintaxisát, és adja meg a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagokat, a VPN-alagút előre megosztott kulcsát stb.</span><span class="sxs-lookup"><span data-stu-id="e0162-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="e0162-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e0162-109">EXAMPLES</span></span>

### <span data-ttu-id="e0162-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e0162-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="e0162-111">A fenti példa a Get-AzVirtualNetworkGatewaySupportedVpnDevice használatával támogatja a támogatott VPN-eszközök márkáit, modelljeit és firmware-verzióit.</span><span class="sxs-lookup"><span data-stu-id="e0162-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="e0162-112">Ezután a kapott modellek egyikét használja a virtuális magánhálózati eszközök konfigurációs parancsfájljának a "TestConnection" VirtualNetworkGatewayConnection való generálásához.</span><span class="sxs-lookup"><span data-stu-id="e0162-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="e0162-113">Az ebben a példában használt eszköz "IOS-teszt", DeviceVendor "Cisco-teszt" és FirmwareVersion 20 DeviceFamily tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e0162-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="e0162-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0162-114">PARAMETERS</span></span>

### <span data-ttu-id="e0162-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0162-115">-DefaultProfile</span></span>
<span data-ttu-id="e0162-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0162-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0162-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="e0162-117">-DeviceFamily</span></span>
<span data-ttu-id="e0162-118">A VPN-eszköz modelljének/családjának neve.</span><span class="sxs-lookup"><span data-stu-id="e0162-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="e0162-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="e0162-119">-DeviceVendor</span></span>
<span data-ttu-id="e0162-120">A VPN-eszköz szállítójának neve</span><span class="sxs-lookup"><span data-stu-id="e0162-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="e0162-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="e0162-121">-FirmwareVersion</span></span>
<span data-ttu-id="e0162-122">A VPN-eszköz firmware-verziója.</span><span class="sxs-lookup"><span data-stu-id="e0162-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="e0162-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0162-123">-Name</span></span>
<span data-ttu-id="e0162-124">Annak a kapcsolatnak az erőforrás neve, amelyhez a konfigurációt létre szeretné venni.</span><span class="sxs-lookup"><span data-stu-id="e0162-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="e0162-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0162-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0162-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0162-126">The resource group name.</span></span>

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

### <span data-ttu-id="e0162-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0162-127">-Confirm</span></span>
<span data-ttu-id="e0162-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0162-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0162-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0162-129">-WhatIf</span></span>
<span data-ttu-id="e0162-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0162-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0162-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0162-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0162-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0162-132">CommonParameters</span></span>
<span data-ttu-id="e0162-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0162-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0162-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0162-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0162-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0162-135">INPUTS</span></span>

### <span data-ttu-id="e0162-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e0162-136">System.String</span></span>

## <span data-ttu-id="e0162-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0162-137">OUTPUTS</span></span>

### <span data-ttu-id="e0162-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e0162-138">System.String</span></span>

## <span data-ttu-id="e0162-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0162-139">NOTES</span></span>

## <span data-ttu-id="e0162-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0162-140">RELATED LINKS</span></span>

