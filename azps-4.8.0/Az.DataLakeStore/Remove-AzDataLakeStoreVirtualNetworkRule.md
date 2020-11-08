---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017845"
---
# <span data-ttu-id="edfc2-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="edfc2-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="edfc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="edfc2-102">SYNOPSIS</span></span>
<span data-ttu-id="edfc2-103">A megadott virtuális hálózati szabály eltávolítása a megadott Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="edfc2-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="edfc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="edfc2-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edfc2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="edfc2-105">DESCRIPTION</span></span>
<span data-ttu-id="edfc2-106">A **Remove-AzDataLakeStoreVirtualNetworkRule** parancsmag eltávolítja a megadott virtuális hálózati szabályt a megadott Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="edfc2-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="edfc2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="edfc2-107">EXAMPLES</span></span>

### <span data-ttu-id="edfc2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="edfc2-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="edfc2-109">A "myVNET" virtuális hálózati szabály eltávolítása a "frissíteni" fiókból</span><span class="sxs-lookup"><span data-stu-id="edfc2-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="edfc2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="edfc2-110">PARAMETERS</span></span>

### <span data-ttu-id="edfc2-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="edfc2-111">-Account</span></span>
<span data-ttu-id="edfc2-112">Az Data Lake Store fiók a virtuális hálózati szabály frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="edfc2-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="edfc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfc2-113">-DefaultProfile</span></span>
<span data-ttu-id="edfc2-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edfc2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edfc2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="edfc2-115">-Name</span></span>
<span data-ttu-id="edfc2-116">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="edfc2-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="edfc2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edfc2-117">-PassThru</span></span>
<span data-ttu-id="edfc2-118">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="edfc2-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="edfc2-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="edfc2-119">-Confirm</span></span>
<span data-ttu-id="edfc2-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="edfc2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edfc2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edfc2-121">-WhatIf</span></span>
<span data-ttu-id="edfc2-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="edfc2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edfc2-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="edfc2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edfc2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfc2-124">CommonParameters</span></span>
<span data-ttu-id="edfc2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="edfc2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfc2-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edfc2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfc2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="edfc2-127">INPUTS</span></span>

### <span data-ttu-id="edfc2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="edfc2-128">System.String</span></span>

## <span data-ttu-id="edfc2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edfc2-129">OUTPUTS</span></span>

### <span data-ttu-id="edfc2-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edfc2-130">System.Boolean</span></span>

## <span data-ttu-id="edfc2-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="edfc2-131">NOTES</span></span>

## <span data-ttu-id="edfc2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edfc2-132">RELATED LINKS</span></span>
