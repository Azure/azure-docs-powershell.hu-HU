---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 9507271fe283277c212e4ed8d4117483a2797857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927442"
---
# <span data-ttu-id="812c1-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="812c1-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="812c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="812c1-102">SYNOPSIS</span></span>
<span data-ttu-id="812c1-103">Annak ellenőrzése, hogy elérhető-e egy erőforrásnév.</span><span class="sxs-lookup"><span data-stu-id="812c1-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="812c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="812c1-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="812c1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="812c1-105">DESCRIPTION</span></span>
<span data-ttu-id="812c1-106">Annak ellenőrzése, hogy elérhető-e egy erőforrásnév.</span><span class="sxs-lookup"><span data-stu-id="812c1-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="812c1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="812c1-107">EXAMPLES</span></span>

### <span data-ttu-id="812c1-108">1. példa: Annak ellenőrzése, hogy elérhető-e egy erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="812c1-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="812c1-109">A parancs ellenőrzi, hogy elérhető-e egy erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="812c1-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="812c1-110">2. példa: Annak ellenőrzése, hogy elérhető-e egy erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="812c1-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="812c1-111">A parancs ellenőrzi, hogy elérhető-e egy erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="812c1-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="812c1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="812c1-112">PARAMETERS</span></span>

### <span data-ttu-id="812c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812c1-113">-DefaultProfile</span></span>
<span data-ttu-id="812c1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="812c1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="812c1-115">-Location</span><span class="sxs-lookup"><span data-stu-id="812c1-115">-Location</span></span>
<span data-ttu-id="812c1-116">Hely neve.</span><span class="sxs-lookup"><span data-stu-id="812c1-116">Location Name.</span></span>

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

### <span data-ttu-id="812c1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="812c1-117">-Name</span></span>
<span data-ttu-id="812c1-118">Beállítja vagy ellenőrzi a nevet.</span><span class="sxs-lookup"><span data-stu-id="812c1-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="812c1-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="812c1-119">-SubscriptionId</span></span>
<span data-ttu-id="812c1-120">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="812c1-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="812c1-121">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="812c1-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="812c1-122">-Type</span><span class="sxs-lookup"><span data-stu-id="812c1-122">-Type</span></span>
<span data-ttu-id="812c1-123">Beállítja vagy beállítja az ellenőrizni szükséges erőforrás típusát.</span><span class="sxs-lookup"><span data-stu-id="812c1-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="812c1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="812c1-124">-Confirm</span></span>
<span data-ttu-id="812c1-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="812c1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="812c1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="812c1-126">-WhatIf</span></span>
<span data-ttu-id="812c1-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="812c1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="812c1-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="812c1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="812c1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812c1-129">CommonParameters</span></span>
<span data-ttu-id="812c1-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="812c1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812c1-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="812c1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812c1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="812c1-132">INPUTS</span></span>

## <span data-ttu-id="812c1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="812c1-133">OUTPUTS</span></span>

### <span data-ttu-id="812c1-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="812c1-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="812c1-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="812c1-135">NOTES</span></span>

<span data-ttu-id="812c1-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="812c1-136">ALIASES</span></span>

## <span data-ttu-id="812c1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="812c1-137">RELATED LINKS</span></span>

