---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: f0c5c52773d5750b86ce82d696e9130df76f4700
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014222"
---
# <span data-ttu-id="24a1a-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24a1a-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="24a1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="24a1a-103">Regisztrálja az erőforrás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="24a1a-103">Register configuration for resource.</span></span>

## <span data-ttu-id="24a1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a1a-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24a1a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="24a1a-106">Az erőforrás karbantartási konfigurációjának nyilvántartása.</span><span class="sxs-lookup"><span data-stu-id="24a1a-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="24a1a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24a1a-107">EXAMPLES</span></span>

### <span data-ttu-id="24a1a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24a1a-108">Example 1</span></span>
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

<span data-ttu-id="24a1a-109">Regisztrálja a didicated-állomás karbantartási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="24a1a-109">Register maintenance configuration for didicated host.</span></span>

## <span data-ttu-id="24a1a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a1a-110">PARAMETERS</span></span>

### <span data-ttu-id="24a1a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24a1a-111">-AsJob</span></span>
<span data-ttu-id="24a1a-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="24a1a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24a1a-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="24a1a-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="24a1a-114">A konfigurációs hozzárendelés nevének egyeznie kell a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="24a1a-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="24a1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a1a-115">-DefaultProfile</span></span>
<span data-ttu-id="24a1a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24a1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a1a-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="24a1a-117">-Location</span></span>
<span data-ttu-id="24a1a-118">Az erőforrás helyének szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="24a1a-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="24a1a-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="24a1a-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="24a1a-120">A teljes mértékben minősített MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="24a1a-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="24a1a-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="24a1a-121">-ProviderName</span></span>
<span data-ttu-id="24a1a-122">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="24a1a-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="24a1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="24a1a-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="24a1a-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="24a1a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24a1a-125">-ResourceId</span></span>
<span data-ttu-id="24a1a-126">A konfigurációs hozzárendelés nevének egyeznie kell a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="24a1a-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="24a1a-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="24a1a-127">-ResourceName</span></span>
<span data-ttu-id="24a1a-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="24a1a-128">The resource name.</span></span>

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

### <span data-ttu-id="24a1a-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="24a1a-129">-ResourceParentName</span></span>
<span data-ttu-id="24a1a-130">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="24a1a-130">The parent resource name.</span></span>

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

### <span data-ttu-id="24a1a-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="24a1a-131">-ResourceParentType</span></span>
<span data-ttu-id="24a1a-132">A szülő-erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="24a1a-132">The parent resource type.</span></span>

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

### <span data-ttu-id="24a1a-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="24a1a-133">-ResourceType</span></span>
<span data-ttu-id="24a1a-134">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="24a1a-134">The resource type.</span></span>

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

### <span data-ttu-id="24a1a-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24a1a-135">-Confirm</span></span>
<span data-ttu-id="24a1a-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24a1a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a1a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a1a-137">-WhatIf</span></span>
<span data-ttu-id="24a1a-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24a1a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a1a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24a1a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a1a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a1a-140">CommonParameters</span></span>
<span data-ttu-id="24a1a-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a1a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a1a-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24a1a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a1a-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a1a-143">INPUTS</span></span>

### <span data-ttu-id="24a1a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="24a1a-144">System.String</span></span>

## <span data-ttu-id="24a1a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a1a-145">OUTPUTS</span></span>

### <span data-ttu-id="24a1a-146">Microsoft. Azure. commands. Maintenance. models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24a1a-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="24a1a-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a1a-147">NOTES</span></span>

## <span data-ttu-id="24a1a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a1a-148">RELATED LINKS</span></span>
