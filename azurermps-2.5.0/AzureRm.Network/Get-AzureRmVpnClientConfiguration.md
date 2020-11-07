---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: 4d6e95534cdadd694fa2ed87d43d3f7387ec9b20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848770"
---
# <span data-ttu-id="6a594-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a594-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="6a594-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a594-102">SYNOPSIS</span></span>
<span data-ttu-id="6a594-103">Lehetővé teszi a felhasználóknak, hogy egyszerűen töltse le a New-AzureRmVpnClientConfiguration parancsmagot létrehozott VPN-profil csomagot.</span><span class="sxs-lookup"><span data-stu-id="6a594-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a594-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a594-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a594-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a594-105">DESCRIPTION</span></span>
<span data-ttu-id="6a594-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="6a594-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="6a594-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a594-107">EXAMPLES</span></span>

### <span data-ttu-id="6a594-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a594-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="6a594-109">Az URL-cím megadásával letöltheti azt a VpnClient-profilt, amelyet korábban a New-AzureRMVpnClientConfiguration parancs segítségével generált.</span><span class="sxs-lookup"><span data-stu-id="6a594-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="6a594-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a594-110">PARAMETERS</span></span>

### <span data-ttu-id="6a594-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a594-111">-DefaultProfile</span></span>
<span data-ttu-id="6a594-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a594-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="6a594-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a594-113">-Name</span></span>
<span data-ttu-id="6a594-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6a594-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a594-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a594-115">-ResourceGroupName</span></span>
<span data-ttu-id="6a594-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6a594-116">The resource group name.</span></span>

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

### <span data-ttu-id="6a594-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a594-117">-Confirm</span></span>
<span data-ttu-id="6a594-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a594-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a594-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a594-119">-WhatIf</span></span>
<span data-ttu-id="6a594-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a594-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a594-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a594-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a594-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a594-122">CommonParameters</span></span>
<span data-ttu-id="6a594-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a594-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a594-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a594-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a594-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a594-125">INPUTS</span></span>

### <span data-ttu-id="6a594-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6a594-126">System.String</span></span>

## <span data-ttu-id="6a594-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a594-127">OUTPUTS</span></span>

### <span data-ttu-id="6a594-128">Microsoft. Azure. commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="6a594-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="6a594-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a594-129">NOTES</span></span>

## <span data-ttu-id="6a594-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a594-130">RELATED LINKS</span></span>

