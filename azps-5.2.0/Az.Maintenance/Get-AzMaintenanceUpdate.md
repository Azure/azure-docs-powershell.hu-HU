---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340830"
---
# <span data-ttu-id="47053-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="47053-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="47053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47053-102">SYNOPSIS</span></span>
<span data-ttu-id="47053-103">Az erőforrás függőben lévő karbantartási frissítései.</span><span class="sxs-lookup"><span data-stu-id="47053-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="47053-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47053-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47053-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47053-105">DESCRIPTION</span></span>
<span data-ttu-id="47053-106">Az erőforrás függőben lévő karbantartási frissítései.</span><span class="sxs-lookup"><span data-stu-id="47053-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="47053-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47053-107">EXAMPLES</span></span>

### <span data-ttu-id="47053-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="47053-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="47053-109">Az erőforrás függőben lévő karbantartási frissítései.</span><span class="sxs-lookup"><span data-stu-id="47053-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="47053-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47053-110">PARAMETERS</span></span>

### <span data-ttu-id="47053-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47053-111">-DefaultProfile</span></span>
<span data-ttu-id="47053-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47053-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47053-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="47053-113">-ProviderName</span></span>
<span data-ttu-id="47053-114">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="47053-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="47053-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47053-115">-ResourceGroupName</span></span>
<span data-ttu-id="47053-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="47053-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="47053-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="47053-117">-ResourceName</span></span>
<span data-ttu-id="47053-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="47053-118">The resource name.</span></span>

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

### <span data-ttu-id="47053-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="47053-119">-ResourceParentName</span></span>
<span data-ttu-id="47053-120">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="47053-120">The parent resource name.</span></span>

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

### <span data-ttu-id="47053-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="47053-121">-ResourceParentType</span></span>
<span data-ttu-id="47053-122">A szülőerőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="47053-122">The parent resource type.</span></span>

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

### <span data-ttu-id="47053-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="47053-123">-ResourceType</span></span>
<span data-ttu-id="47053-124">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="47053-124">The resource type.</span></span>

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

### <span data-ttu-id="47053-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47053-125">CommonParameters</span></span>
<span data-ttu-id="47053-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47053-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47053-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47053-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47053-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47053-128">INPUTS</span></span>

### <span data-ttu-id="47053-129">System.String</span><span class="sxs-lookup"><span data-stu-id="47053-129">System.String</span></span>

## <span data-ttu-id="47053-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47053-130">OUTPUTS</span></span>

### <span data-ttu-id="47053-131">Microsoft.Azure.Management.Maintenance.Models.Update</span><span class="sxs-lookup"><span data-stu-id="47053-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="47053-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47053-132">NOTES</span></span>

## <span data-ttu-id="47053-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47053-133">RELATED LINKS</span></span>
