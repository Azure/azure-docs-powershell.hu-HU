---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194854"
---
# <span data-ttu-id="048e3-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="048e3-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="048e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="048e3-102">SYNOPSIS</span></span>
<span data-ttu-id="048e3-103">Lehetővé teszi a speciális veszélyforrások védelmének házirendjét egy tárterület-vagy cosmosDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="048e3-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="048e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="048e3-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="048e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="048e3-105">DESCRIPTION</span></span>
<span data-ttu-id="048e3-106">A `Enable-AzSecurityAdvancedThreatProtection` parancsmag lehetővé teszi a tároló-vagy cosmosDB-fiók fenyegetések elleni védelemre vonatkozó házirendjét.</span><span class="sxs-lookup"><span data-stu-id="048e3-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="048e3-107">A parancsmag használatához adja meg a *ResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="048e3-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="048e3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="048e3-108">EXAMPLES</span></span>

### <span data-ttu-id="048e3-109">1. példa: tárterület-fiók</span><span class="sxs-lookup"><span data-stu-id="048e3-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="048e3-110">Ez a parancs lehetővé teszi az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="048e3-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="048e3-111">2. példa: CosmosDB-fiók</span><span class="sxs-lookup"><span data-stu-id="048e3-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="048e3-112">Ez a parancs lehetővé teszi az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="048e3-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="048e3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="048e3-113">PARAMETERS</span></span>

### <span data-ttu-id="048e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048e3-114">-DefaultProfile</span></span>
<span data-ttu-id="048e3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="048e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="048e3-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="048e3-116">-ResourceId</span></span>
<span data-ttu-id="048e3-117">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="048e3-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="048e3-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="048e3-118">-Confirm</span></span>
<span data-ttu-id="048e3-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="048e3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="048e3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="048e3-120">-WhatIf</span></span>
<span data-ttu-id="048e3-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="048e3-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="048e3-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="048e3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="048e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048e3-123">CommonParameters</span></span>
<span data-ttu-id="048e3-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="048e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048e3-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="048e3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048e3-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="048e3-126">INPUTS</span></span>

### <span data-ttu-id="048e3-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="048e3-127">None</span></span>

## <span data-ttu-id="048e3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="048e3-128">OUTPUTS</span></span>

### <span data-ttu-id="048e3-129">Microsoft. Azure. commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="048e3-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="048e3-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="048e3-130">NOTES</span></span>

## <span data-ttu-id="048e3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="048e3-131">RELATED LINKS</span></span>
