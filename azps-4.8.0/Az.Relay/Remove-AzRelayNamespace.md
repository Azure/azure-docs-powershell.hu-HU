---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182700"
---
# <span data-ttu-id="7943b-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="7943b-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="7943b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7943b-102">SYNOPSIS</span></span>
<span data-ttu-id="7943b-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="7943b-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="7943b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7943b-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7943b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7943b-105">DESCRIPTION</span></span>
<span data-ttu-id="7943b-106">A **Remove-AzRelayNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="7943b-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="7943b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7943b-107">EXAMPLES</span></span>

### <span data-ttu-id="7943b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7943b-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="7943b-109">A továbbítási névtér eltávolítása `TestNameSpace-Relay1` a megadott erőforrás-csoportból `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="7943b-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="7943b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7943b-110">PARAMETERS</span></span>

### <span data-ttu-id="7943b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7943b-111">-DefaultProfile</span></span>
<span data-ttu-id="7943b-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7943b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7943b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7943b-113">-Name</span></span>
<span data-ttu-id="7943b-114">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="7943b-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="7943b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7943b-115">-ResourceGroupName</span></span>
<span data-ttu-id="7943b-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7943b-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="7943b-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7943b-117">-Confirm</span></span>
<span data-ttu-id="7943b-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7943b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7943b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7943b-119">-WhatIf</span></span>
<span data-ttu-id="7943b-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7943b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7943b-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7943b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7943b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7943b-122">CommonParameters</span></span>
<span data-ttu-id="7943b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7943b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7943b-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7943b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7943b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7943b-125">INPUTS</span></span>

### <span data-ttu-id="7943b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7943b-126">System.String</span></span>

## <span data-ttu-id="7943b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7943b-127">OUTPUTS</span></span>

### <span data-ttu-id="7943b-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="7943b-128">System.Void</span></span>

## <span data-ttu-id="7943b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7943b-129">NOTES</span></span>

## <span data-ttu-id="7943b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7943b-130">RELATED LINKS</span></span>
