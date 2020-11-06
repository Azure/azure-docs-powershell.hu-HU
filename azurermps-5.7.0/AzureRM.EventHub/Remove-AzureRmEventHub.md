---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505524"
---
# <span data-ttu-id="2752c-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="2752c-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="2752c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2752c-102">SYNOPSIS</span></span>
<span data-ttu-id="2752c-103">Eltávolítja a megadott esemény hub-ot.</span><span class="sxs-lookup"><span data-stu-id="2752c-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2752c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2752c-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2752c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2752c-105">DESCRIPTION</span></span>
<span data-ttu-id="2752c-106">A Remove-AzureRmEventHub parancsmag eltávolítja és törli a megadott névtérből a megadott esemény középpontját.</span><span class="sxs-lookup"><span data-stu-id="2752c-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="2752c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2752c-107">EXAMPLES</span></span>

### <span data-ttu-id="2752c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2752c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="2752c-109">Eltávolítja az esemény-hub \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="2752c-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="2752c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2752c-110">PARAMETERS</span></span>

### <span data-ttu-id="2752c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2752c-111">-DefaultProfile</span></span>
<span data-ttu-id="2752c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2752c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2752c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2752c-113">-Name</span></span>
<span data-ttu-id="2752c-114">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="2752c-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2752c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2752c-115">-Namespace</span></span>
<span data-ttu-id="2752c-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="2752c-116">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2752c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2752c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2752c-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2752c-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2752c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2752c-119">-Confirm</span></span>
<span data-ttu-id="2752c-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2752c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2752c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2752c-121">-WhatIf</span></span>
<span data-ttu-id="2752c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2752c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2752c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2752c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2752c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2752c-124">CommonParameters</span></span>
<span data-ttu-id="2752c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2752c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2752c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2752c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2752c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2752c-127">INPUTS</span></span>

### <span data-ttu-id="2752c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2752c-128">System.String</span></span>


## <span data-ttu-id="2752c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2752c-129">OUTPUTS</span></span>

### <span data-ttu-id="2752c-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="2752c-130">System.Object</span></span>

## <span data-ttu-id="2752c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2752c-131">NOTES</span></span>

## <span data-ttu-id="2752c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2752c-132">RELATED LINKS</span></span>
