---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: fe1182f165e347b312288d56604fddad6bad68da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837026"
---
# <span data-ttu-id="7fb5b-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7fb5b-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="7fb5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7fb5b-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb5b-103">Módosítja egy ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="7fb5b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7fb5b-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb5b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7fb5b-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb5b-106">A **set-AzExpressRoutePort** parancsmag a módosított ExpressRoutePort az Azure-ra menti.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="7fb5b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7fb5b-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb5b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7fb5b-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="7fb5b-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="7fb5b-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="7fb5b-110">Egy ExpressRoutePort hivatkozásának rendszergazdai állapotát módosítja</span><span class="sxs-lookup"><span data-stu-id="7fb5b-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="7fb5b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7fb5b-111">PARAMETERS</span></span>

### <span data-ttu-id="7fb5b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fb5b-112">-AsJob</span></span>
<span data-ttu-id="7fb5b-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7fb5b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fb5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb5b-114">-DefaultProfile</span></span>
<span data-ttu-id="7fb5b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb5b-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7fb5b-116">-ExpressRoutePort</span></span>
<span data-ttu-id="7fb5b-117">A ExpressRoutePort objektum.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="7fb5b-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7fb5b-118">-Confirm</span></span>
<span data-ttu-id="7fb5b-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb5b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb5b-120">-WhatIf</span></span>
<span data-ttu-id="7fb5b-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb5b-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7fb5b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb5b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb5b-123">CommonParameters</span></span>
<span data-ttu-id="7fb5b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7fb5b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb5b-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb5b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb5b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fb5b-126">INPUTS</span></span>

### <span data-ttu-id="7fb5b-127">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7fb5b-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7fb5b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fb5b-128">OUTPUTS</span></span>

### <span data-ttu-id="7fb5b-129">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7fb5b-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7fb5b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7fb5b-130">NOTES</span></span>

## <span data-ttu-id="7fb5b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fb5b-131">RELATED LINKS</span></span>

[<span data-ttu-id="7fb5b-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7fb5b-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="7fb5b-133">Új – AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7fb5b-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="7fb5b-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7fb5b-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
