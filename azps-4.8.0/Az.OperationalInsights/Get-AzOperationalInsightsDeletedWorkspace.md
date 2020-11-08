---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184040"
---
# <span data-ttu-id="89ca0-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="89ca0-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="89ca0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="89ca0-103">Törölt munkaterületek listázása</span><span class="sxs-lookup"><span data-stu-id="89ca0-103">List deleted workspaces.</span></span>

## <span data-ttu-id="89ca0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89ca0-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89ca0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="89ca0-106">Törölt munkaterületek listázása</span><span class="sxs-lookup"><span data-stu-id="89ca0-106">List deleted workspaces.</span></span>

## <span data-ttu-id="89ca0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89ca0-107">EXAMPLES</span></span>

### <span data-ttu-id="89ca0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89ca0-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="89ca0-109">Törölt munkaterületek listázása</span><span class="sxs-lookup"><span data-stu-id="89ca0-109">List deleted workspaces.</span></span>

## <span data-ttu-id="89ca0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89ca0-110">PARAMETERS</span></span>

### <span data-ttu-id="89ca0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ca0-111">-DefaultProfile</span></span>
<span data-ttu-id="89ca0-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89ca0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ca0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ca0-113">-ResourceGroupName</span></span>
<span data-ttu-id="89ca0-114">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="89ca0-114">The resource group name.</span></span>

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

### <span data-ttu-id="89ca0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ca0-115">CommonParameters</span></span>
<span data-ttu-id="89ca0-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89ca0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ca0-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89ca0-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ca0-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89ca0-118">INPUTS</span></span>

### <span data-ttu-id="89ca0-119">System. String</span><span class="sxs-lookup"><span data-stu-id="89ca0-119">System.String</span></span>

## <span data-ttu-id="89ca0-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89ca0-120">OUTPUTS</span></span>

### <span data-ttu-id="89ca0-121">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="89ca0-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="89ca0-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89ca0-122">NOTES</span></span>

## <span data-ttu-id="89ca0-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89ca0-123">RELATED LINKS</span></span>
