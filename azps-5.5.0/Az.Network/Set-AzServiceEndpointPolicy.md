---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151379"
---
# <span data-ttu-id="2c668-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2c668-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="2c668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c668-102">SYNOPSIS</span></span>
<span data-ttu-id="2c668-103">Szolgáltatásvégpont-házirend frissítése.</span><span class="sxs-lookup"><span data-stu-id="2c668-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="2c668-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c668-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c668-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c668-105">DESCRIPTION</span></span>
<span data-ttu-id="2c668-106">A **Set-AzServiceEndpointPolicy** parancsmag szolgáltatási végponti házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2c668-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="2c668-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c668-107">EXAMPLES</span></span>

### <span data-ttu-id="2c668-108">1. példa: Szolgáltatásvégpont-házirendet állít be</span><span class="sxs-lookup"><span data-stu-id="2c668-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="2c668-109">Ez a parancs frissíti az "erőforráscsoport1" erőforráscsoporthoz tartozó objektumobjektum által $serviceEndpointPolicy Házirend1 nevű szolgáltatásvégpont-házirendet.</span><span class="sxs-lookup"><span data-stu-id="2c668-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="2c668-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c668-110">PARAMETERS</span></span>

### <span data-ttu-id="2c668-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c668-111">-DefaultProfile</span></span>
<span data-ttu-id="2c668-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c668-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c668-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2c668-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2c668-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2c668-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c668-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c668-115">-Confirm</span></span>
<span data-ttu-id="2c668-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2c668-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c668-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c668-117">-WhatIf</span></span>
<span data-ttu-id="2c668-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2c668-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c668-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c668-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c668-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c668-120">CommonParameters</span></span>
<span data-ttu-id="2c668-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c668-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c668-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c668-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c668-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c668-123">INPUTS</span></span>

### <span data-ttu-id="2c668-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2c668-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="2c668-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c668-125">OUTPUTS</span></span>

### <span data-ttu-id="2c668-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2c668-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="2c668-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c668-127">NOTES</span></span>

## <span data-ttu-id="2c668-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c668-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c668-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2c668-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="2c668-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2c668-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="2c668-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2c668-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
