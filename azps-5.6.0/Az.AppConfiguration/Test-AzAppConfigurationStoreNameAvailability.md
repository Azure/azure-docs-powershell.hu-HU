---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: 87d19475896138ee51a31694f707c1839f839ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924273"
---
# <span data-ttu-id="aaee9-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="aaee9-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="aaee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaee9-102">SYNOPSIS</span></span>
<span data-ttu-id="aaee9-103">Annak ellenőrzése, hogy használható-e a konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="aaee9-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="aaee9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aaee9-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aaee9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aaee9-105">DESCRIPTION</span></span>
<span data-ttu-id="aaee9-106">Annak ellenőrzése, hogy használható-e a konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="aaee9-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="aaee9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aaee9-107">EXAMPLES</span></span>

### <span data-ttu-id="aaee9-108">1. példa: Az appkonfigurációs áruház nevének elérhetőségének tesztelése</span><span class="sxs-lookup"><span data-stu-id="aaee9-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="aaee9-109">Ez a parancs teszteli az alkalmazáskonfigurációs áruház nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="aaee9-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="aaee9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaee9-110">PARAMETERS</span></span>

### <span data-ttu-id="aaee9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaee9-111">-DefaultProfile</span></span>
<span data-ttu-id="aaee9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaee9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaee9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="aaee9-113">-Name</span></span>
<span data-ttu-id="aaee9-114">Az elérhetőség ellenőrzésére vonatkozó név.</span><span class="sxs-lookup"><span data-stu-id="aaee9-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="aaee9-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaee9-115">-SubscriptionId</span></span>
<span data-ttu-id="aaee9-116">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aaee9-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="aaee9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaee9-117">-Confirm</span></span>
<span data-ttu-id="aaee9-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aaee9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaee9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaee9-119">-WhatIf</span></span>
<span data-ttu-id="aaee9-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aaee9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaee9-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aaee9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaee9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaee9-122">CommonParameters</span></span>
<span data-ttu-id="aaee9-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaee9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaee9-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaee9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaee9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaee9-125">INPUTS</span></span>

## <span data-ttu-id="aaee9-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaee9-126">OUTPUTS</span></span>

### <span data-ttu-id="aaee9-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="aaee9-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="aaee9-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aaee9-128">NOTES</span></span>

<span data-ttu-id="aaee9-129">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aaee9-129">ALIASES</span></span>

## <span data-ttu-id="aaee9-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaee9-130">RELATED LINKS</span></span>

