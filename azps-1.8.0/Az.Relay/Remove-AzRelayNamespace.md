---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: dec858fe113725876e7e46d72cf996d9338b34eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669500"
---
# <span data-ttu-id="eaf7e-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="eaf7e-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="eaf7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eaf7e-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf7e-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="eaf7e-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="eaf7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eaf7e-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf7e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eaf7e-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf7e-106">A **Remove-AzRelayNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="eaf7e-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="eaf7e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eaf7e-107">EXAMPLES</span></span>

### <span data-ttu-id="eaf7e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eaf7e-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="eaf7e-109">A továbbítási névtér eltávolítása `TestNameSpace-Relay1` a megadott erőforrás-csoportból `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="eaf7e-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="eaf7e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eaf7e-110">PARAMETERS</span></span>

### <span data-ttu-id="eaf7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf7e-111">-DefaultProfile</span></span>
<span data-ttu-id="eaf7e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eaf7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf7e-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eaf7e-113">-Name</span></span>
<span data-ttu-id="eaf7e-114">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="eaf7e-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="eaf7e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf7e-115">-ResourceGroupName</span></span>
<span data-ttu-id="eaf7e-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="eaf7e-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="eaf7e-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eaf7e-117">-Confirm</span></span>
<span data-ttu-id="eaf7e-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eaf7e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf7e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf7e-119">-WhatIf</span></span>
<span data-ttu-id="eaf7e-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eaf7e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf7e-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eaf7e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf7e-122">CommonParameters</span></span>
<span data-ttu-id="eaf7e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eaf7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf7e-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf7e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf7e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaf7e-125">INPUTS</span></span>

### <span data-ttu-id="eaf7e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="eaf7e-126">System.String</span></span>

## <span data-ttu-id="eaf7e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaf7e-127">OUTPUTS</span></span>

### <span data-ttu-id="eaf7e-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="eaf7e-128">System.Void</span></span>

## <span data-ttu-id="eaf7e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eaf7e-129">NOTES</span></span>

## <span data-ttu-id="eaf7e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eaf7e-130">RELATED LINKS</span></span>
