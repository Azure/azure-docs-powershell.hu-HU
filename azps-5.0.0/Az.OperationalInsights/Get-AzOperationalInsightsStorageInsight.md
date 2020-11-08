---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194209"
---
# <span data-ttu-id="fb4fa-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="fb4fa-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="fb4fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4fa-103">Információt kap a tárterület-betekintésről.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="fb4fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb4fa-104">SYNTAX</span></span>

### <span data-ttu-id="fb4fa-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb4fa-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb4fa-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fb4fa-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb4fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb4fa-107">DESCRIPTION</span></span>
<span data-ttu-id="fb4fa-108">A **Get-AzOperationalInsightsStorageInsight** parancsmag információkat kap a meglévő tárterület-betekintésről.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="fb4fa-109">Ha meg van adva egy tárterület-betekintési név, ez a parancsmag információkat kap a tárterületről.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="fb4fa-110">Ha nem ad meg nevet, ez a parancsmag információkat kap a munkaterületen található összes tárterületről.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="fb4fa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fb4fa-111">EXAMPLES</span></span>

### <span data-ttu-id="fb4fa-112">Példa 1: tárterület-betekintést kaphat név szerint</span><span class="sxs-lookup"><span data-stu-id="fb4fa-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="fb4fa-113">Ez a parancs beolvassa a MyStorageInsight nevű tárterület-betekintést a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fb4fa-114">2. példa: tárterület betekintésének beszerzése munkaterület-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="fb4fa-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="fb4fa-115">Az első parancs a **Get-AzOperationalInsightsWorkspace** parancsmagot használja az üzemeltetési környezetek munkaterületének beszerzéséhez, majd a $Workspace változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="fb4fa-116">A második parancs beolvassa a MyStorageInsight nevű tárterület-betekintést a $Workspace munkaterületéhez.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="fb4fa-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb4fa-117">PARAMETERS</span></span>

### <span data-ttu-id="fb4fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4fa-118">-DefaultProfile</span></span>
<span data-ttu-id="fb4fa-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb4fa-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb4fa-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb4fa-120">-Name</span></span>
<span data-ttu-id="fb4fa-121">A tárterület-betekintési nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="fb4fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb4fa-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="fb4fa-124">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="fb4fa-124">-Workspace</span></span>
<span data-ttu-id="fb4fa-125">A tárolási környezeteket tartalmazó munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="fb4fa-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb4fa-126">-WorkspaceName</span></span>
<span data-ttu-id="fb4fa-127">A tárolási állapotot tartalmazó munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb4fa-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="fb4fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4fa-128">CommonParameters</span></span>
<span data-ttu-id="fb4fa-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb4fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4fa-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4fa-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4fa-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb4fa-131">INPUTS</span></span>

### <span data-ttu-id="fb4fa-132">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fb4fa-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="fb4fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fb4fa-133">System.String</span></span>

## <span data-ttu-id="fb4fa-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb4fa-134">OUTPUTS</span></span>

### <span data-ttu-id="fb4fa-135">Microsoft. Azure. Command. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="fb4fa-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="fb4fa-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb4fa-136">NOTES</span></span>

## <span data-ttu-id="fb4fa-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb4fa-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb4fa-138">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fb4fa-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

