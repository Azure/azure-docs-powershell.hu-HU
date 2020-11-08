---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014225"
---
# <span data-ttu-id="6b58e-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="6b58e-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="6b58e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b58e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b58e-103">Az erőforrás configurationAssignments listája</span><span class="sxs-lookup"><span data-stu-id="6b58e-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="6b58e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b58e-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b58e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b58e-105">DESCRIPTION</span></span>
<span data-ttu-id="6b58e-106">Az erőforrás configurationAssignments listája</span><span class="sxs-lookup"><span data-stu-id="6b58e-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="6b58e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6b58e-107">EXAMPLES</span></span>

### <span data-ttu-id="6b58e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6b58e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="6b58e-109">A lista configurationAssignments dedikált állomáshoz.</span><span class="sxs-lookup"><span data-stu-id="6b58e-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="6b58e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b58e-110">PARAMETERS</span></span>

### <span data-ttu-id="6b58e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b58e-111">-DefaultProfile</span></span>
<span data-ttu-id="6b58e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b58e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b58e-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="6b58e-113">-ProviderName</span></span>
<span data-ttu-id="6b58e-114">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="6b58e-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="6b58e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b58e-115">-ResourceGroupName</span></span>
<span data-ttu-id="6b58e-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6b58e-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="6b58e-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b58e-117">-ResourceName</span></span>
<span data-ttu-id="6b58e-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6b58e-118">The resource name.</span></span>

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

### <span data-ttu-id="6b58e-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="6b58e-119">-ResourceParentName</span></span>
<span data-ttu-id="6b58e-120">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6b58e-120">The parent resource name.</span></span>

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

### <span data-ttu-id="6b58e-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="6b58e-121">-ResourceParentType</span></span>
<span data-ttu-id="6b58e-122">A szülő-erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="6b58e-122">The parent resource type.</span></span>

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

### <span data-ttu-id="6b58e-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6b58e-123">-ResourceType</span></span>
<span data-ttu-id="6b58e-124">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="6b58e-124">The resource type.</span></span>

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

### <span data-ttu-id="6b58e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b58e-125">CommonParameters</span></span>
<span data-ttu-id="6b58e-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b58e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b58e-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6b58e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b58e-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b58e-128">INPUTS</span></span>

### <span data-ttu-id="6b58e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6b58e-129">System.String</span></span>

## <span data-ttu-id="6b58e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b58e-130">OUTPUTS</span></span>

### <span data-ttu-id="6b58e-131">Microsoft. Azure. commands. Maintenance. models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="6b58e-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="6b58e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b58e-132">NOTES</span></span>

## <span data-ttu-id="6b58e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b58e-133">RELATED LINKS</span></span>
