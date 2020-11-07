---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: e51325a18f8a880131e9037473a60e8a56ea488f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93680927"
---
# <span data-ttu-id="72940-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="72940-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="72940-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72940-102">SYNOPSIS</span></span>
<span data-ttu-id="72940-103">Információt kap a tárterület-betekintésről.</span><span class="sxs-lookup"><span data-stu-id="72940-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72940-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72940-104">SYNTAX</span></span>

### <span data-ttu-id="72940-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72940-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72940-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="72940-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72940-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="72940-107">DESCRIPTION</span></span>
<span data-ttu-id="72940-108">A **Get-AzureRmOperationalInsightsStorageInsight** parancsmag információkat kap a meglévő tárterület-betekintésről.</span><span class="sxs-lookup"><span data-stu-id="72940-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="72940-109">Ha meg van adva egy tárterület-betekintési név, ez a parancsmag információkat kap a tárterületről.</span><span class="sxs-lookup"><span data-stu-id="72940-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="72940-110">Ha nem ad meg nevet, ez a parancsmag információkat kap a munkaterületen található összes tárterületről.</span><span class="sxs-lookup"><span data-stu-id="72940-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="72940-111">Példák</span><span class="sxs-lookup"><span data-stu-id="72940-111">EXAMPLES</span></span>

### <span data-ttu-id="72940-112">Példa 1: tárterület-betekintést kaphat név szerint</span><span class="sxs-lookup"><span data-stu-id="72940-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="72940-113">Ez a parancs beolvassa a MyStorageInsight nevű tárterület-betekintést a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="72940-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="72940-114">2. példa: tárterület betekintésének beszerzése munkaterület-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="72940-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="72940-115">Az első parancs a **Get-AzureRmOperationalInsightsWorkspace** parancsmagot használja az üzemeltetési környezetek munkaterületének beszerzéséhez, majd a $Workspace változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="72940-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="72940-116">A második parancs beolvassa a MyStorageInsight nevű tárterület-betekintést a $Workspace munkaterületéhez.</span><span class="sxs-lookup"><span data-stu-id="72940-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="72940-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72940-117">PARAMETERS</span></span>

### <span data-ttu-id="72940-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72940-118">-DefaultProfile</span></span>
<span data-ttu-id="72940-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="72940-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72940-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72940-120">-Name</span></span>
<span data-ttu-id="72940-121">A tárterület-betekintési nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="72940-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72940-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72940-122">-ResourceGroupName</span></span>
<span data-ttu-id="72940-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72940-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72940-124">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="72940-124">-Workspace</span></span>
<span data-ttu-id="72940-125">A tárolási környezeteket tartalmazó munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="72940-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72940-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="72940-126">-WorkspaceName</span></span>
<span data-ttu-id="72940-127">A tárolási állapotot tartalmazó munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72940-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72940-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72940-128">CommonParameters</span></span>
<span data-ttu-id="72940-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72940-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72940-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72940-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72940-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72940-131">INPUTS</span></span>

### <span data-ttu-id="72940-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="72940-132">PSWorkspace</span></span>
<span data-ttu-id="72940-133">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="72940-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="72940-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72940-134">OUTPUTS</span></span>

### <span data-ttu-id="72940-135">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. models. PSStorageInsight]</span><span class="sxs-lookup"><span data-stu-id="72940-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="72940-136">Microsoft. Azure. Command. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="72940-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="72940-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72940-137">NOTES</span></span>

## <span data-ttu-id="72940-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72940-138">RELATED LINKS</span></span>

[<span data-ttu-id="72940-139">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="72940-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


