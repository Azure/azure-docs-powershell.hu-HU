---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017662"
---
# <span data-ttu-id="2df40-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="2df40-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="2df40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2df40-102">SYNOPSIS</span></span>
<span data-ttu-id="2df40-103">Azure-felügyelt alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2df40-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="2df40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2df40-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df40-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2df40-105">DESCRIPTION</span></span>
<span data-ttu-id="2df40-106">A **New-AzManagedApplication** parancsmag egy Azure felügyelt alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2df40-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="2df40-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2df40-107">EXAMPLES</span></span>

### <span data-ttu-id="2df40-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2df40-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="2df40-109">A parancs felügyelt alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2df40-109">This command creates a managed application</span></span>

## <span data-ttu-id="2df40-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2df40-110">PARAMETERS</span></span>

### <span data-ttu-id="2df40-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2df40-111">-ApiVersion</span></span>
<span data-ttu-id="2df40-112">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2df40-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2df40-113">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2df40-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2df40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df40-114">-DefaultProfile</span></span>
<span data-ttu-id="2df40-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2df40-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="2df40-116">-Kind</span></span>
<span data-ttu-id="2df40-117">A felügyelt alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="2df40-117">The managed application kind.</span></span>
<span data-ttu-id="2df40-118">A piactér vagy a servicecatalog egyike</span><span class="sxs-lookup"><span data-stu-id="2df40-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="2df40-119">-Location</span></span>
<span data-ttu-id="2df40-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="2df40-120">The resource location.</span></span>

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

### <span data-ttu-id="2df40-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2df40-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="2df40-122">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2df40-122">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df40-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="2df40-124">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2df40-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2df40-125">-Name</span></span>
<span data-ttu-id="2df40-126">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="2df40-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-127">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="2df40-127">-Parameter</span></span>
<span data-ttu-id="2df40-128">A felügyelt alkalmazás paramétereinek formázott karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="2df40-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="2df40-129">Ez lehet az elérési út a paramétereket tartalmazó fájlnév vagy URI-azonosítók, illetve a paraméterek karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="2df40-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-130">-Terv</span><span class="sxs-lookup"><span data-stu-id="2df40-130">-Plan</span></span>
<span data-ttu-id="2df40-131">Egy kivonatoló táblázat, amely A felügyelt alkalmazási terv tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2df40-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="2df40-132">-Pre</span></span>
<span data-ttu-id="2df40-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2df40-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2df40-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df40-134">-ResourceGroupName</span></span>
<span data-ttu-id="2df40-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2df40-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="2df40-136">-Tag</span></span>
<span data-ttu-id="2df40-137">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2df40-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df40-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2df40-138">-Confirm</span></span>
<span data-ttu-id="2df40-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2df40-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df40-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df40-140">-WhatIf</span></span>
<span data-ttu-id="2df40-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2df40-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df40-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2df40-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df40-143">CommonParameters</span></span>
<span data-ttu-id="2df40-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2df40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df40-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2df40-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df40-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2df40-146">INPUTS</span></span>

### <span data-ttu-id="2df40-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2df40-147">System.String</span></span>

### <span data-ttu-id="2df40-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2df40-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2df40-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2df40-149">OUTPUTS</span></span>

### <span data-ttu-id="2df40-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2df40-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2df40-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2df40-151">NOTES</span></span>

## <span data-ttu-id="2df40-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2df40-152">RELATED LINKS</span></span>
