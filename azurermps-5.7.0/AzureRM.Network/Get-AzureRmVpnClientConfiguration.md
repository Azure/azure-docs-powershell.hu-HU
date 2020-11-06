---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 09c3862513b893003908b07992ae479656ba7ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505448"
---
# <span data-ttu-id="732e1-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="732e1-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="732e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="732e1-102">SYNOPSIS</span></span>
<span data-ttu-id="732e1-103">Lehetővé teszi a felhasználóknak, hogy egyszerűen töltse le a New-AzureRmVpnClientConfiguration parancsmagot létrehozott VPN-profil csomagot.</span><span class="sxs-lookup"><span data-stu-id="732e1-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="732e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="732e1-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="732e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="732e1-105">DESCRIPTION</span></span>
<span data-ttu-id="732e1-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="732e1-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="732e1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="732e1-107">EXAMPLES</span></span>

### <span data-ttu-id="732e1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="732e1-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="732e1-109">Az URL-cím megadásával letöltheti azt a VpnClient-profilt, amelyet korábban a New-AzureRMVpnClientConfiguration parancs segítségével generált.</span><span class="sxs-lookup"><span data-stu-id="732e1-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="732e1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="732e1-110">PARAMETERS</span></span>

### <span data-ttu-id="732e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732e1-111">-DefaultProfile</span></span>
<span data-ttu-id="732e1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="732e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="732e1-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="732e1-113">-Name</span></span>
<span data-ttu-id="732e1-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="732e1-114">The resource name.</span></span>

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

### <span data-ttu-id="732e1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732e1-115">-ResourceGroupName</span></span>
<span data-ttu-id="732e1-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="732e1-116">The resource group name.</span></span>

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

### <span data-ttu-id="732e1-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="732e1-117">-Confirm</span></span>
<span data-ttu-id="732e1-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="732e1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="732e1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="732e1-119">-WhatIf</span></span>
<span data-ttu-id="732e1-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="732e1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="732e1-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="732e1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="732e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732e1-122">CommonParameters</span></span>
<span data-ttu-id="732e1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="732e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732e1-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="732e1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732e1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="732e1-125">INPUTS</span></span>

### <span data-ttu-id="732e1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="732e1-126">System.String</span></span>

## <span data-ttu-id="732e1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="732e1-127">OUTPUTS</span></span>

### <span data-ttu-id="732e1-128">Microsoft. Azure. commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="732e1-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="732e1-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="732e1-129">NOTES</span></span>

## <span data-ttu-id="732e1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="732e1-130">RELATED LINKS</span></span>

