---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159835"
---
# <span data-ttu-id="09fa9-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="09fa9-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="09fa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="09fa9-103">Intelligens csoportelőzmények lekérte</span><span class="sxs-lookup"><span data-stu-id="09fa9-103">Gets smart group history</span></span>

## <span data-ttu-id="09fa9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09fa9-104">SYNTAX</span></span>

### <span data-ttu-id="09fa9-105">BySmartGroupId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09fa9-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09fa9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="09fa9-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09fa9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09fa9-107">DESCRIPTION</span></span>
<span data-ttu-id="09fa9-108">**A Get-AzSmartGroupHistory** parancsmag intelligens csoportelőzményeket kap.</span><span class="sxs-lookup"><span data-stu-id="09fa9-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="09fa9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09fa9-109">EXAMPLES</span></span>

### <span data-ttu-id="09fa9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="09fa9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="09fa9-111">Intelligens csoportelőzményeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="09fa9-111">Gets smart group history details.</span></span>

## <span data-ttu-id="09fa9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09fa9-112">PARAMETERS</span></span>

### <span data-ttu-id="09fa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fa9-113">-DefaultProfile</span></span>
<span data-ttu-id="09fa9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09fa9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09fa9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09fa9-115">-InputObject</span></span>
<span data-ttu-id="09fa9-116">Input object from pipeline.</span><span class="sxs-lookup"><span data-stu-id="09fa9-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09fa9-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="09fa9-117">-SmartGroupId</span></span>
<span data-ttu-id="09fa9-118">A riasztás SmartGroup /ResourceId azonosítója egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="09fa9-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fa9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fa9-119">CommonParameters</span></span>
<span data-ttu-id="09fa9-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fa9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fa9-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09fa9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fa9-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09fa9-122">INPUTS</span></span>

### <span data-ttu-id="09fa9-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="09fa9-123">None</span></span>

## <span data-ttu-id="09fa9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09fa9-124">OUTPUTS</span></span>

### <span data-ttu-id="09fa9-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="09fa9-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="09fa9-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09fa9-126">NOTES</span></span>

## <span data-ttu-id="09fa9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09fa9-127">RELATED LINKS</span></span>
