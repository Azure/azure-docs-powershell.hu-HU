---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467308"
---
# <span data-ttu-id="44347-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44347-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="44347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44347-102">SYNOPSIS</span></span>
<span data-ttu-id="44347-103">Módosítja az ExpressRoutePortot.</span><span class="sxs-lookup"><span data-stu-id="44347-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="44347-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44347-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44347-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44347-105">DESCRIPTION</span></span>
<span data-ttu-id="44347-106">A **Set-AzExpressRoutePort** parancsmag menti a módosított ExpressRoutePortot az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="44347-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="44347-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44347-107">EXAMPLES</span></span>

### <span data-ttu-id="44347-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="44347-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="44347-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="44347-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="44347-110">Módosítja egy ExpressRoutePort-hivatkozás rendszergazdai állapotát</span><span class="sxs-lookup"><span data-stu-id="44347-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="44347-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44347-111">PARAMETERS</span></span>

### <span data-ttu-id="44347-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44347-112">-AsJob</span></span>
<span data-ttu-id="44347-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="44347-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44347-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44347-114">-DefaultProfile</span></span>
<span data-ttu-id="44347-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44347-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44347-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44347-116">-ExpressRoutePort</span></span>
<span data-ttu-id="44347-117">Az ExpressRoutePort objektum.</span><span class="sxs-lookup"><span data-stu-id="44347-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="44347-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44347-118">-Confirm</span></span>
<span data-ttu-id="44347-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44347-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44347-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44347-120">-WhatIf</span></span>
<span data-ttu-id="44347-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44347-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44347-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44347-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44347-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44347-123">CommonParameters</span></span>
<span data-ttu-id="44347-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44347-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44347-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44347-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44347-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44347-126">INPUTS</span></span>

### <span data-ttu-id="44347-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44347-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="44347-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44347-128">OUTPUTS</span></span>

### <span data-ttu-id="44347-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44347-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="44347-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44347-130">NOTES</span></span>

## <span data-ttu-id="44347-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44347-131">RELATED LINKS</span></span>

[<span data-ttu-id="44347-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44347-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="44347-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44347-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="44347-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44347-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
