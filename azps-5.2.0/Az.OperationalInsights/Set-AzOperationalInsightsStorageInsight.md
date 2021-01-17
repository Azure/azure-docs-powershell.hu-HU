---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346170"
---
# <span data-ttu-id="9370b-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="9370b-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="9370b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9370b-102">SYNOPSIS</span></span>
<span data-ttu-id="9370b-103">Frissíti a Tárterület-betekintőt.</span><span class="sxs-lookup"><span data-stu-id="9370b-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="9370b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9370b-104">SYNTAX</span></span>

### <span data-ttu-id="9370b-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9370b-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9370b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9370b-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9370b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9370b-107">DESCRIPTION</span></span>
<span data-ttu-id="9370b-108">A **Set-AzOperationalInsightsStorageInsight** parancsmag módosítja a Storage Insight konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="9370b-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="9370b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9370b-109">EXAMPLES</span></span>

### <span data-ttu-id="9370b-110">1. példa: Tárterület-betekintés módosítása név szerint</span><span class="sxs-lookup"><span data-stu-id="9370b-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="9370b-111">Ez a parancs módosítja a táblákat, amelyekből a MyStorageInsight nevű Tárterület-betekintés felolvassa.</span><span class="sxs-lookup"><span data-stu-id="9370b-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="9370b-112">2. példa: Tárterület-betekintés módosítása munkaterületi objektum használatával</span><span class="sxs-lookup"><span data-stu-id="9370b-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="9370b-113">Az első parancs a Get-AzOperationalInsightsWorkspace parancsmagot használva szerezze be a MyWorkspace nevű munkaterületet, majd tárolja azt a $Workspace változóban.</span><span class="sxs-lookup"><span data-stu-id="9370b-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="9370b-114">A második parancs módosítja a tárolókat, amelyekből a MyStorageInsight nevű Tárterület-betekintés felolvassa.</span><span class="sxs-lookup"><span data-stu-id="9370b-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="9370b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9370b-115">PARAMETERS</span></span>

### <span data-ttu-id="9370b-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="9370b-116">-Containers</span></span>
<span data-ttu-id="9370b-117">Megadja az adatokat tartalmazó tárolók listáját.</span><span class="sxs-lookup"><span data-stu-id="9370b-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="9370b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9370b-118">-DefaultProfile</span></span>
<span data-ttu-id="9370b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9370b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9370b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9370b-120">-Name</span></span>
<span data-ttu-id="9370b-121">A Tárterület-betekintő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9370b-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="9370b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9370b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9370b-123">Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9370b-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="9370b-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9370b-124">-StorageAccountKey</span></span>
<span data-ttu-id="9370b-125">A tárfiók hozzáférési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9370b-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="9370b-126">-Tables</span><span class="sxs-lookup"><span data-stu-id="9370b-126">-Tables</span></span>
<span data-ttu-id="9370b-127">Az adatokat tartalmazó táblák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9370b-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="9370b-128">-Workspace</span><span class="sxs-lookup"><span data-stu-id="9370b-128">-Workspace</span></span>
<span data-ttu-id="9370b-129">A Tárterület-betekintőt tartalmazó munkaterület.</span><span class="sxs-lookup"><span data-stu-id="9370b-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="9370b-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9370b-130">-WorkspaceName</span></span>
<span data-ttu-id="9370b-131">Egy munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9370b-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="9370b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9370b-132">CommonParameters</span></span>
<span data-ttu-id="9370b-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9370b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9370b-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9370b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9370b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9370b-135">INPUTS</span></span>

### <span data-ttu-id="9370b-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9370b-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9370b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9370b-137">System.String</span></span>

### <span data-ttu-id="9370b-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9370b-138">System.String[]</span></span>

## <span data-ttu-id="9370b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9370b-139">OUTPUTS</span></span>

### <span data-ttu-id="9370b-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="9370b-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="9370b-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9370b-141">NOTES</span></span>

## <span data-ttu-id="9370b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9370b-142">RELATED LINKS</span></span>

[<span data-ttu-id="9370b-143">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9370b-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="9370b-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9370b-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


