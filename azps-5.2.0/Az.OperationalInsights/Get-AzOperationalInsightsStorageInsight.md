---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341298"
---
# <span data-ttu-id="ab244-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ab244-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="ab244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab244-102">SYNOPSIS</span></span>
<span data-ttu-id="ab244-103">Információkat kap a Tárterület-betekintésről.</span><span class="sxs-lookup"><span data-stu-id="ab244-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="ab244-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab244-104">SYNTAX</span></span>

### <span data-ttu-id="ab244-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab244-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab244-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ab244-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab244-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab244-107">DESCRIPTION</span></span>
<span data-ttu-id="ab244-108">A **Get-AzOperationalInsightsStorageInsight** parancsmag információt kap egy meglévő Tárterület-információról.</span><span class="sxs-lookup"><span data-stu-id="ab244-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="ab244-109">Ha a Tárterület-információ neve meg van adva, ez a parancsmag információt kap erről a Tárterület-információról.</span><span class="sxs-lookup"><span data-stu-id="ab244-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="ab244-110">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen található összes tárterület-elemzésről.</span><span class="sxs-lookup"><span data-stu-id="ab244-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="ab244-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab244-111">EXAMPLES</span></span>

### <span data-ttu-id="ab244-112">1. példa: Tárterület-betekintés betekintés név szerint</span><span class="sxs-lookup"><span data-stu-id="ab244-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="ab244-113">Ez a parancs bepillantást enged a MyStorageInsight nevű tárterület-információba a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="ab244-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ab244-114">2. példa: Tárterület-betekintés munkaterületi objektum használatával</span><span class="sxs-lookup"><span data-stu-id="ab244-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="ab244-115">Az első parancs a **Get-AzOperationalInsightsWorkspace** parancsmagot használva behoz egy Operational Insights-munkaterületet, majd a $Workspace tárolja.</span><span class="sxs-lookup"><span data-stu-id="ab244-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="ab244-116">A második parancs bepillantást enged a MyStorageInsight nevű tárterület-$Workspace.</span><span class="sxs-lookup"><span data-stu-id="ab244-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="ab244-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab244-117">PARAMETERS</span></span>

### <span data-ttu-id="ab244-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab244-118">-DefaultProfile</span></span>
<span data-ttu-id="ab244-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ab244-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab244-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ab244-120">-Name</span></span>
<span data-ttu-id="ab244-121">A Tárterület-elemzés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab244-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab244-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab244-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab244-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab244-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab244-124">-Workspace</span><span class="sxs-lookup"><span data-stu-id="ab244-124">-Workspace</span></span>
<span data-ttu-id="ab244-125">A Tárterület-elemzéseket tartalmazó munkaterület.</span><span class="sxs-lookup"><span data-stu-id="ab244-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab244-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ab244-126">-WorkspaceName</span></span>
<span data-ttu-id="ab244-127">Annak a munkaterületnek a neve, amely a Storage Insights webhelyet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ab244-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab244-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab244-128">CommonParameters</span></span>
<span data-ttu-id="ab244-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab244-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab244-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab244-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab244-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab244-131">INPUTS</span></span>

### <span data-ttu-id="ab244-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab244-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ab244-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ab244-133">System.String</span></span>

## <span data-ttu-id="ab244-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab244-134">OUTPUTS</span></span>

### <span data-ttu-id="ab244-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ab244-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="ab244-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab244-136">NOTES</span></span>

## <span data-ttu-id="ab244-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab244-137">RELATED LINKS</span></span>

[<span data-ttu-id="ab244-138">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ab244-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


