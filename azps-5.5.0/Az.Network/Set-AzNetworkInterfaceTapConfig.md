---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156683"
---
# <span data-ttu-id="7015c-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7015c-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="7015c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7015c-102">SYNOPSIS</span></span>
<span data-ttu-id="7015c-103">Egy hálózati felület koppintási konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="7015c-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="7015c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7015c-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7015c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7015c-105">DESCRIPTION</span></span>
<span data-ttu-id="7015c-106">A **Set-AzNetworkInterfaceTapConfig** egy hálózati felület koppintási konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="7015c-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="7015c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7015c-107">EXAMPLES</span></span>

### <span data-ttu-id="7015c-108">1. példa: A TapConfiguration beállítása frissített TapConfig névvel</span><span class="sxs-lookup"><span data-stu-id="7015c-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="7015c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7015c-109">PARAMETERS</span></span>

### <span data-ttu-id="7015c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7015c-110">-AsJob</span></span>
<span data-ttu-id="7015c-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7015c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7015c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7015c-112">-DefaultProfile</span></span>
<span data-ttu-id="7015c-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7015c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7015c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7015c-114">-Force</span></span>
<span data-ttu-id="7015c-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7015c-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7015c-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7015c-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="7015c-117">The NetworkInterface Tap configuration</span><span class="sxs-lookup"><span data-stu-id="7015c-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="7015c-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7015c-118">-Confirm</span></span>
<span data-ttu-id="7015c-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7015c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7015c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7015c-120">-WhatIf</span></span>
<span data-ttu-id="7015c-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7015c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7015c-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7015c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7015c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7015c-123">CommonParameters</span></span>
<span data-ttu-id="7015c-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7015c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7015c-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7015c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7015c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7015c-126">INPUTS</span></span>

### <span data-ttu-id="7015c-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="7015c-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="7015c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7015c-128">OUTPUTS</span></span>

### <span data-ttu-id="7015c-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7015c-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7015c-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7015c-130">NOTES</span></span>

## <span data-ttu-id="7015c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7015c-131">RELATED LINKS</span></span>

[<span data-ttu-id="7015c-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7015c-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="7015c-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7015c-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="7015c-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7015c-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
