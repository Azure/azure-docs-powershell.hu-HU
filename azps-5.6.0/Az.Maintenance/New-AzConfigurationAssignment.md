---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 993c1968d144a5a1a56a0bd3dff46a9920a90264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012917"
---
# <span data-ttu-id="39aea-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="39aea-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="39aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39aea-102">SYNOPSIS</span></span>
<span data-ttu-id="39aea-103">Konfiguráció regisztrálása erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="39aea-103">Register configuration for resource.</span></span>

## <span data-ttu-id="39aea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39aea-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39aea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39aea-105">DESCRIPTION</span></span>
<span data-ttu-id="39aea-106">Erőforrás karbantartási konfigurációjának regisztrálása</span><span class="sxs-lookup"><span data-stu-id="39aea-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="39aea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39aea-107">EXAMPLES</span></span>

### <span data-ttu-id="39aea-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="39aea-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="39aea-109">Regisztrálja a karbantartási konfigurációt a dedikált állomáshoz.</span><span class="sxs-lookup"><span data-stu-id="39aea-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="39aea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39aea-110">PARAMETERS</span></span>

### <span data-ttu-id="39aea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39aea-111">-AsJob</span></span>
<span data-ttu-id="39aea-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="39aea-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39aea-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="39aea-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="39aea-114">A konfigurációs hozzárendelés nevének meg kell egyeznie a MaintenanceConfigurationName értéknek.</span><span class="sxs-lookup"><span data-stu-id="39aea-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="39aea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39aea-115">-DefaultProfile</span></span>
<span data-ttu-id="39aea-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39aea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39aea-117">-Location</span><span class="sxs-lookup"><span data-stu-id="39aea-117">-Location</span></span>
<span data-ttu-id="39aea-118">Az erőforrás szóközök nélküli helye.</span><span class="sxs-lookup"><span data-stu-id="39aea-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="39aea-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="39aea-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="39aea-120">A teljesen minősített MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="39aea-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="39aea-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="39aea-121">-ProviderName</span></span>
<span data-ttu-id="39aea-122">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="39aea-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="39aea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39aea-123">-ResourceGroupName</span></span>
<span data-ttu-id="39aea-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39aea-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="39aea-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39aea-125">-ResourceId</span></span>
<span data-ttu-id="39aea-126">A konfigurációs hozzárendelés nevének meg kell egyeznie a MaintenanceConfigurationName értéknek.</span><span class="sxs-lookup"><span data-stu-id="39aea-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="39aea-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="39aea-127">-ResourceName</span></span>
<span data-ttu-id="39aea-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="39aea-128">The resource name.</span></span>

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

### <span data-ttu-id="39aea-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="39aea-129">-ResourceParentName</span></span>
<span data-ttu-id="39aea-130">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="39aea-130">The parent resource name.</span></span>

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

### <span data-ttu-id="39aea-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="39aea-131">-ResourceParentType</span></span>
<span data-ttu-id="39aea-132">A szülőerőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="39aea-132">The parent resource type.</span></span>

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

### <span data-ttu-id="39aea-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="39aea-133">-ResourceType</span></span>
<span data-ttu-id="39aea-134">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="39aea-134">The resource type.</span></span>

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

### <span data-ttu-id="39aea-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39aea-135">-Confirm</span></span>
<span data-ttu-id="39aea-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="39aea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39aea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39aea-137">-WhatIf</span></span>
<span data-ttu-id="39aea-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="39aea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39aea-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39aea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39aea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39aea-140">CommonParameters</span></span>
<span data-ttu-id="39aea-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39aea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39aea-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39aea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39aea-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39aea-143">INPUTS</span></span>

### <span data-ttu-id="39aea-144">System.String</span><span class="sxs-lookup"><span data-stu-id="39aea-144">System.String</span></span>

## <span data-ttu-id="39aea-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39aea-145">OUTPUTS</span></span>

### <span data-ttu-id="39aea-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="39aea-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="39aea-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39aea-147">NOTES</span></span>

## <span data-ttu-id="39aea-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39aea-148">RELATED LINKS</span></span>
