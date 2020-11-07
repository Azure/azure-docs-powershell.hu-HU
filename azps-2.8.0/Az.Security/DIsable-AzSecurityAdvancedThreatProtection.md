---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: c2d2bcaf95b7eda010cc299a7c20cfd703f7eadb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838087"
---
# <span data-ttu-id="b7d25-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b7d25-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="b7d25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7d25-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d25-103">Letiltja a speciális veszélyforrások elleni védelemre vonatkozó házirendet egy tárterület-vagy cosmosDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b7d25-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="b7d25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7d25-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7d25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7d25-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d25-106">A `Disable-AzSecurityAdvancedThreatProtection` parancsmag letiltja a tároló-vagy cosmosDB-fiók fenyegetések elleni védelmét szolgáló házirendet.</span><span class="sxs-lookup"><span data-stu-id="b7d25-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="b7d25-107">A parancsmag használatához adja meg a *ResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b7d25-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="b7d25-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b7d25-108">EXAMPLES</span></span>

### <span data-ttu-id="b7d25-109">1. példa: tárterület-fiók</span><span class="sxs-lookup"><span data-stu-id="b7d25-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="b7d25-110">Ez a parancs letiltja az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="b7d25-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="b7d25-111">2. példa: CosmosDB-fiók</span><span class="sxs-lookup"><span data-stu-id="b7d25-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="b7d25-112">Ez a parancs letiltja az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="b7d25-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="b7d25-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7d25-113">PARAMETERS</span></span>

### <span data-ttu-id="b7d25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d25-114">-DefaultProfile</span></span>
<span data-ttu-id="b7d25-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7d25-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7d25-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7d25-116">-ResourceId</span></span>
<span data-ttu-id="b7d25-117">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="b7d25-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b7d25-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7d25-118">-Confirm</span></span>
<span data-ttu-id="b7d25-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7d25-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d25-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d25-120">-WhatIf</span></span>
<span data-ttu-id="b7d25-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7d25-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7d25-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7d25-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d25-123">CommonParameters</span></span>
<span data-ttu-id="b7d25-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7d25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d25-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7d25-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d25-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7d25-126">INPUTS</span></span>

### <span data-ttu-id="b7d25-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="b7d25-127">None</span></span>

## <span data-ttu-id="b7d25-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7d25-128">OUTPUTS</span></span>

### <span data-ttu-id="b7d25-129">Microsoft. Azure. commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b7d25-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="b7d25-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7d25-130">NOTES</span></span>

## <span data-ttu-id="b7d25-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7d25-131">RELATED LINKS</span></span>
