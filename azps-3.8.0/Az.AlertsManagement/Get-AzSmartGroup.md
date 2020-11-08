---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011206"
---
# <span data-ttu-id="ed194-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="ed194-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="ed194-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed194-102">SYNOPSIS</span></span>
<span data-ttu-id="ed194-103">Intelligens csoportok adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="ed194-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="ed194-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed194-104">SYNTAX</span></span>

### <span data-ttu-id="ed194-105">SmartGroupsListByFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed194-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed194-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="ed194-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed194-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed194-107">DESCRIPTION</span></span>
<span data-ttu-id="ed194-108">A **Get-AzSmartGroup** parancsmag intelligens csoportok adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ed194-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="ed194-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ed194-109">EXAMPLES</span></span>

### <span data-ttu-id="ed194-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ed194-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="ed194-111">Az összes olyan intelligens csoport felsorolása, amely az elmúlt 1 órában alakult.</span><span class="sxs-lookup"><span data-stu-id="ed194-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="ed194-112">A Format-List segítségével megtudhatja, hogy miként fejezheti be az egyes intelligens csoportok listáját.</span><span class="sxs-lookup"><span data-stu-id="ed194-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="ed194-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ed194-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="ed194-114">Intelligens csoport adatainak beolvasása azonosítóval (GUID) vagy erőforrás-azonosítóval (teljes kar-azonosító)</span><span class="sxs-lookup"><span data-stu-id="ed194-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="ed194-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed194-115">PARAMETERS</span></span>

### <span data-ttu-id="ed194-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed194-116">-DefaultProfile</span></span>
<span data-ttu-id="ed194-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed194-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed194-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="ed194-118">-SmartGroupId</span></span>
<span data-ttu-id="ed194-119">A SmartGroup SmartGroup/ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ed194-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="ed194-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="ed194-120">-SortBy</span></span>
<span data-ttu-id="ed194-121">A rendezés során használni kívánt riasztási tulajdonság</span><span class="sxs-lookup"><span data-stu-id="ed194-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="ed194-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="ed194-122">-SortOrder</span></span>
<span data-ttu-id="ed194-123">Rendezési sorrend</span><span class="sxs-lookup"><span data-stu-id="ed194-123">Sort Order</span></span>

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

### <span data-ttu-id="ed194-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="ed194-124">-TimeRange</span></span>
<span data-ttu-id="ed194-125">Támogatott időtartomány-értékek – 1h, 1d, 7D, 30d (alapérték: 1d)</span><span class="sxs-lookup"><span data-stu-id="ed194-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="ed194-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed194-126">CommonParameters</span></span>
<span data-ttu-id="ed194-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed194-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed194-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed194-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed194-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed194-129">INPUTS</span></span>

### <span data-ttu-id="ed194-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="ed194-130">None</span></span>

## <span data-ttu-id="ed194-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed194-131">OUTPUTS</span></span>

### <span data-ttu-id="ed194-132">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="ed194-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="ed194-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed194-133">NOTES</span></span>

## <span data-ttu-id="ed194-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed194-134">RELATED LINKS</span></span>
