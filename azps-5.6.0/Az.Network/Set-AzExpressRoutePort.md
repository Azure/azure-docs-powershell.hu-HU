---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: c431b03c4dd417638f84fe3a483bcaf9eefcb837
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924602"
---
# <span data-ttu-id="a2ed0-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2ed0-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="a2ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ed0-103">Módosítja az ExpressRoutePortot.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="a2ed0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2ed0-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2ed0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2ed0-105">DESCRIPTION</span></span>
<span data-ttu-id="a2ed0-106">A **Set-AzExpressRoutePort** parancsmag menti a módosított ExpressRoutePortot az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="a2ed0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2ed0-107">EXAMPLES</span></span>

### <span data-ttu-id="a2ed0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a2ed0-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="a2ed0-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2ed0-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="a2ed0-110">Módosítja egy ExpressRoutePort-hivatkozás rendszergazdai állapotát</span><span class="sxs-lookup"><span data-stu-id="a2ed0-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="a2ed0-111">3. példa</span><span class="sxs-lookup"><span data-stu-id="a2ed0-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="a2ed0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2ed0-112">PARAMETERS</span></span>

### <span data-ttu-id="a2ed0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2ed0-113">-AsJob</span></span>
<span data-ttu-id="a2ed0-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a2ed0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2ed0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ed0-115">-DefaultProfile</span></span>
<span data-ttu-id="a2ed0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2ed0-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2ed0-117">-ExpressRoutePort</span></span>
<span data-ttu-id="a2ed0-118">Az ExpressRoutePort objektum.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-118">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="a2ed0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2ed0-119">-Confirm</span></span>
<span data-ttu-id="a2ed0-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2ed0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ed0-121">-WhatIf</span></span>
<span data-ttu-id="a2ed0-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2ed0-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2ed0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ed0-124">CommonParameters</span></span>
<span data-ttu-id="a2ed0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ed0-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ed0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ed0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2ed0-127">INPUTS</span></span>

### <span data-ttu-id="a2ed0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2ed0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a2ed0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2ed0-129">OUTPUTS</span></span>

### <span data-ttu-id="a2ed0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2ed0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a2ed0-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2ed0-131">NOTES</span></span>

## <span data-ttu-id="a2ed0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2ed0-132">RELATED LINKS</span></span>

[<span data-ttu-id="a2ed0-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2ed0-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="a2ed0-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2ed0-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="a2ed0-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2ed0-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
