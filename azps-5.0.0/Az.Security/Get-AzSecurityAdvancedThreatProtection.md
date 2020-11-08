---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187537"
---
# <span data-ttu-id="c7908-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c7908-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="c7908-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7908-102">SYNOPSIS</span></span>
<span data-ttu-id="c7908-103">Megkeresi az Advanced Threat Protection házirendet egy tárterület-vagy cosmosDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c7908-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="c7908-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7908-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7908-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7908-105">DESCRIPTION</span></span>
<span data-ttu-id="c7908-106">A `Get-AzSecurityAdvancedThreatProtection` parancsmag egy tárterület-vagy cosmosDB-fiókhoz kapja a fenyegetések elleni védelemre vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="c7908-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="c7908-107">A parancsmag használatához adja meg a *ResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="c7908-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="c7908-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c7908-108">EXAMPLES</span></span>

### <span data-ttu-id="c7908-109">1. példa: tárterület-fiók</span><span class="sxs-lookup"><span data-stu-id="c7908-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="c7908-110">Ez a parancs az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet kapja meg `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="c7908-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="c7908-111">2. példa: CosmosDB-fiók</span><span class="sxs-lookup"><span data-stu-id="c7908-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="c7908-112">Ez a parancs az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet kapja meg ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="c7908-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="c7908-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7908-113">PARAMETERS</span></span>

### <span data-ttu-id="c7908-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7908-114">-DefaultProfile</span></span>
<span data-ttu-id="c7908-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7908-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7908-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7908-116">-ResourceId</span></span>
<span data-ttu-id="c7908-117">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="c7908-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c7908-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7908-118">CommonParameters</span></span>
<span data-ttu-id="c7908-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7908-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7908-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c7908-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7908-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7908-121">INPUTS</span></span>

### <span data-ttu-id="c7908-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c7908-122">System.String</span></span>

## <span data-ttu-id="c7908-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7908-123">OUTPUTS</span></span>

### <span data-ttu-id="c7908-124">Microsoft. Azure. commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c7908-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="c7908-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7908-125">NOTES</span></span>

## <span data-ttu-id="c7908-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7908-126">RELATED LINKS</span></span>
