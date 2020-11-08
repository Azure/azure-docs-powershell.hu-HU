---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011665"
---
# <span data-ttu-id="9dae0-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="9dae0-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="9dae0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dae0-102">SYNOPSIS</span></span>
<span data-ttu-id="9dae0-103">Ez a parancsmagot a támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="9dae0-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="9dae0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dae0-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dae0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dae0-105">DESCRIPTION</span></span>
<span data-ttu-id="9dae0-106">Ez a parancsmagot a támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="9dae0-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="9dae0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9dae0-107">EXAMPLES</span></span>

### <span data-ttu-id="9dae0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9dae0-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="9dae0-109">A támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="9dae0-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="9dae0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dae0-110">PARAMETERS</span></span>

### <span data-ttu-id="9dae0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dae0-111">-DefaultProfile</span></span>
<span data-ttu-id="9dae0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dae0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dae0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9dae0-113">-Name</span></span>
<span data-ttu-id="9dae0-114">A virtuális hálózat átjárójának neve.</span><span class="sxs-lookup"><span data-stu-id="9dae0-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="9dae0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dae0-115">-ResourceGroupName</span></span>
<span data-ttu-id="9dae0-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9dae0-116">The resource group name.</span></span>

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

### <span data-ttu-id="9dae0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dae0-117">CommonParameters</span></span>
<span data-ttu-id="9dae0-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dae0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dae0-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9dae0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dae0-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dae0-120">INPUTS</span></span>

### <span data-ttu-id="9dae0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9dae0-121">System.String</span></span>

## <span data-ttu-id="9dae0-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dae0-122">OUTPUTS</span></span>

### <span data-ttu-id="9dae0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9dae0-123">System.String</span></span>

## <span data-ttu-id="9dae0-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dae0-124">NOTES</span></span>

## <span data-ttu-id="9dae0-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dae0-125">RELATED LINKS</span></span>
