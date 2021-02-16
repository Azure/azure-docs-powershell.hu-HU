---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: cdea7cba3dea72df80b8571198bb50d5e337b14e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146626"
---
# <span data-ttu-id="8fff3-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8fff3-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="8fff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fff3-102">SYNOPSIS</span></span>
<span data-ttu-id="8fff3-103">Alaphelyzetbe állítja a méretezhető P2S VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="8fff3-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="8fff3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8fff3-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fff3-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fff3-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fff3-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8fff3-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fff3-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8fff3-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fff3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8fff3-108">DESCRIPTION</span></span>
<span data-ttu-id="8fff3-109">A P2SVpnGateway alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="8fff3-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="8fff3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8fff3-110">EXAMPLES</span></span>

### <span data-ttu-id="8fff3-111">1. példa:</span><span class="sxs-lookup"><span data-stu-id="8fff3-111">Example 1:</span></span>
```
$Gateway = Get-AzP2SVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="8fff3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fff3-112">PARAMETERS</span></span>

### <span data-ttu-id="8fff3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fff3-113">-AsJob</span></span>
<span data-ttu-id="8fff3-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8fff3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fff3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fff3-115">-DefaultProfile</span></span>
<span data-ttu-id="8fff3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fff3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fff3-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8fff3-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="8fff3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fff3-118">CommonParameters</span></span>
<span data-ttu-id="8fff3-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fff3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fff3-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fff3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fff3-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fff3-121">INPUTS</span></span>

### <span data-ttu-id="8fff3-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8fff3-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="8fff3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8fff3-123">System.String</span></span>

## <span data-ttu-id="8fff3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fff3-124">OUTPUTS</span></span>

### <span data-ttu-id="8fff3-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8fff3-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="8fff3-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8fff3-126">NOTES</span></span>

## <span data-ttu-id="8fff3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fff3-127">RELATED LINKS</span></span>

[<span data-ttu-id="8fff3-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8fff3-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="8fff3-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8fff3-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="8fff3-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8fff3-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="8fff3-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8fff3-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
