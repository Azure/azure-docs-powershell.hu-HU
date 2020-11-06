---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: d0ac732a0feaffa187ec33d60f9587a7a6a1cff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503219"
---
# <span data-ttu-id="3620c-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="3620c-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="3620c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3620c-102">SYNOPSIS</span></span>
<span data-ttu-id="3620c-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="3620c-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3620c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3620c-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3620c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3620c-105">DESCRIPTION</span></span>
<span data-ttu-id="3620c-106">A **Remove-AzureRmRelayNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="3620c-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="3620c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3620c-107">EXAMPLES</span></span>

### <span data-ttu-id="3620c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3620c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="3620c-109">A továbbítási névtér eltávolítása `TestNameSpace-Relay1` a megadott erőforrás-csoportból `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="3620c-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="3620c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3620c-110">PARAMETERS</span></span>

### <span data-ttu-id="3620c-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3620c-111">-Name</span></span>
<span data-ttu-id="3620c-112">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="3620c-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="3620c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3620c-113">-ResourceGroupName</span></span>
<span data-ttu-id="3620c-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3620c-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="3620c-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3620c-115">-Confirm</span></span>
<span data-ttu-id="3620c-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3620c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3620c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3620c-117">-WhatIf</span></span>
<span data-ttu-id="3620c-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3620c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3620c-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3620c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3620c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3620c-120">-DefaultProfile</span></span>
<span data-ttu-id="3620c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3620c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3620c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3620c-122">CommonParameters</span></span>
<span data-ttu-id="3620c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3620c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3620c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3620c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3620c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3620c-125">INPUTS</span></span>

### <span data-ttu-id="3620c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3620c-126">-ResourceGroupName</span></span>
 <span data-ttu-id="3620c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3620c-127">System.String</span></span>

### <span data-ttu-id="3620c-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3620c-128">-Name</span></span>
 <span data-ttu-id="3620c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3620c-129">System.String</span></span>

## <span data-ttu-id="3620c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3620c-130">OUTPUTS</span></span>

### <span data-ttu-id="3620c-131">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="3620c-131">System.Object</span></span>

## <span data-ttu-id="3620c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3620c-132">NOTES</span></span>

## <span data-ttu-id="3620c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3620c-133">RELATED LINKS</span></span>

