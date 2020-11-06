---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f66765d69cb6d9d626322446223aa5f94ff94eac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493436"
---
# <span data-ttu-id="d840a-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="d840a-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="d840a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d840a-102">SYNOPSIS</span></span>
<span data-ttu-id="d840a-103">Ez a parancsmagot a támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d840a-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d840a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d840a-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d840a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d840a-105">DESCRIPTION</span></span>
<span data-ttu-id="d840a-106">Ez a parancsmagot a támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d840a-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="d840a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d840a-107">EXAMPLES</span></span>

### <span data-ttu-id="d840a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d840a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="d840a-109">A támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d840a-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="d840a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d840a-110">PARAMETERS</span></span>

### <span data-ttu-id="d840a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d840a-111">-DefaultProfile</span></span>
<span data-ttu-id="d840a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d840a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d840a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d840a-113">-Name</span></span>
<span data-ttu-id="d840a-114">A virtuális hálózat átjárójának neve.</span><span class="sxs-lookup"><span data-stu-id="d840a-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="d840a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d840a-115">-ResourceGroupName</span></span>
<span data-ttu-id="d840a-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d840a-116">The resource group name.</span></span>

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

### <span data-ttu-id="d840a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d840a-117">CommonParameters</span></span>
<span data-ttu-id="d840a-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d840a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d840a-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d840a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d840a-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d840a-120">INPUTS</span></span>

### <span data-ttu-id="d840a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d840a-121">System.String</span></span>

## <span data-ttu-id="d840a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d840a-122">OUTPUTS</span></span>

### <span data-ttu-id="d840a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d840a-123">System.String</span></span>

## <span data-ttu-id="d840a-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d840a-124">NOTES</span></span>

## <span data-ttu-id="d840a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d840a-125">RELATED LINKS</span></span>

