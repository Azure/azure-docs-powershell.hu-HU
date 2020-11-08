---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017980"
---
# <span data-ttu-id="bd5fc-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="bd5fc-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="bd5fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5fc-103">Ellenőrzi, hogy elérhető-e a konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="bd5fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd5fc-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd5fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd5fc-105">DESCRIPTION</span></span>
<span data-ttu-id="bd5fc-106">Ellenőrzi, hogy elérhető-e a konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="bd5fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bd5fc-107">EXAMPLES</span></span>

### <span data-ttu-id="bd5fc-108">1. példa: az App Configuration Store-név elérhetőségének tesztelése</span><span class="sxs-lookup"><span data-stu-id="bd5fc-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="bd5fc-109">Ez a parancs az App Configuration Store-név elérhetőségét teszteli.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="bd5fc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd5fc-110">PARAMETERS</span></span>

### <span data-ttu-id="bd5fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd5fc-111">-DefaultProfile</span></span>
<span data-ttu-id="bd5fc-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd5fc-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd5fc-113">-Name</span></span>
<span data-ttu-id="bd5fc-114">Az elérhetőség ellenőrzésére szolgáló név.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="bd5fc-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd5fc-115">-SubscriptionId</span></span>
<span data-ttu-id="bd5fc-116">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="bd5fc-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bd5fc-117">-Confirm</span></span>
<span data-ttu-id="bd5fc-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd5fc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd5fc-119">-WhatIf</span></span>
<span data-ttu-id="bd5fc-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd5fc-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd5fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd5fc-122">CommonParameters</span></span>
<span data-ttu-id="bd5fc-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd5fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd5fc-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bd5fc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd5fc-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd5fc-125">INPUTS</span></span>

## <span data-ttu-id="bd5fc-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd5fc-126">OUTPUTS</span></span>

### <span data-ttu-id="bd5fc-127">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. modellek. Api20200601. INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="bd5fc-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="bd5fc-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd5fc-128">NOTES</span></span>

<span data-ttu-id="bd5fc-129">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bd5fc-129">ALIASES</span></span>

## <span data-ttu-id="bd5fc-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd5fc-130">RELATED LINKS</span></span>

