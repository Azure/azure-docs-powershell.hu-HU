---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b5b9f154cb494aad7c1ef0faec130b4c4c1cc3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923770"
---
# <span data-ttu-id="06dfe-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="06dfe-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="06dfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="06dfe-103">A megadott virtuális hálózati szabály eltávolítása a megadott Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="06dfe-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="06dfe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06dfe-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06dfe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06dfe-105">DESCRIPTION</span></span>
<span data-ttu-id="06dfe-106">A **Remove-AzDataLakeStoreVirtualNetworkRule** parancsmag eltávolítja a megadott virtuális hálózati szabályt a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="06dfe-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="06dfe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06dfe-107">EXAMPLES</span></span>

### <span data-ttu-id="06dfe-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="06dfe-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="06dfe-109">Eltávolítja a "myVNET" virtuális hálózati szabályt a "dls" fiókból</span><span class="sxs-lookup"><span data-stu-id="06dfe-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="06dfe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06dfe-110">PARAMETERS</span></span>

### <span data-ttu-id="06dfe-111">-Account</span><span class="sxs-lookup"><span data-stu-id="06dfe-111">-Account</span></span>
<span data-ttu-id="06dfe-112">The Data Lake Store account to update the virtual network rule in</span><span class="sxs-lookup"><span data-stu-id="06dfe-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="06dfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06dfe-113">-DefaultProfile</span></span>
<span data-ttu-id="06dfe-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06dfe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06dfe-115">-Name</span><span class="sxs-lookup"><span data-stu-id="06dfe-115">-Name</span></span>
<span data-ttu-id="06dfe-116">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="06dfe-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="06dfe-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06dfe-117">-PassThru</span></span>
<span data-ttu-id="06dfe-118">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="06dfe-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="06dfe-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06dfe-119">-Confirm</span></span>
<span data-ttu-id="06dfe-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06dfe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06dfe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06dfe-121">-WhatIf</span></span>
<span data-ttu-id="06dfe-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06dfe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06dfe-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06dfe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06dfe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dfe-124">CommonParameters</span></span>
<span data-ttu-id="06dfe-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06dfe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dfe-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06dfe-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dfe-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06dfe-127">INPUTS</span></span>

### <span data-ttu-id="06dfe-128">System.String</span><span class="sxs-lookup"><span data-stu-id="06dfe-128">System.String</span></span>

## <span data-ttu-id="06dfe-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06dfe-129">OUTPUTS</span></span>

### <span data-ttu-id="06dfe-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06dfe-130">System.Boolean</span></span>

## <span data-ttu-id="06dfe-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06dfe-131">NOTES</span></span>

## <span data-ttu-id="06dfe-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06dfe-132">RELATED LINKS</span></span>
