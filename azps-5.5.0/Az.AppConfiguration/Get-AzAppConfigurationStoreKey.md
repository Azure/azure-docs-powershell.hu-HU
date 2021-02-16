---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162571"
---
# <span data-ttu-id="d8ce3-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="d8ce3-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="d8ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ce3-103">A megadott konfigurációs tároló hozzáférési kulcsát sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="d8ce3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8ce3-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8ce3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ce3-106">A megadott konfigurációs tároló hozzáférési kulcsát sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="d8ce3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="d8ce3-108">1. példa: Egy alkalmazáskonfigurációs áruház összes áruházkulcsának felsorolása</span><span class="sxs-lookup"><span data-stu-id="d8ce3-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="d8ce3-109">Ez a parancs felsorolja az alkalmazáskonfigurációs áruház összes áruházkulcsát.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="d8ce3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8ce3-110">PARAMETERS</span></span>

### <span data-ttu-id="d8ce3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ce3-111">-DefaultProfile</span></span>
<span data-ttu-id="d8ce3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8ce3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d8ce3-113">-Name</span></span>
<span data-ttu-id="d8ce3-114">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="d8ce3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ce3-115">-ResourceGroupName</span></span>
<span data-ttu-id="d8ce3-116">Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="d8ce3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8ce3-117">-SubscriptionId</span></span>
<span data-ttu-id="d8ce3-118">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-118">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="d8ce3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8ce3-119">-Confirm</span></span>
<span data-ttu-id="d8ce3-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8ce3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ce3-121">-WhatIf</span></span>
<span data-ttu-id="d8ce3-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8ce3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8ce3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ce3-124">CommonParameters</span></span>
<span data-ttu-id="d8ce3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ce3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ce3-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8ce3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ce3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8ce3-127">INPUTS</span></span>

## <span data-ttu-id="d8ce3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8ce3-128">OUTPUTS</span></span>

### <span data-ttu-id="d8ce3-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="d8ce3-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="d8ce3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8ce3-130">NOTES</span></span>

<span data-ttu-id="d8ce3-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d8ce3-131">ALIASES</span></span>

## <span data-ttu-id="d8ce3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8ce3-132">RELATED LINKS</span></span>

