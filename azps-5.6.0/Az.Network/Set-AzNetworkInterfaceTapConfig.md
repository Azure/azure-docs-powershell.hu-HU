---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: a542b69b1f028a7fdfd3e02d02f95735bc4add9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003349"
---
# <span data-ttu-id="22d8d-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="22d8d-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="22d8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="22d8d-103">Egy hálózati felület koppintási konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="22d8d-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="22d8d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22d8d-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d8d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="22d8d-106">A **Set-AzNetworkInterfaceTapConfig** egy hálózati felület koppintási konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="22d8d-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="22d8d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="22d8d-108">1. példa: A TapConfiguration beállítása frissített TapConfig névvel</span><span class="sxs-lookup"><span data-stu-id="22d8d-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="22d8d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22d8d-109">PARAMETERS</span></span>

### <span data-ttu-id="22d8d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22d8d-110">-AsJob</span></span>
<span data-ttu-id="22d8d-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="22d8d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22d8d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d8d-112">-DefaultProfile</span></span>
<span data-ttu-id="22d8d-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22d8d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d8d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="22d8d-114">-Force</span></span>
<span data-ttu-id="22d8d-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22d8d-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="22d8d-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="22d8d-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="22d8d-117">The NetworkInterface Tap configuration</span><span class="sxs-lookup"><span data-stu-id="22d8d-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="22d8d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22d8d-118">-Confirm</span></span>
<span data-ttu-id="22d8d-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22d8d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d8d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d8d-120">-WhatIf</span></span>
<span data-ttu-id="22d8d-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22d8d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d8d-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22d8d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d8d-123">CommonParameters</span></span>
<span data-ttu-id="22d8d-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d8d-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d8d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d8d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22d8d-126">INPUTS</span></span>

### <span data-ttu-id="22d8d-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="22d8d-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="22d8d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d8d-128">OUTPUTS</span></span>

### <span data-ttu-id="22d8d-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="22d8d-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="22d8d-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22d8d-130">NOTES</span></span>

## <span data-ttu-id="22d8d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22d8d-131">RELATED LINKS</span></span>

[<span data-ttu-id="22d8d-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="22d8d-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="22d8d-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="22d8d-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="22d8d-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="22d8d-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
