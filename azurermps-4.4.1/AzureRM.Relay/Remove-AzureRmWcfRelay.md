---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: a774f388690ab2ee0528e94a2a96addecf1687fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504771"
---
# <span data-ttu-id="d0032-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="d0032-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="d0032-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0032-102">SYNOPSIS</span></span>
<span data-ttu-id="d0032-103">Eltávolítja a WcfRelay a megadott továbbítási névtérből.</span><span class="sxs-lookup"><span data-stu-id="d0032-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0032-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0032-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0032-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0032-105">DESCRIPTION</span></span>
<span data-ttu-id="d0032-106">A **Remove-AzureRmWcfRelay** parancsmag eltávolítja a WcfRelay a megadott továbbító névtérből.</span><span class="sxs-lookup"><span data-stu-id="d0032-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="d0032-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d0032-107">EXAMPLES</span></span>

### <span data-ttu-id="d0032-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d0032-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="d0032-109">Eltávolítja a WcfRelay `TestWCFRelay1` a névtérből `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="d0032-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="d0032-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0032-110">PARAMETERS</span></span>

### <span data-ttu-id="d0032-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0032-111">-Namespace</span></span>
<span data-ttu-id="d0032-112">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d0032-112">Namespace Name.</span></span>

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

### <span data-ttu-id="d0032-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0032-113">-ResourceGroupName</span></span>
<span data-ttu-id="d0032-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d0032-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0032-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0032-115">-Name</span></span>
<span data-ttu-id="d0032-116">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="d0032-116">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d0032-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0032-117">-Confirm</span></span>
<span data-ttu-id="d0032-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0032-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0032-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0032-119">-WhatIf</span></span>
<span data-ttu-id="d0032-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0032-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0032-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0032-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0032-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0032-122">-DefaultProfile</span></span>
<span data-ttu-id="d0032-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0032-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0032-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0032-124">CommonParameters</span></span>
<span data-ttu-id="d0032-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0032-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0032-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0032-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0032-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0032-127">INPUTS</span></span>

### <span data-ttu-id="d0032-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0032-128">-ResourceGroupName</span></span>
 <span data-ttu-id="d0032-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d0032-129">System.String</span></span>
 

### <span data-ttu-id="d0032-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0032-130">-Namespace</span></span>
 <span data-ttu-id="d0032-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d0032-131">System.String</span></span>
 

### <span data-ttu-id="d0032-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0032-132">-Name</span></span>
 <span data-ttu-id="d0032-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d0032-133">System.String</span></span>

## <span data-ttu-id="d0032-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0032-134">OUTPUTS</span></span>

### <span data-ttu-id="d0032-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="d0032-135">System.Object</span></span>

## <span data-ttu-id="d0032-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0032-136">NOTES</span></span>

## <span data-ttu-id="d0032-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0032-137">RELATED LINKS</span></span>

