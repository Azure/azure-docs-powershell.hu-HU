---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: ed59b77a934787b1030166b24e9ed3af81698c16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936074"
---
# <span data-ttu-id="44bf0-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="44bf0-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="44bf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="44bf0-103">Letiltja a komplex veszélyforrások elleni védelemre vonatkozó speciális házirendet egy tár- vagy tárterületDB-fiókban.</span><span class="sxs-lookup"><span data-stu-id="44bf0-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="44bf0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44bf0-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44bf0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="44bf0-106">A `Disable-AzSecurityAdvancedThreatProtection` parancsmag letiltja a veszélyforrás-védelmi házirendet egy storage/cossDB-fiókban.</span><span class="sxs-lookup"><span data-stu-id="44bf0-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="44bf0-107">A parancsmagot a *ResourceId paraméter megadásával használhatja.*</span><span class="sxs-lookup"><span data-stu-id="44bf0-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="44bf0-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44bf0-108">EXAMPLES</span></span>

### <span data-ttu-id="44bf0-109">1. példa: Tárfiók</span><span class="sxs-lookup"><span data-stu-id="44bf0-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="44bf0-110">Ez a parancs letiltja a komplex veszélyforrás-védelmi házirendet az erőforrás-azonosítóhoz. `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`</span><span class="sxs-lookup"><span data-stu-id="44bf0-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="44bf0-111">2. példa: EzresDB-fiók</span><span class="sxs-lookup"><span data-stu-id="44bf0-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="44bf0-112">Ez a parancs letiltja a komplex veszélyforrás-védelmi házirendet az erőforrás-azonosítóhoz. ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`</span><span class="sxs-lookup"><span data-stu-id="44bf0-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="44bf0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44bf0-113">PARAMETERS</span></span>

### <span data-ttu-id="44bf0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44bf0-114">-DefaultProfile</span></span>
<span data-ttu-id="44bf0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44bf0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44bf0-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44bf0-116">-ResourceId</span></span>
<span data-ttu-id="44bf0-117">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="44bf0-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="44bf0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44bf0-118">-Confirm</span></span>
<span data-ttu-id="44bf0-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44bf0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44bf0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44bf0-120">-WhatIf</span></span>
<span data-ttu-id="44bf0-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44bf0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44bf0-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44bf0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44bf0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44bf0-123">CommonParameters</span></span>
<span data-ttu-id="44bf0-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44bf0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44bf0-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44bf0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44bf0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44bf0-126">INPUTS</span></span>

### <span data-ttu-id="44bf0-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="44bf0-127">None</span></span>

## <span data-ttu-id="44bf0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44bf0-128">OUTPUTS</span></span>

### <span data-ttu-id="44bf0-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="44bf0-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="44bf0-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44bf0-130">NOTES</span></span>

## <span data-ttu-id="44bf0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44bf0-131">RELATED LINKS</span></span>
