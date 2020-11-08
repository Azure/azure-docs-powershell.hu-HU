---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181648"
---
# <span data-ttu-id="f8acb-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f8acb-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="f8acb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8acb-102">SYNOPSIS</span></span>
<span data-ttu-id="f8acb-103">Regisztrálja az erőforrás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f8acb-103">Register configuration for resource.</span></span>

## <span data-ttu-id="f8acb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8acb-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8acb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8acb-105">DESCRIPTION</span></span>
<span data-ttu-id="f8acb-106">Az erőforrás karbantartási konfigurációjának nyilvántartása.</span><span class="sxs-lookup"><span data-stu-id="f8acb-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="f8acb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f8acb-107">EXAMPLES</span></span>

### <span data-ttu-id="f8acb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f8acb-108">Example 1</span></span>
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

<span data-ttu-id="f8acb-109">A dedikált állomás karbantartási beállításainak nyilvántartása.</span><span class="sxs-lookup"><span data-stu-id="f8acb-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="f8acb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8acb-110">PARAMETERS</span></span>

### <span data-ttu-id="f8acb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8acb-111">-AsJob</span></span>
<span data-ttu-id="f8acb-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f8acb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8acb-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f8acb-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="f8acb-114">A konfigurációs hozzárendelés nevének egyeznie kell a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="f8acb-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="f8acb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8acb-115">-DefaultProfile</span></span>
<span data-ttu-id="f8acb-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8acb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8acb-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="f8acb-117">-Location</span></span>
<span data-ttu-id="f8acb-118">Az erőforrás helyének szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="f8acb-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="f8acb-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f8acb-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="f8acb-120">A teljes mértékben minősített MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f8acb-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="f8acb-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="f8acb-121">-ProviderName</span></span>
<span data-ttu-id="f8acb-122">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="f8acb-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="f8acb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8acb-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8acb-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8acb-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="f8acb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8acb-125">-ResourceId</span></span>
<span data-ttu-id="f8acb-126">A konfigurációs hozzárendelés nevének egyeznie kell a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="f8acb-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="f8acb-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f8acb-127">-ResourceName</span></span>
<span data-ttu-id="f8acb-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f8acb-128">The resource name.</span></span>

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

### <span data-ttu-id="f8acb-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="f8acb-129">-ResourceParentName</span></span>
<span data-ttu-id="f8acb-130">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f8acb-130">The parent resource name.</span></span>

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

### <span data-ttu-id="f8acb-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="f8acb-131">-ResourceParentType</span></span>
<span data-ttu-id="f8acb-132">A szülő-erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="f8acb-132">The parent resource type.</span></span>

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

### <span data-ttu-id="f8acb-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f8acb-133">-ResourceType</span></span>
<span data-ttu-id="f8acb-134">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="f8acb-134">The resource type.</span></span>

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

### <span data-ttu-id="f8acb-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f8acb-135">-Confirm</span></span>
<span data-ttu-id="f8acb-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f8acb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8acb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8acb-137">-WhatIf</span></span>
<span data-ttu-id="f8acb-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f8acb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8acb-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8acb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8acb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8acb-140">CommonParameters</span></span>
<span data-ttu-id="f8acb-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8acb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8acb-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f8acb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8acb-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8acb-143">INPUTS</span></span>

### <span data-ttu-id="f8acb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f8acb-144">System.String</span></span>

## <span data-ttu-id="f8acb-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8acb-145">OUTPUTS</span></span>

### <span data-ttu-id="f8acb-146">Microsoft. Azure. commands. Maintenance. models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f8acb-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="f8acb-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8acb-147">NOTES</span></span>

## <span data-ttu-id="f8acb-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8acb-148">RELATED LINKS</span></span>
