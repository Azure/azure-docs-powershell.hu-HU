---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 7b57892316402eab20a14a2761141235a086badb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837009"
---
# <span data-ttu-id="da162-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="da162-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="da162-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da162-102">SYNOPSIS</span></span>
<span data-ttu-id="da162-103">Egy hálózati kapcsolat koppintási konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="da162-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="da162-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da162-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da162-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da162-105">DESCRIPTION</span></span>
<span data-ttu-id="da162-106">A **set-AzNetworkInterfaceTapConfig** frissíti a hálózati felület koppintásos konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="da162-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="da162-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da162-107">EXAMPLES</span></span>

### <span data-ttu-id="da162-108">1. példa: a TapConfiguration beállítása frissített TapConfig névvel</span><span class="sxs-lookup"><span data-stu-id="da162-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="da162-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da162-109">PARAMETERS</span></span>

### <span data-ttu-id="da162-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da162-110">-AsJob</span></span>
<span data-ttu-id="da162-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da162-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da162-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da162-112">-DefaultProfile</span></span>
<span data-ttu-id="da162-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da162-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da162-114">-Force</span><span class="sxs-lookup"><span data-stu-id="da162-114">-Force</span></span>
<span data-ttu-id="da162-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da162-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="da162-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="da162-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="da162-117">A NetworkInterface koppintson a konfiguráció elemre</span><span class="sxs-lookup"><span data-stu-id="da162-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="da162-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da162-118">-Confirm</span></span>
<span data-ttu-id="da162-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da162-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da162-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da162-120">-WhatIf</span></span>
<span data-ttu-id="da162-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da162-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da162-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da162-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da162-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da162-123">CommonParameters</span></span>
<span data-ttu-id="da162-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da162-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da162-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da162-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da162-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da162-126">INPUTS</span></span>

### <span data-ttu-id="da162-127">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="da162-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="da162-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da162-128">OUTPUTS</span></span>

### <span data-ttu-id="da162-129">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="da162-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="da162-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da162-130">NOTES</span></span>

## <span data-ttu-id="da162-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da162-131">RELATED LINKS</span></span>

[<span data-ttu-id="da162-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="da162-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="da162-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="da162-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="da162-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="da162-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
