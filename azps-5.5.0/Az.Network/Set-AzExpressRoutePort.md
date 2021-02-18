---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: 2365729f3960e3652e2b4c0709ca14092fea3264
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206518"
---
# <span data-ttu-id="445f0-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="445f0-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="445f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="445f0-102">SYNOPSIS</span></span>
<span data-ttu-id="445f0-103">Módosítja az ExpressRoutePortot.</span><span class="sxs-lookup"><span data-stu-id="445f0-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="445f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="445f0-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="445f0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="445f0-105">DESCRIPTION</span></span>
<span data-ttu-id="445f0-106">A **Set-AzExpressRoutePort** parancsmag menti a módosított ExpressRoutePortot az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="445f0-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="445f0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="445f0-107">EXAMPLES</span></span>

### <span data-ttu-id="445f0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="445f0-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="445f0-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="445f0-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="445f0-110">Módosítja egy ExpressRoutePort-hivatkozás rendszergazdai állapotát</span><span class="sxs-lookup"><span data-stu-id="445f0-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="445f0-111">3. példa</span><span class="sxs-lookup"><span data-stu-id="445f0-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="445f0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="445f0-112">PARAMETERS</span></span>

### <span data-ttu-id="445f0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="445f0-113">-AsJob</span></span>
<span data-ttu-id="445f0-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="445f0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="445f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445f0-115">-DefaultProfile</span></span>
<span data-ttu-id="445f0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="445f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="445f0-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="445f0-117">-ExpressRoutePort</span></span>
<span data-ttu-id="445f0-118">Az ExpressRoutePort objektum.</span><span class="sxs-lookup"><span data-stu-id="445f0-118">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="445f0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="445f0-119">-Confirm</span></span>
<span data-ttu-id="445f0-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="445f0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="445f0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445f0-121">-WhatIf</span></span>
<span data-ttu-id="445f0-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="445f0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445f0-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="445f0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="445f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445f0-124">CommonParameters</span></span>
<span data-ttu-id="445f0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="445f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445f0-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="445f0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445f0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="445f0-127">INPUTS</span></span>

### <span data-ttu-id="445f0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="445f0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="445f0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="445f0-129">OUTPUTS</span></span>

### <span data-ttu-id="445f0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="445f0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="445f0-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="445f0-131">NOTES</span></span>

## <span data-ttu-id="445f0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="445f0-132">RELATED LINKS</span></span>

[<span data-ttu-id="445f0-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="445f0-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="445f0-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="445f0-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="445f0-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="445f0-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
