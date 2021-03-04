---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 33abb4e724f5a442efd6791cbf6256100662ab65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932378"
---
# <span data-ttu-id="fe3f4-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe3f4-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="fe3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3f4-103">Alaphelyzetbe állítja a méretezhető VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="fe3f4-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="fe3f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe3f4-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3f4-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe3f4-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3f4-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="fe3f4-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3f4-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3f4-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe3f4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe3f4-108">DESCRIPTION</span></span>
<span data-ttu-id="fe3f4-109">A VpnGateway alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="fe3f4-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="fe3f4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe3f4-110">EXAMPLES</span></span>

### <span data-ttu-id="fe3f4-111">1. példa:</span><span class="sxs-lookup"><span data-stu-id="fe3f4-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="fe3f4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe3f4-112">PARAMETERS</span></span>

### <span data-ttu-id="fe3f4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe3f4-113">-AsJob</span></span>
<span data-ttu-id="fe3f4-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fe3f4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe3f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3f4-115">-DefaultProfile</span></span>
<span data-ttu-id="fe3f4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe3f4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe3f4-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe3f4-117">-VpnGateway</span></span>
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

### <span data-ttu-id="fe3f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3f4-118">CommonParameters</span></span>
<span data-ttu-id="fe3f4-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3f4-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe3f4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3f4-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe3f4-121">INPUTS</span></span>

### <span data-ttu-id="fe3f4-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe3f4-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="fe3f4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fe3f4-123">System.String</span></span>

## <span data-ttu-id="fe3f4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe3f4-124">OUTPUTS</span></span>

### <span data-ttu-id="fe3f4-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe3f4-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="fe3f4-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe3f4-126">NOTES</span></span>

## <span data-ttu-id="fe3f4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe3f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="fe3f4-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe3f4-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="fe3f4-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe3f4-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="fe3f4-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe3f4-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="fe3f4-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe3f4-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
