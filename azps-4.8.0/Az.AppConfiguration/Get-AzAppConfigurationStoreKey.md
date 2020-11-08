---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180667"
---
# <span data-ttu-id="2ae95-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="2ae95-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="2ae95-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ae95-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae95-103">A megadott konfigurációs tároló elérési kulcsát sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="2ae95-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="2ae95-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ae95-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ae95-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ae95-105">DESCRIPTION</span></span>
<span data-ttu-id="2ae95-106">A megadott konfigurációs tároló elérési kulcsát sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="2ae95-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="2ae95-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2ae95-107">EXAMPLES</span></span>

### <span data-ttu-id="2ae95-108">1. példa: az App konfigurációs tárolójának összes áruházi kulcsának listázása</span><span class="sxs-lookup"><span data-stu-id="2ae95-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="2ae95-109">Ez a parancs felsorolja az App Configuration Store áruházának összes kulcsát.</span><span class="sxs-lookup"><span data-stu-id="2ae95-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="2ae95-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ae95-110">PARAMETERS</span></span>

### <span data-ttu-id="2ae95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae95-111">-DefaultProfile</span></span>
<span data-ttu-id="2ae95-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ae95-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ae95-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ae95-113">-Name</span></span>
<span data-ttu-id="2ae95-114">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="2ae95-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="2ae95-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ae95-115">-ResourceGroupName</span></span>
<span data-ttu-id="2ae95-116">Annak az erőforráscsoportnek a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="2ae95-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="2ae95-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ae95-117">-SubscriptionId</span></span>
<span data-ttu-id="2ae95-118">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2ae95-118">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae95-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ae95-119">-Confirm</span></span>
<span data-ttu-id="2ae95-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ae95-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae95-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae95-121">-WhatIf</span></span>
<span data-ttu-id="2ae95-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ae95-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ae95-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ae95-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ae95-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae95-124">CommonParameters</span></span>
<span data-ttu-id="2ae95-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ae95-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae95-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2ae95-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae95-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ae95-127">INPUTS</span></span>

## <span data-ttu-id="2ae95-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ae95-128">OUTPUTS</span></span>

### <span data-ttu-id="2ae95-129">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. modellek. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="2ae95-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="2ae95-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ae95-130">NOTES</span></span>

<span data-ttu-id="2ae95-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2ae95-131">ALIASES</span></span>

## <span data-ttu-id="2ae95-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ae95-132">RELATED LINKS</span></span>

