---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338597"
---
# <span data-ttu-id="61912-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="61912-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="61912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61912-102">SYNOPSIS</span></span>
<span data-ttu-id="61912-103">Listdeleted workspaces.</span><span class="sxs-lookup"><span data-stu-id="61912-103">List deleted workspaces.</span></span>

## <span data-ttu-id="61912-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61912-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61912-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61912-105">DESCRIPTION</span></span>
<span data-ttu-id="61912-106">Listdeleted workspaces.</span><span class="sxs-lookup"><span data-stu-id="61912-106">List deleted workspaces.</span></span>

## <span data-ttu-id="61912-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61912-107">EXAMPLES</span></span>

### <span data-ttu-id="61912-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="61912-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="61912-109">Listdeleted workspaces.</span><span class="sxs-lookup"><span data-stu-id="61912-109">List deleted workspaces.</span></span>

## <span data-ttu-id="61912-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61912-110">PARAMETERS</span></span>

### <span data-ttu-id="61912-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61912-111">-DefaultProfile</span></span>
<span data-ttu-id="61912-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61912-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61912-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61912-113">-ResourceGroupName</span></span>
<span data-ttu-id="61912-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="61912-114">The resource group name.</span></span>

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

### <span data-ttu-id="61912-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61912-115">CommonParameters</span></span>
<span data-ttu-id="61912-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61912-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61912-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61912-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61912-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61912-118">INPUTS</span></span>

### <span data-ttu-id="61912-119">System.String</span><span class="sxs-lookup"><span data-stu-id="61912-119">System.String</span></span>

## <span data-ttu-id="61912-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61912-120">OUTPUTS</span></span>

### <span data-ttu-id="61912-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="61912-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="61912-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61912-122">NOTES</span></span>

## <span data-ttu-id="61912-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61912-123">RELATED LINKS</span></span>
