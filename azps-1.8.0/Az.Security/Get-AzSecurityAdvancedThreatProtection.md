---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669258"
---
# <span data-ttu-id="b27df-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b27df-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="b27df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b27df-102">SYNOPSIS</span></span>
<span data-ttu-id="b27df-103">Az Advanced Threat Protection házirendet kapja meg egy tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b27df-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="b27df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b27df-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b27df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b27df-105">DESCRIPTION</span></span>
<span data-ttu-id="b27df-106">A `Get-AzSecurityAdvancedThreatProtection` parancsmag biztonsági házirendet kap a tárolási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b27df-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="b27df-107">A parancsmag használatához adja meg a *ResourceId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b27df-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="b27df-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b27df-108">EXAMPLES</span></span>

### <span data-ttu-id="b27df-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b27df-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="b27df-110">Ez a parancs az erőforrás-azonosítóhoz tartozó Advanced Threat Protection házirendet kapja meg `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="b27df-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="b27df-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b27df-111">PARAMETERS</span></span>

### <span data-ttu-id="b27df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27df-112">-DefaultProfile</span></span>
<span data-ttu-id="b27df-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b27df-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b27df-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b27df-114">-ResourceId</span></span>
<span data-ttu-id="b27df-115">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="b27df-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b27df-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27df-116">CommonParameters</span></span>
<span data-ttu-id="b27df-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b27df-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27df-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b27df-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27df-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b27df-119">INPUTS</span></span>

### <span data-ttu-id="b27df-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b27df-120">System.String</span></span>

## <span data-ttu-id="b27df-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b27df-121">OUTPUTS</span></span>

### <span data-ttu-id="b27df-122">Microsoft. Azure. commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b27df-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="b27df-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b27df-123">NOTES</span></span>

## <span data-ttu-id="b27df-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b27df-124">RELATED LINKS</span></span>
