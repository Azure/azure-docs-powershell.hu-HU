---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479726"
---
# <span data-ttu-id="bd92f-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="bd92f-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="bd92f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd92f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd92f-103">Adatcsatlakozó adatokat fog kapni.</span><span class="sxs-lookup"><span data-stu-id="bd92f-103">Get a Data Connector.</span></span>

## <span data-ttu-id="bd92f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd92f-104">SYNTAX</span></span>

### <span data-ttu-id="bd92f-105">WorkspaceScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd92f-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd92f-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="bd92f-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd92f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd92f-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd92f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd92f-108">DESCRIPTION</span></span>
<span data-ttu-id="bd92f-109">A **Get-AzSentinelDataConnector** parancsmag egy adatösszekötőt kap a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="bd92f-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="bd92f-110">Ha a *DataConnectorId* paramétert adja meg, egyetlen **DataConnector-objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="bd92f-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="bd92f-111">Ha nem adja meg a *DataConnectorId* paramétert, a rendszer visszaad egy tömböt, amely a megadott munkaterület összes adatösszekötőt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bd92f-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="bd92f-112">A **DataConnector objektummal** frissítheti az Adatösszekötőt, például letilthatja az **Adatösszekötőt.**</span><span class="sxs-lookup"><span data-stu-id="bd92f-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="bd92f-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd92f-113">EXAMPLES</span></span>

### <span data-ttu-id="bd92f-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="bd92f-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="bd92f-115">Ebben a példában az összes **DataConnectors** a megadott munkaterületen, majd tárolja azt a $DataConnectors változóban.</span><span class="sxs-lookup"><span data-stu-id="bd92f-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="bd92f-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="bd92f-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="bd92f-117">Ez a példa lekért **egy DataConnectort** a megadott munkaterületre, majd tárolja azt a $DataConnector változóban.</span><span class="sxs-lookup"><span data-stu-id="bd92f-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="bd92f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd92f-118">PARAMETERS</span></span>

### <span data-ttu-id="bd92f-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="bd92f-119">-DataConnectorId</span></span>
<span data-ttu-id="bd92f-120">Adatkapcsolat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd92f-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd92f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd92f-121">-DefaultProfile</span></span>
<span data-ttu-id="bd92f-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd92f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd92f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd92f-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd92f-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd92f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd92f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd92f-125">-ResourceId</span></span>
<span data-ttu-id="bd92f-126">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bd92f-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd92f-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd92f-127">-WorkspaceName</span></span>
<span data-ttu-id="bd92f-128">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="bd92f-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd92f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd92f-129">CommonParameters</span></span>
<span data-ttu-id="bd92f-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd92f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd92f-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd92f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd92f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd92f-132">INPUTS</span></span>

### <span data-ttu-id="bd92f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bd92f-133">System.String</span></span>
## <span data-ttu-id="bd92f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd92f-134">OUTPUTS</span></span>

### <span data-ttu-id="bd92f-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="bd92f-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="bd92f-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd92f-136">NOTES</span></span>

## <span data-ttu-id="bd92f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd92f-137">RELATED LINKS</span></span>
