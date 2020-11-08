---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012486"
---
# <span data-ttu-id="6703c-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6703c-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="6703c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6703c-102">SYNOPSIS</span></span>
<span data-ttu-id="6703c-103">Egy hálózati kapcsolat koppintási konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="6703c-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="6703c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6703c-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6703c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6703c-105">DESCRIPTION</span></span>
<span data-ttu-id="6703c-106">A **set-AzNetworkInterfaceTapConfig** frissíti a hálózati felület koppintásos konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6703c-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="6703c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6703c-107">EXAMPLES</span></span>

### <span data-ttu-id="6703c-108">1. példa: a TapConfiguration beállítása frissített TapConfig névvel</span><span class="sxs-lookup"><span data-stu-id="6703c-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="6703c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6703c-109">PARAMETERS</span></span>

### <span data-ttu-id="6703c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6703c-110">-AsJob</span></span>
<span data-ttu-id="6703c-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6703c-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6703c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6703c-112">-DefaultProfile</span></span>
<span data-ttu-id="6703c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6703c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6703c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6703c-114">-Force</span></span>
<span data-ttu-id="6703c-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6703c-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6703c-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6703c-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="6703c-117">A NetworkInterface koppintson a konfiguráció elemre</span><span class="sxs-lookup"><span data-stu-id="6703c-117">The NetworkInterface Tap configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6703c-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6703c-118">-Confirm</span></span>
<span data-ttu-id="6703c-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6703c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6703c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6703c-120">-WhatIf</span></span>
<span data-ttu-id="6703c-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6703c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6703c-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6703c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6703c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6703c-123">CommonParameters</span></span>
<span data-ttu-id="6703c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6703c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6703c-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6703c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6703c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6703c-126">INPUTS</span></span>

### <span data-ttu-id="6703c-127">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="6703c-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="6703c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6703c-128">OUTPUTS</span></span>

### <span data-ttu-id="6703c-129">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6703c-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6703c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6703c-130">NOTES</span></span>

## <span data-ttu-id="6703c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6703c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6703c-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6703c-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="6703c-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6703c-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="6703c-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6703c-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
