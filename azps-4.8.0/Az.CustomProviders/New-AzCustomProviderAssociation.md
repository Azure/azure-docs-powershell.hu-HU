---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182557"
---
# <span data-ttu-id="da115-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="da115-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="da115-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da115-102">SYNOPSIS</span></span>
<span data-ttu-id="da115-103">Társítás létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="da115-103">Create or update an association.</span></span>

## <span data-ttu-id="da115-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da115-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da115-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da115-105">DESCRIPTION</span></span>
<span data-ttu-id="da115-106">Társítás létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="da115-106">Create or update an association.</span></span>

## <span data-ttu-id="da115-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da115-107">EXAMPLES</span></span>

### <span data-ttu-id="da115-108">Példa 1: egyéni szolgáltatói társítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="da115-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="da115-109">Hozzon létre egy egyéni szolgáltatói társítást, a kapcsolódó cél provioder megfelelően kell konfigurálni a "társítások" útvonalra</span><span class="sxs-lookup"><span data-stu-id="da115-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="da115-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da115-110">PARAMETERS</span></span>

### <span data-ttu-id="da115-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da115-111">-AsJob</span></span>
<span data-ttu-id="da115-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="da115-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da115-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da115-113">-DefaultProfile</span></span>
<span data-ttu-id="da115-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da115-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da115-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da115-115">-Name</span></span>
<span data-ttu-id="da115-116">A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="da115-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da115-117">-Várva</span><span class="sxs-lookup"><span data-stu-id="da115-117">-NoWait</span></span>
<span data-ttu-id="da115-118">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="da115-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da115-119">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="da115-119">-Scope</span></span>
<span data-ttu-id="da115-120">A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="da115-120">The scope of the association.</span></span>
<span data-ttu-id="da115-121">A hatókör bármely érvényes REST-erőforrás-példány lehet.</span><span class="sxs-lookup"><span data-stu-id="da115-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="da115-122">Használja például a "/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}" értéket egy virtuális gép erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="da115-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="da115-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="da115-123">-TargetResourceId</span></span>
<span data-ttu-id="da115-124">A hozzárendelés erőforrásának REST típusú erőforrás-példánya.</span><span class="sxs-lookup"><span data-stu-id="da115-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="da115-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da115-125">-Confirm</span></span>
<span data-ttu-id="da115-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da115-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da115-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da115-127">-WhatIf</span></span>
<span data-ttu-id="da115-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da115-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da115-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da115-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da115-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da115-130">CommonParameters</span></span>
<span data-ttu-id="da115-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da115-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da115-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da115-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da115-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da115-133">INPUTS</span></span>

## <span data-ttu-id="da115-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da115-134">OUTPUTS</span></span>

### <span data-ttu-id="da115-135">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. modellek. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="da115-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="da115-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da115-136">NOTES</span></span>

<span data-ttu-id="da115-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="da115-137">ALIASES</span></span>

## <span data-ttu-id="da115-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da115-138">RELATED LINKS</span></span>

