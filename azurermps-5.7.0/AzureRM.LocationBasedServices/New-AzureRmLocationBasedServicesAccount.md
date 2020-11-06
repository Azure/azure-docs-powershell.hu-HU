---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493781"
---
# <span data-ttu-id="9c82d-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9c82d-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="9c82d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c82d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c82d-103">Hely-és szolgáltatási fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9c82d-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c82d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c82d-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c82d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c82d-105">DESCRIPTION</span></span>
<span data-ttu-id="9c82d-106">A **New-AzureRmLocationBasedServicesAccount** parancsmag a megadott SKU-hoz létrehoz egy helyet-alapú szolgáltatási fiókot.</span><span class="sxs-lookup"><span data-stu-id="9c82d-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="9c82d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9c82d-107">EXAMPLES</span></span>

### <span data-ttu-id="9c82d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c82d-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="9c82d-109">Új helyekre épülő szolgáltatások nevű fiókot hoz létre a MyAccount nevű erőforrás-MyResourceGroup az SKU S0 és egy címkével.</span><span class="sxs-lookup"><span data-stu-id="9c82d-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="9c82d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c82d-110">PARAMETERS</span></span>

### <span data-ttu-id="9c82d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c82d-111">-DefaultProfile</span></span>
<span data-ttu-id="9c82d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c82d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c82d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9c82d-113">-Force</span></span>
<span data-ttu-id="9c82d-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c82d-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c82d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c82d-115">-Name</span></span>
<span data-ttu-id="9c82d-116">A helyeken nyugvó szolgáltatások fiókjának neve.</span><span class="sxs-lookup"><span data-stu-id="9c82d-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c82d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c82d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9c82d-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9c82d-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c82d-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9c82d-119">-SkuName</span></span>
<span data-ttu-id="9c82d-120">A helyeken nyugvó szolgáltatások fiók SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="9c82d-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="9c82d-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9c82d-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c82d-122">S0</span><span class="sxs-lookup"><span data-stu-id="9c82d-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c82d-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="9c82d-123">-Tag</span></span>
<span data-ttu-id="9c82d-124">A helyeken nyugvó Services-fiók címkéi.</span><span class="sxs-lookup"><span data-stu-id="9c82d-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c82d-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c82d-125">-Confirm</span></span>
<span data-ttu-id="9c82d-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c82d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c82d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c82d-127">-WhatIf</span></span>
<span data-ttu-id="9c82d-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c82d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c82d-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c82d-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c82d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c82d-130">CommonParameters</span></span>
<span data-ttu-id="9c82d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c82d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c82d-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c82d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c82d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c82d-133">INPUTS</span></span>

### <span data-ttu-id="9c82d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9c82d-134">System.String</span></span>

## <span data-ttu-id="9c82d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c82d-135">OUTPUTS</span></span>

### <span data-ttu-id="9c82d-136">Microsoft. Azure. Command. LocationBasedServices. models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9c82d-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="9c82d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c82d-137">NOTES</span></span>

<span data-ttu-id="9c82d-138">A helyekre épülő szolgáltatások fiók létrehozásakor figyelmeztetést kell kérni a feltételről (lásd: https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="9c82d-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="9c82d-139">A-Force paraméter a fogalmak átvételének jelzésére használható.</span><span class="sxs-lookup"><span data-stu-id="9c82d-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="9c82d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c82d-140">RELATED LINKS</span></span>
