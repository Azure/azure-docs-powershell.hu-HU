---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491894"
---
# <span data-ttu-id="59275-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="59275-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="59275-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59275-102">SYNOPSIS</span></span>
<span data-ttu-id="59275-103">A TAP-konfiguráció cél állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="59275-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59275-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59275-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59275-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59275-105">DESCRIPTION</span></span>
<span data-ttu-id="59275-106">A **set-AzureRmNetworkInterfaceTapConfig** az Azure-hálózati kapcsolat céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="59275-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="59275-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59275-107">EXAMPLES</span></span>

### <span data-ttu-id="59275-108">1. példa: a TapConfiguration beállítása frissített TapConfig névvel</span><span class="sxs-lookup"><span data-stu-id="59275-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="59275-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59275-109">PARAMETERS</span></span>

### <span data-ttu-id="59275-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59275-110">-AsJob</span></span>
<span data-ttu-id="59275-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="59275-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59275-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59275-112">-DefaultProfile</span></span>
<span data-ttu-id="59275-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59275-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59275-114">-Force</span><span class="sxs-lookup"><span data-stu-id="59275-114">-Force</span></span>
<span data-ttu-id="59275-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59275-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59275-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="59275-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="59275-117">A NetworkInterface koppintson a configurtion</span><span class="sxs-lookup"><span data-stu-id="59275-117">The NetworkInterface Tap configurtion</span></span>

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

### <span data-ttu-id="59275-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59275-118">-Confirm</span></span>
<span data-ttu-id="59275-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59275-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59275-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59275-120">-WhatIf</span></span>
<span data-ttu-id="59275-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59275-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59275-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59275-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59275-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59275-123">CommonParameters</span></span>
<span data-ttu-id="59275-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59275-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59275-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59275-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59275-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59275-126">INPUTS</span></span>

### <span data-ttu-id="59275-127">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="59275-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="59275-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59275-128">OUTPUTS</span></span>

### <span data-ttu-id="59275-129">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="59275-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="59275-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59275-130">NOTES</span></span>

## <span data-ttu-id="59275-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59275-131">RELATED LINKS</span></span>
