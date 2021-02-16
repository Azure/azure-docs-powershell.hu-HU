---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145170"
---
# <span data-ttu-id="b0af2-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b0af2-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="b0af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0af2-102">SYNOPSIS</span></span>
<span data-ttu-id="b0af2-103">Annak ellenőrzése, hogy elérhető-e egy erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b0af2-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="b0af2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0af2-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0af2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0af2-105">DESCRIPTION</span></span>
<span data-ttu-id="b0af2-106">Annak ellenőrzése, hogy elérhető-e egy erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b0af2-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="b0af2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0af2-107">EXAMPLES</span></span>

### <span data-ttu-id="b0af2-108">1. példa: Annak ellenőrzése, hogy elérhető-e egy erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b0af2-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="b0af2-109">A parancs ellenőrzi, hogy elérhető-e egy erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b0af2-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="b0af2-110">2. példa: Annak ellenőrzése, hogy elérhető-e egy erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b0af2-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="b0af2-111">A parancs ellenőrzi, hogy elérhető-e egy erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b0af2-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="b0af2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0af2-112">PARAMETERS</span></span>

### <span data-ttu-id="b0af2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0af2-113">-DefaultProfile</span></span>
<span data-ttu-id="b0af2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0af2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0af2-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b0af2-115">-Location</span></span>
<span data-ttu-id="b0af2-116">Hely neve.</span><span class="sxs-lookup"><span data-stu-id="b0af2-116">Location Name.</span></span>

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

### <span data-ttu-id="b0af2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b0af2-117">-Name</span></span>
<span data-ttu-id="b0af2-118">Beállítja vagy ellenőrzi a nevet.</span><span class="sxs-lookup"><span data-stu-id="b0af2-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="b0af2-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0af2-119">-SubscriptionId</span></span>
<span data-ttu-id="b0af2-120">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="b0af2-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0af2-121">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="b0af2-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b0af2-122">-Type</span><span class="sxs-lookup"><span data-stu-id="b0af2-122">-Type</span></span>
<span data-ttu-id="b0af2-123">Beállítja vagy beállítja az ellenőrizni szükséges erőforrás típusát.</span><span class="sxs-lookup"><span data-stu-id="b0af2-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="b0af2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0af2-124">-Confirm</span></span>
<span data-ttu-id="b0af2-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0af2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0af2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0af2-126">-WhatIf</span></span>
<span data-ttu-id="b0af2-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0af2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0af2-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0af2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0af2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0af2-129">CommonParameters</span></span>
<span data-ttu-id="b0af2-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0af2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0af2-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0af2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0af2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0af2-132">INPUTS</span></span>

## <span data-ttu-id="b0af2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0af2-133">OUTPUTS</span></span>

### <span data-ttu-id="b0af2-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="b0af2-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="b0af2-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0af2-135">NOTES</span></span>

<span data-ttu-id="b0af2-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b0af2-136">ALIASES</span></span>

## <span data-ttu-id="b0af2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0af2-137">RELATED LINKS</span></span>

