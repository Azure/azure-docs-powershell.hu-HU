---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185953"
---
# <span data-ttu-id="fcc3b-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcc3b-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="fcc3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcc3b-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc3b-103">Visszaállítja a skálázható VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="fcc3b-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="fcc3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcc3b-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcc3b-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fcc3b-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcc3b-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="fcc3b-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcc3b-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="fcc3b-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcc3b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcc3b-108">DESCRIPTION</span></span>
<span data-ttu-id="fcc3b-109">A VpnGateway alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="fcc3b-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="fcc3b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fcc3b-110">EXAMPLES</span></span>

### <span data-ttu-id="fcc3b-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="fcc3b-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="fcc3b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcc3b-112">PARAMETERS</span></span>

### <span data-ttu-id="fcc3b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcc3b-113">-AsJob</span></span>
<span data-ttu-id="fcc3b-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fcc3b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fcc3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc3b-115">-DefaultProfile</span></span>
<span data-ttu-id="fcc3b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcc3b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcc3b-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcc3b-117">-VpnGateway</span></span>
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

### <span data-ttu-id="fcc3b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc3b-118">CommonParameters</span></span>
<span data-ttu-id="fcc3b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcc3b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc3b-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc3b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc3b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcc3b-121">INPUTS</span></span>

### <span data-ttu-id="fcc3b-122">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcc3b-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="fcc3b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fcc3b-123">System.String</span></span>

## <span data-ttu-id="fcc3b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcc3b-124">OUTPUTS</span></span>

### <span data-ttu-id="fcc3b-125">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcc3b-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="fcc3b-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcc3b-126">NOTES</span></span>

## <span data-ttu-id="fcc3b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcc3b-127">RELATED LINKS</span></span>

[<span data-ttu-id="fcc3b-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcc3b-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="fcc3b-129">Új – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcc3b-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="fcc3b-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcc3b-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="fcc3b-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcc3b-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
