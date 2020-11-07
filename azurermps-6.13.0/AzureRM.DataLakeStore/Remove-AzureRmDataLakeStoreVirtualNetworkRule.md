---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672956"
---
# <span data-ttu-id="e5294-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e5294-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e5294-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5294-102">SYNOPSIS</span></span>
<span data-ttu-id="e5294-103">A megadott virtuális hálózati szabály eltávolítása a megadott Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="e5294-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5294-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5294-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5294-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5294-105">DESCRIPTION</span></span>
<span data-ttu-id="e5294-106">A **Remove-AzureRmDataLakeStoreVirtualNetworkRule** parancsmag eltávolítja a megadott virtuális hálózati szabályt a megadott Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="e5294-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="e5294-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5294-107">EXAMPLES</span></span>

### <span data-ttu-id="e5294-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e5294-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="e5294-109">A "myVNET" virtuális hálózati szabály eltávolítása a "frissíteni" fiókból</span><span class="sxs-lookup"><span data-stu-id="e5294-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="e5294-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5294-110">PARAMETERS</span></span>

### <span data-ttu-id="e5294-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="e5294-111">-Account</span></span>
<span data-ttu-id="e5294-112">Az Data Lake Store fiók a virtuális hálózati szabály frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="e5294-112">The Data Lake Store account to update the virtual network rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5294-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5294-113">-DefaultProfile</span></span>
<span data-ttu-id="e5294-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5294-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5294-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5294-115">-Name</span></span>
<span data-ttu-id="e5294-116">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="e5294-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5294-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5294-117">-PassThru</span></span>
<span data-ttu-id="e5294-118">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e5294-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5294-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5294-119">-Confirm</span></span>
<span data-ttu-id="e5294-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5294-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5294-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5294-121">-WhatIf</span></span>
<span data-ttu-id="e5294-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5294-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5294-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5294-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5294-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5294-124">CommonParameters</span></span>
<span data-ttu-id="e5294-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5294-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5294-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5294-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5294-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5294-127">INPUTS</span></span>

### <span data-ttu-id="e5294-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e5294-128">System.String</span></span>

### <span data-ttu-id="e5294-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e5294-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5294-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5294-130">OUTPUTS</span></span>

### <span data-ttu-id="e5294-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5294-131">System.Boolean</span></span>

## <span data-ttu-id="e5294-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5294-132">NOTES</span></span>

## <span data-ttu-id="e5294-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5294-133">RELATED LINKS</span></span>
