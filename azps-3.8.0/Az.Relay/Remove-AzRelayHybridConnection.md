---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846862"
---
# <span data-ttu-id="08525-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="08525-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="08525-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08525-102">SYNOPSIS</span></span>
<span data-ttu-id="08525-103">Eltávolítja a HybridConnection a megadott HybridConnection-névtérből.</span><span class="sxs-lookup"><span data-stu-id="08525-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="08525-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08525-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08525-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08525-105">DESCRIPTION</span></span>
<span data-ttu-id="08525-106">A **Remove-AzRelayHybridConnection** parancsmag eltávolítja a HybridConnection a megadott továbbító névtérből.</span><span class="sxs-lookup"><span data-stu-id="08525-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="08525-107">Példák</span><span class="sxs-lookup"><span data-stu-id="08525-107">EXAMPLES</span></span>

### <span data-ttu-id="08525-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08525-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="08525-109">Eltávolítja a HybridConnection `TestHybridConnection` a névtérből `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="08525-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="08525-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08525-110">PARAMETERS</span></span>

### <span data-ttu-id="08525-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08525-111">-DefaultProfile</span></span>
<span data-ttu-id="08525-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08525-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08525-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08525-113">-Name</span></span>
<span data-ttu-id="08525-114">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="08525-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="08525-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="08525-115">-Namespace</span></span>
<span data-ttu-id="08525-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="08525-116">Namespace Name.</span></span>

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

### <span data-ttu-id="08525-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08525-117">-ResourceGroupName</span></span>
<span data-ttu-id="08525-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="08525-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="08525-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08525-119">-Confirm</span></span>
<span data-ttu-id="08525-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08525-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08525-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08525-121">-WhatIf</span></span>
<span data-ttu-id="08525-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08525-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08525-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08525-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08525-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08525-124">CommonParameters</span></span>
<span data-ttu-id="08525-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08525-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08525-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08525-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08525-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08525-127">INPUTS</span></span>

### <span data-ttu-id="08525-128">System. String</span><span class="sxs-lookup"><span data-stu-id="08525-128">System.String</span></span>

## <span data-ttu-id="08525-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08525-129">OUTPUTS</span></span>

### <span data-ttu-id="08525-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="08525-130">System.Void</span></span>

## <span data-ttu-id="08525-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08525-131">NOTES</span></span>

## <span data-ttu-id="08525-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08525-132">RELATED LINKS</span></span>