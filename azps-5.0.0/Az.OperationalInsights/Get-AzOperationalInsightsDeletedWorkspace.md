---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194210"
---
# <span data-ttu-id="1a836-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="1a836-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="1a836-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a836-102">SYNOPSIS</span></span>
<span data-ttu-id="1a836-103">Törölt munkaterületek listázása</span><span class="sxs-lookup"><span data-stu-id="1a836-103">List deleted workspaces.</span></span>

## <span data-ttu-id="1a836-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a836-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a836-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a836-105">DESCRIPTION</span></span>
<span data-ttu-id="1a836-106">Törölt munkaterületek listázása</span><span class="sxs-lookup"><span data-stu-id="1a836-106">List deleted workspaces.</span></span>

## <span data-ttu-id="1a836-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1a836-107">EXAMPLES</span></span>

### <span data-ttu-id="1a836-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1a836-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="1a836-109">Törölt munkaterületek listázása</span><span class="sxs-lookup"><span data-stu-id="1a836-109">List deleted workspaces.</span></span>

## <span data-ttu-id="1a836-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a836-110">PARAMETERS</span></span>

### <span data-ttu-id="1a836-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a836-111">-DefaultProfile</span></span>
<span data-ttu-id="1a836-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a836-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a836-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a836-113">-ResourceGroupName</span></span>
<span data-ttu-id="1a836-114">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1a836-114">The resource group name.</span></span>

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

### <span data-ttu-id="1a836-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a836-115">CommonParameters</span></span>
<span data-ttu-id="1a836-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a836-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a836-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1a836-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a836-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a836-118">INPUTS</span></span>

### <span data-ttu-id="1a836-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1a836-119">System.String</span></span>

## <span data-ttu-id="1a836-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a836-120">OUTPUTS</span></span>

### <span data-ttu-id="1a836-121">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1a836-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1a836-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a836-122">NOTES</span></span>

## <span data-ttu-id="1a836-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a836-123">RELATED LINKS</span></span>
