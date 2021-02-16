---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167027"
---
# <span data-ttu-id="5427a-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="5427a-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="5427a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5427a-102">SYNOPSIS</span></span>
<span data-ttu-id="5427a-103">Intelligens csoportokra vonatkozó információk lekérte</span><span class="sxs-lookup"><span data-stu-id="5427a-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="5427a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5427a-104">SYNTAX</span></span>

### <span data-ttu-id="5427a-105">SmartGroupsListByFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5427a-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5427a-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="5427a-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5427a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5427a-107">DESCRIPTION</span></span>
<span data-ttu-id="5427a-108">**A Get-AzSmartGroup** parancsmag intelligens csoportokkal kapcsolatos információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="5427a-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="5427a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5427a-109">EXAMPLES</span></span>

### <span data-ttu-id="5427a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="5427a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="5427a-111">List all smart groups formed in last 1 hour.</span><span class="sxs-lookup"><span data-stu-id="5427a-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="5427a-112">A Format-List a lista minden intelligens csoportjának részletes adatait.</span><span class="sxs-lookup"><span data-stu-id="5427a-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="5427a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5427a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="5427a-114">Intelligens csoport részleteinek lekérte azonosító (GUID) vagy erőforrás-azonosító (Complete ARM Id) szerint</span><span class="sxs-lookup"><span data-stu-id="5427a-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="5427a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5427a-115">PARAMETERS</span></span>

### <span data-ttu-id="5427a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5427a-116">-DefaultProfile</span></span>
<span data-ttu-id="5427a-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5427a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5427a-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="5427a-118">-SmartGroupId</span></span>
<span data-ttu-id="5427a-119">A SmartGroup /ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5427a-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5427a-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="5427a-120">-SortBy</span></span>
<span data-ttu-id="5427a-121">A rendezéshez használható Riasztás tulajdonság</span><span class="sxs-lookup"><span data-stu-id="5427a-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5427a-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="5427a-122">-SortOrder</span></span>
<span data-ttu-id="5427a-123">Rendezési sorrend</span><span class="sxs-lookup"><span data-stu-id="5427a-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5427a-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="5427a-124">-TimeRange</span></span>
<span data-ttu-id="5427a-125">Támogatott időtartomány-értékek – 1h, 1d, 7d, 30d (Az alapértelmezett érték 1d)</span><span class="sxs-lookup"><span data-stu-id="5427a-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5427a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5427a-126">CommonParameters</span></span>
<span data-ttu-id="5427a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5427a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5427a-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5427a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5427a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5427a-129">INPUTS</span></span>

### <span data-ttu-id="5427a-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="5427a-130">None</span></span>

## <span data-ttu-id="5427a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5427a-131">OUTPUTS</span></span>

### <span data-ttu-id="5427a-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="5427a-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="5427a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5427a-133">NOTES</span></span>

## <span data-ttu-id="5427a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5427a-134">RELATED LINKS</span></span>
