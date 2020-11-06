---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500164"
---
# <span data-ttu-id="b6e4e-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b6e4e-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="b6e4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e4e-103">Módosítja egy ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6e4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6e4e-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6e4e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6e4e-105">DESCRIPTION</span></span>
<span data-ttu-id="b6e4e-106">A **set-AzureRmExpressRoutePort** parancsmag a módosított ExpressRoutePort az Azure-ra menti.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="b6e4e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6e4e-107">EXAMPLES</span></span>

### <span data-ttu-id="b6e4e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6e4e-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="b6e4e-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="b6e4e-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="b6e4e-110">Egy ExpressRoutePort hivatkozásának rendszergazdai állapotát módosítja</span><span class="sxs-lookup"><span data-stu-id="b6e4e-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="b6e4e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6e4e-111">PARAMETERS</span></span>

### <span data-ttu-id="b6e4e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6e4e-112">-AsJob</span></span>
<span data-ttu-id="b6e4e-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b6e4e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6e4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e4e-114">-DefaultProfile</span></span>
<span data-ttu-id="b6e4e-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e4e-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b6e4e-116">-ExpressRoutePort</span></span>
<span data-ttu-id="b6e4e-117">A ExpressRoutePort objektum.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-117">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e4e-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6e4e-118">-Confirm</span></span>
<span data-ttu-id="b6e4e-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6e4e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e4e-120">-WhatIf</span></span>
<span data-ttu-id="b6e4e-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6e4e-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6e4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e4e-123">CommonParameters</span></span>
<span data-ttu-id="b6e4e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6e4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e4e-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6e4e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e4e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e4e-126">INPUTS</span></span>

### <span data-ttu-id="b6e4e-127">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b6e4e-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b6e4e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e4e-128">OUTPUTS</span></span>

### <span data-ttu-id="b6e4e-129">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b6e4e-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b6e4e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6e4e-130">NOTES</span></span>

## <span data-ttu-id="b6e4e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6e4e-131">RELATED LINKS</span></span>
