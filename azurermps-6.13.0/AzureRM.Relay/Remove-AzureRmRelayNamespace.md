---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: ac6327176c587bcb221a5ebddbb12ae9adeffbf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680021"
---
# <span data-ttu-id="fd3a5-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="fd3a5-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="fd3a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3a5-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="fd3a5-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd3a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd3a5-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd3a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd3a5-105">DESCRIPTION</span></span>
<span data-ttu-id="fd3a5-106">A **Remove-AzureRmRelayNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="fd3a5-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="fd3a5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fd3a5-107">EXAMPLES</span></span>

### <span data-ttu-id="fd3a5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd3a5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="fd3a5-109">A továbbítási névtér eltávolítása `TestNameSpace-Relay1` a megadott erőforrás-csoportból `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="fd3a5-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="fd3a5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd3a5-110">PARAMETERS</span></span>

### <span data-ttu-id="fd3a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3a5-111">-DefaultProfile</span></span>
<span data-ttu-id="fd3a5-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd3a5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd3a5-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd3a5-113">-Name</span></span>
<span data-ttu-id="fd3a5-114">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="fd3a5-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="fd3a5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd3a5-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd3a5-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fd3a5-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="fd3a5-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd3a5-117">-Confirm</span></span>
<span data-ttu-id="fd3a5-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd3a5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd3a5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd3a5-119">-WhatIf</span></span>
<span data-ttu-id="fd3a5-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd3a5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd3a5-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd3a5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd3a5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3a5-122">CommonParameters</span></span>
<span data-ttu-id="fd3a5-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd3a5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fd3a5-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd3a5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3a5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd3a5-125">INPUTS</span></span>

### <span data-ttu-id="fd3a5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fd3a5-126">System.String</span></span>


## <span data-ttu-id="fd3a5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd3a5-127">OUTPUTS</span></span>

### <span data-ttu-id="fd3a5-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="fd3a5-128">System.Void</span></span>


## <span data-ttu-id="fd3a5-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd3a5-129">NOTES</span></span>

## <span data-ttu-id="fd3a5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd3a5-130">RELATED LINKS</span></span>
