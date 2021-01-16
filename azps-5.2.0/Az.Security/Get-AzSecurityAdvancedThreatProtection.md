---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349097"
---
# <span data-ttu-id="2ab55-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2ab55-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="2ab55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ab55-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab55-103">Komplex veszélyforrások elleni védelemre vonatkozó speciális házirendet kap egy tárhely- vagy tárterületDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="2ab55-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="2ab55-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ab55-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ab55-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ab55-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab55-106">A `Get-AzSecurityAdvancedThreatProtection` parancsmag megkapja a veszélyforrás-védelmi házirendet egy tárterület-/tárterületDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="2ab55-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="2ab55-107">A parancsmagot a *ResourceId paraméter megadásával használhatja.*</span><span class="sxs-lookup"><span data-stu-id="2ab55-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="2ab55-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ab55-108">EXAMPLES</span></span>

### <span data-ttu-id="2ab55-109">1. példa: Tárfiók</span><span class="sxs-lookup"><span data-stu-id="2ab55-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="2ab55-110">Ez a parancs az erőforrás-azonosító komplex veszélyforrás-védelmi házirendet `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` kapja.</span><span class="sxs-lookup"><span data-stu-id="2ab55-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="2ab55-111">2. példa: EzresDB-fiók</span><span class="sxs-lookup"><span data-stu-id="2ab55-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="2ab55-112">Ez a parancs az erőforrás-azonosító komplex veszélyforrás-védelmi házirendet ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` kapja.</span><span class="sxs-lookup"><span data-stu-id="2ab55-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="2ab55-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ab55-113">PARAMETERS</span></span>

### <span data-ttu-id="2ab55-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab55-114">-DefaultProfile</span></span>
<span data-ttu-id="2ab55-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ab55-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ab55-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ab55-116">-ResourceId</span></span>
<span data-ttu-id="2ab55-117">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="2ab55-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2ab55-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab55-118">CommonParameters</span></span>
<span data-ttu-id="2ab55-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab55-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab55-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ab55-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab55-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ab55-121">INPUTS</span></span>

### <span data-ttu-id="2ab55-122">System.String</span><span class="sxs-lookup"><span data-stu-id="2ab55-122">System.String</span></span>

## <span data-ttu-id="2ab55-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ab55-123">OUTPUTS</span></span>

### <span data-ttu-id="2ab55-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2ab55-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="2ab55-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ab55-125">NOTES</span></span>

## <span data-ttu-id="2ab55-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ab55-126">RELATED LINKS</span></span>
