---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302558"
---
# <span data-ttu-id="f6776-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="f6776-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="f6776-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6776-102">SYNOPSIS</span></span>
<span data-ttu-id="f6776-103">Eltávolítja a WcfRelay a megadott továbbítási névtérből.</span><span class="sxs-lookup"><span data-stu-id="f6776-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="f6776-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6776-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6776-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6776-105">DESCRIPTION</span></span>
<span data-ttu-id="f6776-106">A **Remove-AzWcfRelay** parancsmag eltávolítja a WcfRelay a megadott továbbító névtérből.</span><span class="sxs-lookup"><span data-stu-id="f6776-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="f6776-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6776-107">EXAMPLES</span></span>

### <span data-ttu-id="f6776-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f6776-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="f6776-109">Eltávolítja a WcfRelay `TestWCFRelay1` a névtérből `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="f6776-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="f6776-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6776-110">PARAMETERS</span></span>

### <span data-ttu-id="f6776-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6776-111">-DefaultProfile</span></span>
<span data-ttu-id="f6776-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6776-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6776-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6776-113">-Name</span></span>
<span data-ttu-id="f6776-114">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="f6776-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6776-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f6776-115">-Namespace</span></span>
<span data-ttu-id="f6776-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f6776-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6776-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6776-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6776-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f6776-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6776-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6776-119">-Confirm</span></span>
<span data-ttu-id="f6776-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6776-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6776-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6776-121">-WhatIf</span></span>
<span data-ttu-id="f6776-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6776-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6776-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6776-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6776-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6776-124">CommonParameters</span></span>
<span data-ttu-id="f6776-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6776-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6776-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6776-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6776-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6776-127">INPUTS</span></span>

### <span data-ttu-id="f6776-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f6776-128">System.String</span></span>

## <span data-ttu-id="f6776-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6776-129">OUTPUTS</span></span>

### <span data-ttu-id="f6776-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="f6776-130">System.Void</span></span>

## <span data-ttu-id="f6776-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6776-131">NOTES</span></span>

## <span data-ttu-id="f6776-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6776-132">RELATED LINKS</span></span>
