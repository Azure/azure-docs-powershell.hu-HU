---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468838"
---
# <span data-ttu-id="ccb8c-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ccb8c-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="ccb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb8c-103">Alaphelyzetbe állítja a méretezhető VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="ccb8c-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="ccb8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ccb8c-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccb8c-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccb8c-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb8c-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ccb8c-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb8c-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ccb8c-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb8c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ccb8c-108">DESCRIPTION</span></span>
<span data-ttu-id="ccb8c-109">A VpnGateway alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="ccb8c-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="ccb8c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ccb8c-110">EXAMPLES</span></span>

### <span data-ttu-id="ccb8c-111">1. példa:</span><span class="sxs-lookup"><span data-stu-id="ccb8c-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="ccb8c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccb8c-112">PARAMETERS</span></span>

### <span data-ttu-id="ccb8c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccb8c-113">-AsJob</span></span>
<span data-ttu-id="ccb8c-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ccb8c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccb8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb8c-115">-DefaultProfile</span></span>
<span data-ttu-id="ccb8c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccb8c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccb8c-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="ccb8c-117">-VpnGateway</span></span>
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

### <span data-ttu-id="ccb8c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb8c-118">CommonParameters</span></span>
<span data-ttu-id="ccb8c-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccb8c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb8c-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb8c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb8c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccb8c-121">INPUTS</span></span>

### <span data-ttu-id="ccb8c-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ccb8c-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ccb8c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ccb8c-123">System.String</span></span>

## <span data-ttu-id="ccb8c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccb8c-124">OUTPUTS</span></span>

### <span data-ttu-id="ccb8c-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ccb8c-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="ccb8c-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ccb8c-126">NOTES</span></span>

## <span data-ttu-id="ccb8c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccb8c-127">RELATED LINKS</span></span>

[<span data-ttu-id="ccb8c-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ccb8c-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="ccb8c-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ccb8c-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="ccb8c-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ccb8c-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="ccb8c-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ccb8c-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
