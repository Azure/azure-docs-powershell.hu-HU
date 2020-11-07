---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672837"
---
# <span data-ttu-id="06b0f-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="06b0f-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="06b0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="06b0f-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="06b0f-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06b0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06b0f-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b0f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="06b0f-106">A **Remove-AzureRmServiceBusNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="06b0f-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="06b0f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="06b0f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06b0f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="06b0f-109">Eltávolítja a szervizsor névterét `SB-Example1` a megadott erőforráscsoport közül `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="06b0f-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="06b0f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06b0f-110">PARAMETERS</span></span>

### <span data-ttu-id="06b0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b0f-111">-DefaultProfile</span></span>
<span data-ttu-id="06b0f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06b0f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06b0f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06b0f-113">-Name</span></span>
<span data-ttu-id="06b0f-114">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="06b0f-114">Namespace Name.</span></span>

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

### <span data-ttu-id="06b0f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b0f-115">-ResourceGroupName</span></span>
<span data-ttu-id="06b0f-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="06b0f-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b0f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06b0f-117">-Confirm</span></span>
<span data-ttu-id="06b0f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06b0f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b0f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b0f-119">-WhatIf</span></span>
<span data-ttu-id="06b0f-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06b0f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b0f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06b0f-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b0f-122">CommonParameters</span></span>
<span data-ttu-id="06b0f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06b0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b0f-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06b0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b0f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06b0f-125">INPUTS</span></span>

### <span data-ttu-id="06b0f-126">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06b0f-126">-ResourceGroup</span></span>
 <span data-ttu-id="06b0f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="06b0f-127">System.String</span></span>

### <span data-ttu-id="06b0f-128">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="06b0f-128">-NamespaceName</span></span>
 <span data-ttu-id="06b0f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="06b0f-129">System.String</span></span>

## <span data-ttu-id="06b0f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06b0f-130">OUTPUTS</span></span>

### <span data-ttu-id="06b0f-131">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="06b0f-131">System.Object</span></span>

## <span data-ttu-id="06b0f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06b0f-132">NOTES</span></span>

## <span data-ttu-id="06b0f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06b0f-133">RELATED LINKS</span></span>

