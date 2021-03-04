---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: c2a622b110bdc17fe325934b50c59ac7e9b8f3ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937817"
---
# <span data-ttu-id="16002-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="16002-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="16002-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16002-102">SYNOPSIS</span></span>
<span data-ttu-id="16002-103">Frissíti a Tárterület-betekintőt.</span><span class="sxs-lookup"><span data-stu-id="16002-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="16002-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16002-104">SYNTAX</span></span>

### <span data-ttu-id="16002-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16002-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16002-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="16002-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16002-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16002-107">DESCRIPTION</span></span>
<span data-ttu-id="16002-108">A **Set-AzOperationalInsightsStorageInsight** parancsmag módosítja a Storage Insight konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="16002-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="16002-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16002-109">EXAMPLES</span></span>

### <span data-ttu-id="16002-110">1. példa: Tárterület-betekintés módosítása név szerint</span><span class="sxs-lookup"><span data-stu-id="16002-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="16002-111">Ez a parancs módosítja a táblákat, amelyekből a MyStorageInsight nevű Tárterület-betekintés felolvassa.</span><span class="sxs-lookup"><span data-stu-id="16002-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="16002-112">2. példa: Tárterület-betekintés módosítása munkaterületi objektum használatával</span><span class="sxs-lookup"><span data-stu-id="16002-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="16002-113">Az első parancs a Get-AzOperationalInsightsWorkspace parancsmagot használva szerezze be a MyWorkspace nevű munkaterületet, majd tárolja azt a $Workspace változóban.</span><span class="sxs-lookup"><span data-stu-id="16002-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="16002-114">A második parancs módosítja a tárolókat, amelyekből a MyStorageInsight nevű Tárterület-betekintés felolvassa.</span><span class="sxs-lookup"><span data-stu-id="16002-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="16002-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16002-115">PARAMETERS</span></span>

### <span data-ttu-id="16002-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="16002-116">-Containers</span></span>
<span data-ttu-id="16002-117">Megadja az adatokat tartalmazó tárolók listáját.</span><span class="sxs-lookup"><span data-stu-id="16002-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16002-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16002-118">-DefaultProfile</span></span>
<span data-ttu-id="16002-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16002-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16002-120">-Name</span><span class="sxs-lookup"><span data-stu-id="16002-120">-Name</span></span>
<span data-ttu-id="16002-121">A Tárterület-betekintő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16002-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16002-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16002-122">-ResourceGroupName</span></span>
<span data-ttu-id="16002-123">Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16002-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="16002-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="16002-124">-StorageAccountKey</span></span>
<span data-ttu-id="16002-125">A tárfiók hozzáférési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16002-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16002-126">-Tables</span><span class="sxs-lookup"><span data-stu-id="16002-126">-Tables</span></span>
<span data-ttu-id="16002-127">Az adatokat tartalmazó táblák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="16002-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16002-128">-Workspace</span><span class="sxs-lookup"><span data-stu-id="16002-128">-Workspace</span></span>
<span data-ttu-id="16002-129">A Tárterület-betekintőt tartalmazó munkaterület.</span><span class="sxs-lookup"><span data-stu-id="16002-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="16002-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="16002-130">-WorkspaceName</span></span>
<span data-ttu-id="16002-131">Egy munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16002-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="16002-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16002-132">CommonParameters</span></span>
<span data-ttu-id="16002-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16002-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16002-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16002-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16002-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16002-135">INPUTS</span></span>

### <span data-ttu-id="16002-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="16002-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="16002-137">System.String</span><span class="sxs-lookup"><span data-stu-id="16002-137">System.String</span></span>

### <span data-ttu-id="16002-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="16002-138">System.String[]</span></span>

## <span data-ttu-id="16002-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16002-139">OUTPUTS</span></span>

### <span data-ttu-id="16002-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="16002-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="16002-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16002-141">NOTES</span></span>

## <span data-ttu-id="16002-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16002-142">RELATED LINKS</span></span>

[<span data-ttu-id="16002-143">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="16002-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="16002-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="16002-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


