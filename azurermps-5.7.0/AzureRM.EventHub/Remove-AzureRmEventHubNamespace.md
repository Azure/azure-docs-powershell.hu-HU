---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672646"
---
# <span data-ttu-id="5272b-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5272b-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="5272b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5272b-102">SYNOPSIS</span></span>
<span data-ttu-id="5272b-103">Eltávolítja a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="5272b-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5272b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5272b-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5272b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5272b-105">DESCRIPTION</span></span>
<span data-ttu-id="5272b-106">A Remove-AzureRmEventHubNamespace parancsmag eltávolítja és törli a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="5272b-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="5272b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5272b-107">EXAMPLES</span></span>

### <span data-ttu-id="5272b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5272b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="5272b-109">Eltávolítja az esemény-hubok \` névtér \` -MyNamespaceName az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5272b-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5272b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5272b-110">PARAMETERS</span></span>

### <span data-ttu-id="5272b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5272b-111">-DefaultProfile</span></span>
<span data-ttu-id="5272b-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5272b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5272b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5272b-113">-Name</span></span>
<span data-ttu-id="5272b-114">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="5272b-114">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="5272b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5272b-115">-ResourceGroupName</span></span>
<span data-ttu-id="5272b-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5272b-116">Resource Group Name</span></span>

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

### <span data-ttu-id="5272b-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5272b-117">-Confirm</span></span>
<span data-ttu-id="5272b-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5272b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5272b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5272b-119">-WhatIf</span></span>
<span data-ttu-id="5272b-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5272b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5272b-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5272b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5272b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5272b-122">CommonParameters</span></span>
<span data-ttu-id="5272b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5272b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5272b-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5272b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5272b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5272b-125">INPUTS</span></span>

### <span data-ttu-id="5272b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5272b-126">System.String</span></span>


## <span data-ttu-id="5272b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5272b-127">OUTPUTS</span></span>

### <span data-ttu-id="5272b-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5272b-128">System.Object</span></span>

## <span data-ttu-id="5272b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5272b-129">NOTES</span></span>

## <span data-ttu-id="5272b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5272b-130">RELATED LINKS</span></span>
