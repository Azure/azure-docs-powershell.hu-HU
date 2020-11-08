---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181643"
---
# <span data-ttu-id="8622b-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="8622b-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="8622b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8622b-102">SYNOPSIS</span></span>
<span data-ttu-id="8622b-103">Az erőforrás-konfiguráció regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="8622b-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="8622b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8622b-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8622b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8622b-105">DESCRIPTION</span></span>
<span data-ttu-id="8622b-106">Az erőforrás-konfiguráció regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="8622b-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="8622b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8622b-107">EXAMPLES</span></span>

### <span data-ttu-id="8622b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8622b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="8622b-109">Az erőforrás-konfiguráció regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="8622b-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="8622b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8622b-110">PARAMETERS</span></span>

### <span data-ttu-id="8622b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8622b-111">-AsJob</span></span>
<span data-ttu-id="8622b-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8622b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8622b-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="8622b-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="8622b-114">A konfiguráció hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="8622b-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="8622b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8622b-115">-DefaultProfile</span></span>
<span data-ttu-id="8622b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8622b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8622b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8622b-117">-Force</span></span>
<span data-ttu-id="8622b-118">Kényszerített eltávolítás megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="8622b-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="8622b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8622b-119">-PassThru</span></span>
<span data-ttu-id="8622b-120">Az eltávolítási művelet állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8622b-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="8622b-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8622b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8622b-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="8622b-122">-ProviderName</span></span>
<span data-ttu-id="8622b-123">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="8622b-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8622b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8622b-124">-ResourceGroupName</span></span>
<span data-ttu-id="8622b-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8622b-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8622b-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8622b-126">-ResourceName</span></span>
<span data-ttu-id="8622b-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8622b-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8622b-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="8622b-128">-ResourceParentName</span></span>
<span data-ttu-id="8622b-129">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8622b-129">The parent resource name.</span></span>

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

### <span data-ttu-id="8622b-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="8622b-130">-ResourceParentType</span></span>
<span data-ttu-id="8622b-131">A szülő-erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="8622b-131">The parent resource type.</span></span>

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

### <span data-ttu-id="8622b-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8622b-132">-ResourceType</span></span>
<span data-ttu-id="8622b-133">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="8622b-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8622b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8622b-134">-Confirm</span></span>
<span data-ttu-id="8622b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8622b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8622b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8622b-136">-WhatIf</span></span>
<span data-ttu-id="8622b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8622b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8622b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8622b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8622b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8622b-139">CommonParameters</span></span>
<span data-ttu-id="8622b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8622b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8622b-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8622b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8622b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8622b-142">INPUTS</span></span>

### <span data-ttu-id="8622b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8622b-143">System.String</span></span>

## <span data-ttu-id="8622b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8622b-144">OUTPUTS</span></span>

### <span data-ttu-id="8622b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8622b-145">System.Boolean</span></span>

## <span data-ttu-id="8622b-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8622b-146">NOTES</span></span>

## <span data-ttu-id="8622b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8622b-147">RELATED LINKS</span></span>
