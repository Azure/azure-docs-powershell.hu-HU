---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186288"
---
# <span data-ttu-id="3eb6f-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="3eb6f-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="3eb6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3eb6f-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb6f-103">Intelligens csoportok előzményeinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="3eb6f-103">Gets smart group history</span></span>

## <span data-ttu-id="3eb6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3eb6f-104">SYNTAX</span></span>

### <span data-ttu-id="3eb6f-105">BySmartGroupId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3eb6f-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eb6f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3eb6f-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3eb6f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3eb6f-107">DESCRIPTION</span></span>
<span data-ttu-id="3eb6f-108">A **Get-AzSmartGroupHistory** parancsmag az intelligens csoportok előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="3eb6f-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="3eb6f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3eb6f-109">EXAMPLES</span></span>

### <span data-ttu-id="3eb6f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3eb6f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="3eb6f-111">Az intelligens csoportok előzményeinek részletezése.</span><span class="sxs-lookup"><span data-stu-id="3eb6f-111">Gets smart group history details.</span></span>

## <span data-ttu-id="3eb6f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3eb6f-112">PARAMETERS</span></span>

### <span data-ttu-id="3eb6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb6f-113">-DefaultProfile</span></span>
<span data-ttu-id="3eb6f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3eb6f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb6f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eb6f-115">-InputObject</span></span>
<span data-ttu-id="3eb6f-116">Bemeneti objektum a pipeline-ról</span><span class="sxs-lookup"><span data-stu-id="3eb6f-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="3eb6f-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="3eb6f-117">-SmartGroupId</span></span>
<span data-ttu-id="3eb6f-118">A SmartGroup/ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3eb6f-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="3eb6f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb6f-119">CommonParameters</span></span>
<span data-ttu-id="3eb6f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3eb6f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb6f-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3eb6f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb6f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb6f-122">INPUTS</span></span>

### <span data-ttu-id="3eb6f-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="3eb6f-123">None</span></span>

## <span data-ttu-id="3eb6f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb6f-124">OUTPUTS</span></span>

### <span data-ttu-id="3eb6f-125">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="3eb6f-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="3eb6f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3eb6f-126">NOTES</span></span>

## <span data-ttu-id="3eb6f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3eb6f-127">RELATED LINKS</span></span>
