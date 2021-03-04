---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 32e40bf33ac5f79529f7924b604998c97d004bef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936777"
---
# <span data-ttu-id="a338e-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="a338e-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="a338e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a338e-102">SYNOPSIS</span></span>
<span data-ttu-id="a338e-103">List configurationAssignments for resource.</span><span class="sxs-lookup"><span data-stu-id="a338e-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="a338e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a338e-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a338e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a338e-105">DESCRIPTION</span></span>
<span data-ttu-id="a338e-106">List configurationAssignments for resource.</span><span class="sxs-lookup"><span data-stu-id="a338e-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="a338e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a338e-107">EXAMPLES</span></span>

### <span data-ttu-id="a338e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a338e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="a338e-109">List configurationAssignments for dedicated host.</span><span class="sxs-lookup"><span data-stu-id="a338e-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="a338e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a338e-110">PARAMETERS</span></span>

### <span data-ttu-id="a338e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a338e-111">-DefaultProfile</span></span>
<span data-ttu-id="a338e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a338e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a338e-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="a338e-113">-ProviderName</span></span>
<span data-ttu-id="a338e-114">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="a338e-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="a338e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a338e-115">-ResourceGroupName</span></span>
<span data-ttu-id="a338e-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a338e-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="a338e-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a338e-117">-ResourceName</span></span>
<span data-ttu-id="a338e-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a338e-118">The resource name.</span></span>

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

### <span data-ttu-id="a338e-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="a338e-119">-ResourceParentName</span></span>
<span data-ttu-id="a338e-120">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a338e-120">The parent resource name.</span></span>

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

### <span data-ttu-id="a338e-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="a338e-121">-ResourceParentType</span></span>
<span data-ttu-id="a338e-122">A szülőerőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="a338e-122">The parent resource type.</span></span>

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

### <span data-ttu-id="a338e-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a338e-123">-ResourceType</span></span>
<span data-ttu-id="a338e-124">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="a338e-124">The resource type.</span></span>

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

### <span data-ttu-id="a338e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a338e-125">CommonParameters</span></span>
<span data-ttu-id="a338e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a338e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a338e-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a338e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a338e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a338e-128">INPUTS</span></span>

### <span data-ttu-id="a338e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a338e-129">System.String</span></span>

## <span data-ttu-id="a338e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a338e-130">OUTPUTS</span></span>

### <span data-ttu-id="a338e-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="a338e-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="a338e-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a338e-132">NOTES</span></span>

## <span data-ttu-id="a338e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a338e-133">RELATED LINKS</span></span>
