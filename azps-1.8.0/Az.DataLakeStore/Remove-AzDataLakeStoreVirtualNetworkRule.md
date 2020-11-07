---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 7faa09d45082e6443ab389ebe3a355c9656bb8e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836273"
---
# <span data-ttu-id="fb2e3-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fb2e3-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="fb2e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb2e3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2e3-103">A megadott virtuális hálózati szabály eltávolítása a megadott Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="fb2e3-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="fb2e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb2e3-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb2e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb2e3-105">DESCRIPTION</span></span>
<span data-ttu-id="fb2e3-106">A **Remove-AzDataLakeStoreVirtualNetworkRule** parancsmag eltávolítja a megadott virtuális hálózati szabályt a megadott Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="fb2e3-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="fb2e3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb2e3-107">EXAMPLES</span></span>

### <span data-ttu-id="fb2e3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb2e3-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="fb2e3-109">A "myVNET" virtuális hálózati szabály eltávolítása a "frissíteni" fiókból</span><span class="sxs-lookup"><span data-stu-id="fb2e3-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="fb2e3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb2e3-110">PARAMETERS</span></span>

### <span data-ttu-id="fb2e3-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="fb2e3-111">-Account</span></span>
<span data-ttu-id="fb2e3-112">Az Data Lake Store fiók a virtuális hálózati szabály frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="fb2e3-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="fb2e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2e3-113">-DefaultProfile</span></span>
<span data-ttu-id="fb2e3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb2e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb2e3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb2e3-115">-Name</span></span>
<span data-ttu-id="fb2e3-116">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fb2e3-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="fb2e3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb2e3-117">-PassThru</span></span>
<span data-ttu-id="fb2e3-118">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fb2e3-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="fb2e3-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb2e3-119">-Confirm</span></span>
<span data-ttu-id="fb2e3-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb2e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb2e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb2e3-121">-WhatIf</span></span>
<span data-ttu-id="fb2e3-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb2e3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb2e3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb2e3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb2e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2e3-124">CommonParameters</span></span>
<span data-ttu-id="fb2e3-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb2e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2e3-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb2e3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2e3-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb2e3-127">INPUTS</span></span>

### <span data-ttu-id="fb2e3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fb2e3-128">System.String</span></span>

## <span data-ttu-id="fb2e3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb2e3-129">OUTPUTS</span></span>

### <span data-ttu-id="fb2e3-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb2e3-130">System.Boolean</span></span>

## <span data-ttu-id="fb2e3-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb2e3-131">NOTES</span></span>

## <span data-ttu-id="fb2e3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb2e3-132">RELATED LINKS</span></span>
