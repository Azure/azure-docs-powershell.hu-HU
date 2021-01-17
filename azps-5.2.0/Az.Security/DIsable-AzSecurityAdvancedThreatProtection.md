---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 12cd510a495dbb538532dac95e4388c78e9c6bb5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337517"
---
# <span data-ttu-id="323d6-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="323d6-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="323d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="323d6-102">SYNOPSIS</span></span>
<span data-ttu-id="323d6-103">Letiltja a komplex veszélyforrások elleni védelemre vonatkozó speciális házirendet egy tároló- vagy tárterületDB-fiókban.</span><span class="sxs-lookup"><span data-stu-id="323d6-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="323d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="323d6-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="323d6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="323d6-105">DESCRIPTION</span></span>
<span data-ttu-id="323d6-106">A `Disable-AzSecurityAdvancedThreatProtection` parancsmag letiltja a veszélyforrás-védelmi házirendet egy storage/cossDB-fiókban.</span><span class="sxs-lookup"><span data-stu-id="323d6-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="323d6-107">A parancsmagot a *ResourceId paraméter megadásával használhatja.*</span><span class="sxs-lookup"><span data-stu-id="323d6-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="323d6-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="323d6-108">EXAMPLES</span></span>

### <span data-ttu-id="323d6-109">1. példa: Tárfiók</span><span class="sxs-lookup"><span data-stu-id="323d6-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="323d6-110">Ez a parancs letiltja a komplex veszélyforrás-védelmi házirendet az erőforrás-azonosítóhoz. `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`</span><span class="sxs-lookup"><span data-stu-id="323d6-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="323d6-111">2. példa: EzresDB-fiók</span><span class="sxs-lookup"><span data-stu-id="323d6-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="323d6-112">Ez a parancs letiltja a komplex veszélyforrás-védelmi házirendet az erőforrás-azonosítóhoz. ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`</span><span class="sxs-lookup"><span data-stu-id="323d6-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="323d6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="323d6-113">PARAMETERS</span></span>

### <span data-ttu-id="323d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="323d6-114">-DefaultProfile</span></span>
<span data-ttu-id="323d6-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="323d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="323d6-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="323d6-116">-ResourceId</span></span>
<span data-ttu-id="323d6-117">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="323d6-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="323d6-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="323d6-118">-Confirm</span></span>
<span data-ttu-id="323d6-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="323d6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="323d6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="323d6-120">-WhatIf</span></span>
<span data-ttu-id="323d6-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="323d6-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="323d6-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="323d6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="323d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323d6-123">CommonParameters</span></span>
<span data-ttu-id="323d6-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="323d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323d6-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="323d6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323d6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="323d6-126">INPUTS</span></span>

### <span data-ttu-id="323d6-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="323d6-127">None</span></span>

## <span data-ttu-id="323d6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="323d6-128">OUTPUTS</span></span>

### <span data-ttu-id="323d6-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="323d6-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="323d6-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="323d6-130">NOTES</span></span>

## <span data-ttu-id="323d6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="323d6-131">RELATED LINKS</span></span>
