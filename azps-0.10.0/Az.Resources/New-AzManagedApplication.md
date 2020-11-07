---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: a34754e0032f2dc8b833eb6b03de6e97ab5486fe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843362"
---
# <span data-ttu-id="a4be9-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="a4be9-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="a4be9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4be9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4be9-103">Azure-felügyelt alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4be9-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="a4be9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4be9-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4be9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4be9-105">DESCRIPTION</span></span>
<span data-ttu-id="a4be9-106">A **New-AzManagedApplication** parancsmag egy Azure felügyelt alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4be9-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="a4be9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4be9-107">EXAMPLES</span></span>

### <span data-ttu-id="a4be9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a4be9-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="a4be9-109">A parancs felügyelt alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4be9-109">This command creates a managed application</span></span>

## <span data-ttu-id="a4be9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4be9-110">PARAMETERS</span></span>

### <span data-ttu-id="a4be9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a4be9-111">-ApiVersion</span></span>
<span data-ttu-id="a4be9-112">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4be9-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a4be9-113">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a4be9-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a4be9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4be9-114">-DefaultProfile</span></span>
<span data-ttu-id="a4be9-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4be9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4be9-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="a4be9-116">-Kind</span></span>
<span data-ttu-id="a4be9-117">A felügyelt alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="a4be9-117">The managed application kind.</span></span>
<span data-ttu-id="a4be9-118">A piactér vagy a servicecatalog egyike</span><span class="sxs-lookup"><span data-stu-id="a4be9-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="a4be9-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="a4be9-119">-Location</span></span>
<span data-ttu-id="a4be9-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a4be9-120">The resource location.</span></span>

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

### <span data-ttu-id="a4be9-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a4be9-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="a4be9-122">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4be9-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="a4be9-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4be9-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="a4be9-124">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4be9-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="a4be9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4be9-125">-Name</span></span>
<span data-ttu-id="a4be9-126">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="a4be9-126">The managed application name.</span></span>

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

### <span data-ttu-id="a4be9-127">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="a4be9-127">-Parameter</span></span>
<span data-ttu-id="a4be9-128">A felügyelt alkalmazás paramétereinek formázott karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="a4be9-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="a4be9-129">Ez lehet az elérési út a paramétereket tartalmazó fájlnév vagy URI-azonosítók, illetve a paraméterek karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="a4be9-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="a4be9-130">-Terv</span><span class="sxs-lookup"><span data-stu-id="a4be9-130">-Plan</span></span>
<span data-ttu-id="a4be9-131">Egy kivonatoló táblázat, amely A felügyelt alkalmazási terv tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a4be9-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="a4be9-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="a4be9-132">-Pre</span></span>
<span data-ttu-id="a4be9-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a4be9-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a4be9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4be9-134">-ResourceGroupName</span></span>
<span data-ttu-id="a4be9-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4be9-135">The resource group name.</span></span>

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

### <span data-ttu-id="a4be9-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="a4be9-136">-Tag</span></span>
<span data-ttu-id="a4be9-137">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a4be9-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a4be9-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4be9-138">-Confirm</span></span>
<span data-ttu-id="a4be9-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4be9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4be9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4be9-140">-WhatIf</span></span>
<span data-ttu-id="a4be9-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4be9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4be9-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4be9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4be9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4be9-143">CommonParameters</span></span>
<span data-ttu-id="a4be9-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4be9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4be9-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4be9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4be9-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4be9-146">INPUTS</span></span>

### <span data-ttu-id="a4be9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a4be9-147">System.String</span></span>

### <span data-ttu-id="a4be9-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a4be9-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a4be9-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4be9-149">OUTPUTS</span></span>

### <span data-ttu-id="a4be9-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a4be9-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a4be9-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4be9-151">NOTES</span></span>

## <span data-ttu-id="a4be9-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4be9-152">RELATED LINKS</span></span>
