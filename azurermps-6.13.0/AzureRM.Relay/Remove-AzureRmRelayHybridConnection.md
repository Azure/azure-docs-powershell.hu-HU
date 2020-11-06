---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 746033cfdf48782d10c0fdabf7a018d309269afb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491861"
---
# <span data-ttu-id="7bc8e-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="7bc8e-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="7bc8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7bc8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc8e-103">Eltávolítja a HybridConnection a megadott HybridConnection-névtérből.</span><span class="sxs-lookup"><span data-stu-id="7bc8e-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bc8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7bc8e-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc8e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7bc8e-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc8e-106">A **Remove-AzureRmRelayHybridConnection** parancsmag eltávolítja a HybridConnection a megadott továbbító névtérből.</span><span class="sxs-lookup"><span data-stu-id="7bc8e-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="7bc8e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7bc8e-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc8e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7bc8e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="7bc8e-109">Eltávolítja a HybridConnection `TestHybridConnection` a névtérből `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="7bc8e-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="7bc8e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7bc8e-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc8e-111">-DefaultProfile</span></span>
<span data-ttu-id="7bc8e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bc8e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bc8e-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7bc8e-113">-Name</span></span>
<span data-ttu-id="7bc8e-114">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="7bc8e-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="7bc8e-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7bc8e-115">-Namespace</span></span>
<span data-ttu-id="7bc8e-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="7bc8e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="7bc8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="7bc8e-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7bc8e-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="7bc8e-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7bc8e-119">-Confirm</span></span>
<span data-ttu-id="7bc8e-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7bc8e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc8e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc8e-121">-WhatIf</span></span>
<span data-ttu-id="7bc8e-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7bc8e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc8e-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bc8e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc8e-124">CommonParameters</span></span>
<span data-ttu-id="7bc8e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7bc8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7bc8e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc8e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc8e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bc8e-127">INPUTS</span></span>

### <span data-ttu-id="7bc8e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7bc8e-128">System.String</span></span>


## <span data-ttu-id="7bc8e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bc8e-129">OUTPUTS</span></span>

### <span data-ttu-id="7bc8e-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="7bc8e-130">System.Void</span></span>


## <span data-ttu-id="7bc8e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7bc8e-131">NOTES</span></span>

## <span data-ttu-id="7bc8e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bc8e-132">RELATED LINKS</span></span>
