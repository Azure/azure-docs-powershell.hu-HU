---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172894"
---
# <span data-ttu-id="87380-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87380-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="87380-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87380-102">SYNOPSIS</span></span>
<span data-ttu-id="87380-103">Visszaállítja a skálázható VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="87380-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="87380-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87380-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87380-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87380-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87380-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="87380-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87380-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="87380-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87380-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="87380-108">DESCRIPTION</span></span>
<span data-ttu-id="87380-109">A VpnGateway alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="87380-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="87380-110">Példák</span><span class="sxs-lookup"><span data-stu-id="87380-110">EXAMPLES</span></span>

### <span data-ttu-id="87380-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="87380-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="87380-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87380-112">PARAMETERS</span></span>

### <span data-ttu-id="87380-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87380-113">-AsJob</span></span>
<span data-ttu-id="87380-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="87380-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87380-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87380-115">-DefaultProfile</span></span>
<span data-ttu-id="87380-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87380-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87380-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="87380-117">-VpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87380-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87380-118">CommonParameters</span></span>
<span data-ttu-id="87380-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87380-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87380-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87380-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87380-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87380-121">INPUTS</span></span>

### <span data-ttu-id="87380-122">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87380-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="87380-123">System. String</span><span class="sxs-lookup"><span data-stu-id="87380-123">System.String</span></span>

## <span data-ttu-id="87380-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87380-124">OUTPUTS</span></span>

### <span data-ttu-id="87380-125">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87380-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="87380-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87380-126">NOTES</span></span>

## <span data-ttu-id="87380-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87380-127">RELATED LINKS</span></span>

[<span data-ttu-id="87380-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87380-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="87380-129">Új – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87380-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="87380-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87380-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="87380-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87380-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
