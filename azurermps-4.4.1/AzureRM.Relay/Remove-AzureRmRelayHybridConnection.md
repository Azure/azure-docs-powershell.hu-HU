---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7f65f77d9d1f525dd8850c6934263b608d241751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501643"
---
# <span data-ttu-id="4c328-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="4c328-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="4c328-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c328-102">SYNOPSIS</span></span>
<span data-ttu-id="4c328-103">Eltávolítja a HybridConnection a megadott HybridConnection-névtérből.</span><span class="sxs-lookup"><span data-stu-id="4c328-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c328-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c328-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c328-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c328-105">DESCRIPTION</span></span>
<span data-ttu-id="4c328-106">A **Remove-AzureRmRelayHybridConnection** parancsmag eltávolítja a HybridConnection a megadott továbbító névtérből.</span><span class="sxs-lookup"><span data-stu-id="4c328-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="4c328-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4c328-107">EXAMPLES</span></span>

### <span data-ttu-id="4c328-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c328-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="4c328-109">Eltávolítja a HybridConnection `TestHybridConnection` a névtérből `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="4c328-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="4c328-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c328-110">PARAMETERS</span></span>

### <span data-ttu-id="4c328-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c328-111">-Name</span></span>
<span data-ttu-id="4c328-112">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="4c328-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="4c328-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4c328-113">-Namespace</span></span>
<span data-ttu-id="4c328-114">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="4c328-114">Namespace Name.</span></span>

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

### <span data-ttu-id="4c328-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c328-115">-ResourceGroupName</span></span>
<span data-ttu-id="4c328-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4c328-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="4c328-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c328-117">-Confirm</span></span>
<span data-ttu-id="4c328-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c328-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c328-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c328-119">-WhatIf</span></span>
<span data-ttu-id="4c328-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4c328-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c328-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c328-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c328-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c328-122">-DefaultProfile</span></span>
<span data-ttu-id="4c328-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c328-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c328-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c328-124">CommonParameters</span></span>
<span data-ttu-id="4c328-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c328-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c328-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c328-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c328-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c328-127">INPUTS</span></span>

### <span data-ttu-id="4c328-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c328-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="4c328-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4c328-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="4c328-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c328-130">-Name</span></span>
    System.String

## <span data-ttu-id="4c328-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c328-131">OUTPUTS</span></span>

### <span data-ttu-id="4c328-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="4c328-132">System.Object</span></span>

## <span data-ttu-id="4c328-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c328-133">NOTES</span></span>

## <span data-ttu-id="4c328-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c328-134">RELATED LINKS</span></span>

