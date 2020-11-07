---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: deef0be93c3a80c0db9762907eb52cdc51da9ed3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669263"
---
# <span data-ttu-id="6daa6-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6daa6-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="6daa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6daa6-102">SYNOPSIS</span></span>
<span data-ttu-id="6daa6-103">Lehetővé teszi a speciális veszélyforrások elleni védelemre vonatkozó házirendet egy tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6daa6-103">Enables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="6daa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6daa6-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6daa6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6daa6-105">DESCRIPTION</span></span>
<span data-ttu-id="6daa6-106">A `Enable-AzSecurityAdvancedThreatProtection` parancsmag lehetővé teszi a Protetion-házirendet a tárolási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6daa6-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="6daa6-107">A parancsmag használatához adja meg a *ResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="6daa6-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="6daa6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6daa6-108">EXAMPLES</span></span>

### <span data-ttu-id="6daa6-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6daa6-109">Example 1</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="6daa6-110">Ez a parancs lehetővé teszi az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="6daa6-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="6daa6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6daa6-111">PARAMETERS</span></span>

### <span data-ttu-id="6daa6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6daa6-112">-DefaultProfile</span></span>
<span data-ttu-id="6daa6-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6daa6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6daa6-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6daa6-114">-ResourceId</span></span>
<span data-ttu-id="6daa6-115">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="6daa6-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="6daa6-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6daa6-116">-Confirm</span></span>
<span data-ttu-id="6daa6-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6daa6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6daa6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6daa6-118">-WhatIf</span></span>
<span data-ttu-id="6daa6-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6daa6-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6daa6-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6daa6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6daa6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6daa6-121">CommonParameters</span></span>
<span data-ttu-id="6daa6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6daa6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6daa6-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6daa6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6daa6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6daa6-124">INPUTS</span></span>

### <span data-ttu-id="6daa6-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="6daa6-125">None</span></span>

## <span data-ttu-id="6daa6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6daa6-126">OUTPUTS</span></span>

### <span data-ttu-id="6daa6-127">Microsoft. Azure. commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6daa6-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="6daa6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6daa6-128">NOTES</span></span>

## <span data-ttu-id="6daa6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6daa6-129">RELATED LINKS</span></span>
