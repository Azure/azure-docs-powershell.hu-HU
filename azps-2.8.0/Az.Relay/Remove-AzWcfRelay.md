---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f523f0d1166a40e04ac85344c0fc96640a140bb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838965"
---
# <span data-ttu-id="8010a-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="8010a-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="8010a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8010a-102">SYNOPSIS</span></span>
<span data-ttu-id="8010a-103">Eltávolítja a WcfRelay a megadott továbbítási névtérből.</span><span class="sxs-lookup"><span data-stu-id="8010a-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="8010a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8010a-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8010a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8010a-105">DESCRIPTION</span></span>
<span data-ttu-id="8010a-106">A **Remove-AzWcfRelay** parancsmag eltávolítja a WcfRelay a megadott továbbító névtérből.</span><span class="sxs-lookup"><span data-stu-id="8010a-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="8010a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8010a-107">EXAMPLES</span></span>

### <span data-ttu-id="8010a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8010a-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="8010a-109">Eltávolítja a WcfRelay `TestWCFRelay1` a névtérből `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="8010a-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="8010a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8010a-110">PARAMETERS</span></span>

### <span data-ttu-id="8010a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8010a-111">-DefaultProfile</span></span>
<span data-ttu-id="8010a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8010a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8010a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8010a-113">-Name</span></span>
<span data-ttu-id="8010a-114">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="8010a-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="8010a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8010a-115">-Namespace</span></span>
<span data-ttu-id="8010a-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="8010a-116">Namespace Name.</span></span>

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

### <span data-ttu-id="8010a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8010a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8010a-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8010a-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="8010a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8010a-119">-Confirm</span></span>
<span data-ttu-id="8010a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8010a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8010a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8010a-121">-WhatIf</span></span>
<span data-ttu-id="8010a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8010a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8010a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8010a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8010a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8010a-124">CommonParameters</span></span>
<span data-ttu-id="8010a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8010a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8010a-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8010a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8010a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8010a-127">INPUTS</span></span>

### <span data-ttu-id="8010a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8010a-128">System.String</span></span>

## <span data-ttu-id="8010a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8010a-129">OUTPUTS</span></span>

### <span data-ttu-id="8010a-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="8010a-130">System.Void</span></span>

## <span data-ttu-id="8010a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8010a-131">NOTES</span></span>

## <span data-ttu-id="8010a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8010a-132">RELATED LINKS</span></span>
