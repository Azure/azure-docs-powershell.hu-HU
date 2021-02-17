---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208335"
---
# <span data-ttu-id="a9e67-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a9e67-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="a9e67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e67-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e67-103">Komplex veszélyforrások elleni védelemre vonatkozó speciális házirendet kap egy tárhely- vagy tárterületDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a9e67-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="a9e67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9e67-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9e67-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9e67-105">DESCRIPTION</span></span>
<span data-ttu-id="a9e67-106">A `Get-AzSecurityAdvancedThreatProtection` parancsmag megkapja a veszélyforrás-védelmi házirendet egy tároló- vagy tárterületDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a9e67-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="a9e67-107">A parancsmagot a *ResourceId paraméter megadásával használhatja.*</span><span class="sxs-lookup"><span data-stu-id="a9e67-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="a9e67-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9e67-108">EXAMPLES</span></span>

### <span data-ttu-id="a9e67-109">1. példa: Tárfiók</span><span class="sxs-lookup"><span data-stu-id="a9e67-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="a9e67-110">Ez a parancs az erőforrás-azonosító komplex veszélyforrás-védelmi házirendet `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` kapja.</span><span class="sxs-lookup"><span data-stu-id="a9e67-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="a9e67-111">2. példa: EzresDB-fiók</span><span class="sxs-lookup"><span data-stu-id="a9e67-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="a9e67-112">Ez a parancs az erőforrás-azonosító komplex veszélyforrás-védelmi házirendet ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` kapja.</span><span class="sxs-lookup"><span data-stu-id="a9e67-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="a9e67-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9e67-113">PARAMETERS</span></span>

### <span data-ttu-id="a9e67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e67-114">-DefaultProfile</span></span>
<span data-ttu-id="a9e67-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9e67-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e67-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e67-116">-ResourceId</span></span>
<span data-ttu-id="a9e67-117">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="a9e67-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a9e67-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e67-118">CommonParameters</span></span>
<span data-ttu-id="a9e67-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e67-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e67-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9e67-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e67-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9e67-121">INPUTS</span></span>

### <span data-ttu-id="a9e67-122">System.String</span><span class="sxs-lookup"><span data-stu-id="a9e67-122">System.String</span></span>

## <span data-ttu-id="a9e67-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9e67-123">OUTPUTS</span></span>

### <span data-ttu-id="a9e67-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a9e67-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="a9e67-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9e67-125">NOTES</span></span>

## <span data-ttu-id="a9e67-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9e67-126">RELATED LINKS</span></span>
