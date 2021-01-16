---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335621"
---
# <span data-ttu-id="383c6-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="383c6-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="383c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="383c6-102">SYNOPSIS</span></span>
<span data-ttu-id="383c6-103">Ez a parancsmag a kapcsolaterőforrást, a VPN-eszköz márkát, a modellt, a belső vezérlőprogram verzióját veszi fel, és visszaadja a megfelelő konfigurációs parancsfájlt, amit az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközeiken.</span><span class="sxs-lookup"><span data-stu-id="383c6-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="383c6-104">A parancsfájl a kijelölt eszköz szintaxisát követi, és kitölti a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagját, a VPN-átjáró előre megosztott kulcsát stb., így az ügyfelek egyszerűen másolhat és illeszthet be VPN-eszközkonfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="383c6-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="383c6-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="383c6-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="383c6-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="383c6-106">DESCRIPTION</span></span>
<span data-ttu-id="383c6-107">Ez a parancsmag a kapcsolaterőforrást, a VPN-eszköz márkát, a modellt, a belső vezérlőprogram verzióját veszi fel, és visszaadja a megfelelő konfigurációs parancsfájlt, amit az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközeiken.</span><span class="sxs-lookup"><span data-stu-id="383c6-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="383c6-108">A parancsfájl a kijelölt eszköz szintaxisát követi, és kitölti a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagját, a VPN-átjáró előre megosztott kulcsát stb., így az ügyfelek egyszerűen másolhat és illeszthet be VPN-eszközkonfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="383c6-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="383c6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="383c6-109">EXAMPLES</span></span>

### <span data-ttu-id="383c6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="383c6-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="383c6-111">A fenti példa Get-AzVirtualNetworkGatewaySupportedVpnDevice virtuális magánhálózati eszközmárkák, -modellek és belső vezérlőprogram-verziók lekértéhez.</span><span class="sxs-lookup"><span data-stu-id="383c6-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="383c6-112">Ezután a visszaadott modellinformációk egyikével létrehoz egy VPN-eszköz konfigurációs parancsfájlt a VirtualNetworkGatewayConnection "TestConnection" szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="383c6-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="383c6-113">A példában használt eszközben a DeviceFamily "IOS-Test", a DeviceVendor "Cisco-Test" és a FirmwareVersion 20 található.</span><span class="sxs-lookup"><span data-stu-id="383c6-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="383c6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="383c6-114">PARAMETERS</span></span>

### <span data-ttu-id="383c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="383c6-115">-DefaultProfile</span></span>
<span data-ttu-id="383c6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="383c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="383c6-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="383c6-117">-DeviceFamily</span></span>
<span data-ttu-id="383c6-118">A VPN-eszközmodell/-család neve.</span><span class="sxs-lookup"><span data-stu-id="383c6-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="383c6-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="383c6-119">-DeviceVendor</span></span>
<span data-ttu-id="383c6-120">A VPN-eszköz szállítójának neve.</span><span class="sxs-lookup"><span data-stu-id="383c6-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="383c6-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="383c6-121">-FirmwareVersion</span></span>
<span data-ttu-id="383c6-122">A VPN-eszköz belső vezérlőprogram-verziója.</span><span class="sxs-lookup"><span data-stu-id="383c6-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="383c6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="383c6-123">-Name</span></span>
<span data-ttu-id="383c6-124">Annak a kapcsolatnak az erőforrásneve, amelyhez létre kell hozatni a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="383c6-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="383c6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="383c6-125">-ResourceGroupName</span></span>
<span data-ttu-id="383c6-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="383c6-126">The resource group name.</span></span>

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

### <span data-ttu-id="383c6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="383c6-127">-Confirm</span></span>
<span data-ttu-id="383c6-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="383c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="383c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="383c6-129">-WhatIf</span></span>
<span data-ttu-id="383c6-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="383c6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="383c6-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="383c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="383c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383c6-132">CommonParameters</span></span>
<span data-ttu-id="383c6-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="383c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383c6-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="383c6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383c6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="383c6-135">INPUTS</span></span>

### <span data-ttu-id="383c6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="383c6-136">System.String</span></span>

## <span data-ttu-id="383c6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="383c6-137">OUTPUTS</span></span>

### <span data-ttu-id="383c6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="383c6-138">System.String</span></span>

## <span data-ttu-id="383c6-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="383c6-139">NOTES</span></span>

## <span data-ttu-id="383c6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="383c6-140">RELATED LINKS</span></span>
