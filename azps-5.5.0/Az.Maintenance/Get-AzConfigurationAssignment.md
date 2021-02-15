---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207239"
---
# <span data-ttu-id="cb0d1-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="cb0d1-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="cb0d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0d1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0d1-103">List configurationAssignments for resource.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="cb0d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb0d1-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb0d1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb0d1-105">DESCRIPTION</span></span>
<span data-ttu-id="cb0d1-106">List configurationAssignments for resource.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="cb0d1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb0d1-107">EXAMPLES</span></span>

### <span data-ttu-id="cb0d1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="cb0d1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="cb0d1-109">List configurationAssignments for dedicated host.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="cb0d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb0d1-110">PARAMETERS</span></span>

### <span data-ttu-id="cb0d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0d1-111">-DefaultProfile</span></span>
<span data-ttu-id="cb0d1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb0d1-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="cb0d1-113">-ProviderName</span></span>
<span data-ttu-id="cb0d1-114">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="cb0d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb0d1-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="cb0d1-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cb0d1-117">-ResourceName</span></span>
<span data-ttu-id="cb0d1-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-118">The resource name.</span></span>

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

### <span data-ttu-id="cb0d1-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="cb0d1-119">-ResourceParentName</span></span>
<span data-ttu-id="cb0d1-120">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-120">The parent resource name.</span></span>

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

### <span data-ttu-id="cb0d1-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="cb0d1-121">-ResourceParentType</span></span>
<span data-ttu-id="cb0d1-122">A szülőerőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-122">The parent resource type.</span></span>

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

### <span data-ttu-id="cb0d1-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cb0d1-123">-ResourceType</span></span>
<span data-ttu-id="cb0d1-124">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-124">The resource type.</span></span>

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

### <span data-ttu-id="cb0d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0d1-125">CommonParameters</span></span>
<span data-ttu-id="cb0d1-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0d1-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb0d1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0d1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb0d1-128">INPUTS</span></span>

### <span data-ttu-id="cb0d1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cb0d1-129">System.String</span></span>

## <span data-ttu-id="cb0d1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb0d1-130">OUTPUTS</span></span>

### <span data-ttu-id="cb0d1-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="cb0d1-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="cb0d1-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb0d1-132">NOTES</span></span>

## <span data-ttu-id="cb0d1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb0d1-133">RELATED LINKS</span></span>
