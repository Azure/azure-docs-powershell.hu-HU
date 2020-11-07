---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: a3e83b4c58a7de2a0c020bc156e78656a6fd75ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669265"
---
# <span data-ttu-id="dd319-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="dd319-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="dd319-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd319-102">SYNOPSIS</span></span>
<span data-ttu-id="dd319-103">Letiltja a tároló fiók speciális veszélyforrások elleni védelmét.</span><span class="sxs-lookup"><span data-stu-id="dd319-103">Disables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="dd319-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd319-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd319-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd319-105">DESCRIPTION</span></span>
<span data-ttu-id="dd319-106">A `Disable-AzSecurityAdvancedThreatProtection` parancsmag letiltja a Protetion-házirendet a tárolási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="dd319-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="dd319-107">A parancsmag használatához adja meg a *ResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="dd319-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="dd319-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dd319-108">EXAMPLES</span></span>

### <span data-ttu-id="dd319-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd319-109">Example 1</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="dd319-110">Ez a parancs letiltja az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="dd319-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="dd319-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd319-111">PARAMETERS</span></span>

### <span data-ttu-id="dd319-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd319-112">-DefaultProfile</span></span>
<span data-ttu-id="dd319-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd319-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd319-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd319-114">-ResourceId</span></span>
<span data-ttu-id="dd319-115">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="dd319-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="dd319-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd319-116">-Confirm</span></span>
<span data-ttu-id="dd319-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd319-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd319-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd319-118">-WhatIf</span></span>
<span data-ttu-id="dd319-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd319-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd319-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd319-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd319-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd319-121">CommonParameters</span></span>
<span data-ttu-id="dd319-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd319-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd319-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd319-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd319-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd319-124">INPUTS</span></span>

### <span data-ttu-id="dd319-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="dd319-125">None</span></span>

## <span data-ttu-id="dd319-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd319-126">OUTPUTS</span></span>

### <span data-ttu-id="dd319-127">Microsoft. Azure. commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="dd319-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="dd319-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd319-128">NOTES</span></span>

## <span data-ttu-id="dd319-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd319-129">RELATED LINKS</span></span>
