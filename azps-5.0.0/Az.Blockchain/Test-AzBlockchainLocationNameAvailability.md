---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194128"
---
# <span data-ttu-id="64441-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="64441-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="64441-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64441-102">SYNOPSIS</span></span>
<span data-ttu-id="64441-103">Annak ellenőrzése, hogy elérhető-e az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="64441-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="64441-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64441-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64441-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64441-105">DESCRIPTION</span></span>
<span data-ttu-id="64441-106">Annak ellenőrzése, hogy elérhető-e az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="64441-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="64441-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64441-107">EXAMPLES</span></span>

### <span data-ttu-id="64441-108">Példa 1: annak ellenőrzése, hogy elérhető-e az erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="64441-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="64441-109">A parancs azt ellenőrzi, hogy elérhető-e az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="64441-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="64441-110">2. példa: annak ellenőrzése, hogy elérhető-e az erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="64441-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="64441-111">A parancs azt ellenőrzi, hogy elérhető-e az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="64441-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="64441-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64441-112">PARAMETERS</span></span>

### <span data-ttu-id="64441-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64441-113">-DefaultProfile</span></span>
<span data-ttu-id="64441-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64441-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64441-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="64441-115">-Location</span></span>
<span data-ttu-id="64441-116">Tartózkodási hely neve.</span><span class="sxs-lookup"><span data-stu-id="64441-116">Location Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64441-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64441-117">-Name</span></span>
<span data-ttu-id="64441-118">Beolvassa vagy beállítja az ellenőrizendő nevet.</span><span class="sxs-lookup"><span data-stu-id="64441-118">Gets or sets the name to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64441-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64441-119">-SubscriptionId</span></span>
<span data-ttu-id="64441-120">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="64441-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="64441-121">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="64441-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64441-122">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="64441-122">-Type</span></span>
<span data-ttu-id="64441-123">Az ellenőrizendő erőforrás típusa vagy típusának megadása</span><span class="sxs-lookup"><span data-stu-id="64441-123">Gets or sets the type of the resource to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64441-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64441-124">-Confirm</span></span>
<span data-ttu-id="64441-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64441-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64441-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64441-126">-WhatIf</span></span>
<span data-ttu-id="64441-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64441-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64441-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64441-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64441-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64441-129">CommonParameters</span></span>
<span data-ttu-id="64441-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64441-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64441-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="64441-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64441-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64441-132">INPUTS</span></span>

## <span data-ttu-id="64441-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64441-133">OUTPUTS</span></span>

### <span data-ttu-id="64441-134">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. INameAvailability</span><span class="sxs-lookup"><span data-stu-id="64441-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="64441-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64441-135">NOTES</span></span>

<span data-ttu-id="64441-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="64441-136">ALIASES</span></span>

## <span data-ttu-id="64441-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64441-137">RELATED LINKS</span></span>

