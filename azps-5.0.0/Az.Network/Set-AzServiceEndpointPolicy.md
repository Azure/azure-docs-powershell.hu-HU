---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187585"
---
# <span data-ttu-id="21399-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="21399-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="21399-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21399-102">SYNOPSIS</span></span>
<span data-ttu-id="21399-103">A szolgáltatás végpont-házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="21399-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="21399-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21399-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21399-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="21399-105">DESCRIPTION</span></span>
<span data-ttu-id="21399-106">A **set-AzServiceEndpointPolicy** parancsmag szolgáltatás-végponti házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="21399-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="21399-107">Példák</span><span class="sxs-lookup"><span data-stu-id="21399-107">EXAMPLES</span></span>

### <span data-ttu-id="21399-108">1. példa: szolgáltatási végpontokra vonatkozó házirendet állít be</span><span class="sxs-lookup"><span data-stu-id="21399-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="21399-109">Ez a parancs frissíti az objektum által meghatározott Házirend1 nevű szolgáltatási végpont-házirendet, $serviceEndpointPolicy a "resourcegroup1" resourcegroup tartozik.</span><span class="sxs-lookup"><span data-stu-id="21399-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="21399-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21399-110">PARAMETERS</span></span>

### <span data-ttu-id="21399-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21399-111">-DefaultProfile</span></span>
<span data-ttu-id="21399-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21399-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21399-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="21399-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="21399-114">A ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="21399-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="21399-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21399-115">-Confirm</span></span>
<span data-ttu-id="21399-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21399-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21399-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21399-117">-WhatIf</span></span>
<span data-ttu-id="21399-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21399-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21399-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21399-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21399-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21399-120">CommonParameters</span></span>
<span data-ttu-id="21399-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21399-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21399-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21399-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21399-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21399-123">INPUTS</span></span>

### <span data-ttu-id="21399-124">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="21399-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="21399-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21399-125">OUTPUTS</span></span>

### <span data-ttu-id="21399-126">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="21399-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="21399-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21399-127">NOTES</span></span>

## <span data-ttu-id="21399-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21399-128">RELATED LINKS</span></span>

[<span data-ttu-id="21399-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="21399-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="21399-130">Új – AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="21399-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="21399-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="21399-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)