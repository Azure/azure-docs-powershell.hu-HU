---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381455"
---
# <span data-ttu-id="942c3-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="942c3-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="942c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="942c3-102">SYNOPSIS</span></span>
<span data-ttu-id="942c3-103">Annak ellenőrzése, hogy használható-e a konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="942c3-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="942c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="942c3-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="942c3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="942c3-105">DESCRIPTION</span></span>
<span data-ttu-id="942c3-106">Annak ellenőrzése, hogy használható-e a konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="942c3-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="942c3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="942c3-107">EXAMPLES</span></span>

### <span data-ttu-id="942c3-108">1. példa: Az appkonfigurációs áruház nevének elérhetőségének tesztelése</span><span class="sxs-lookup"><span data-stu-id="942c3-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="942c3-109">Ez a parancs teszteli az alkalmazáskonfigurációs áruház nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="942c3-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="942c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="942c3-110">PARAMETERS</span></span>

### <span data-ttu-id="942c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942c3-111">-DefaultProfile</span></span>
<span data-ttu-id="942c3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="942c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="942c3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="942c3-113">-Name</span></span>
<span data-ttu-id="942c3-114">Az elérhetőség ellenőrzésére vonatkozó név.</span><span class="sxs-lookup"><span data-stu-id="942c3-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="942c3-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="942c3-115">-SubscriptionId</span></span>
<span data-ttu-id="942c3-116">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="942c3-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="942c3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="942c3-117">-Confirm</span></span>
<span data-ttu-id="942c3-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="942c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="942c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="942c3-119">-WhatIf</span></span>
<span data-ttu-id="942c3-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="942c3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="942c3-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="942c3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="942c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942c3-122">CommonParameters</span></span>
<span data-ttu-id="942c3-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="942c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942c3-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="942c3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942c3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="942c3-125">INPUTS</span></span>

## <span data-ttu-id="942c3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="942c3-126">OUTPUTS</span></span>

### <span data-ttu-id="942c3-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="942c3-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="942c3-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="942c3-128">NOTES</span></span>

<span data-ttu-id="942c3-129">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="942c3-129">ALIASES</span></span>

## <span data-ttu-id="942c3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="942c3-130">RELATED LINKS</span></span>

