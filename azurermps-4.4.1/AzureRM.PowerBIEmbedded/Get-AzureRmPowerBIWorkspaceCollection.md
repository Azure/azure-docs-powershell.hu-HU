---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 93ca812f726e036d195e83170153f7b2df4a2352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504032"
---
# <span data-ttu-id="1e433-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1e433-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="1e433-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e433-102">SYNOPSIS</span></span>
<span data-ttu-id="1e433-103">A Power BI Workspace-gyűjteményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="1e433-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e433-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e433-104">SYNTAX</span></span>

### <span data-ttu-id="1e433-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e433-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e433-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e433-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e433-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e433-107">DESCRIPTION</span></span>
<span data-ttu-id="1e433-108">A **Get-AzureRmPowerBIWorkspaceCollection** PARANCSMAG Power bi-munkaterületi gyűjteményeket kap az Azure-előfizetésben és az erőforrás-csoportban, illetve a gyűjtemény neve alapján.</span><span class="sxs-lookup"><span data-stu-id="1e433-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="1e433-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1e433-109">EXAMPLES</span></span>

### <span data-ttu-id="1e433-110">Példa 1: az összes munkaterületi gyűjtemény beolvasása egy erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="1e433-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="1e433-111">Ez a parancs a ResourceGroup17 nevű erőforráscsoport csoportjába tartozó munkaterületi gyűjteményeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1e433-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="1e433-112">2. példa: munkaterületi gyűjtemény beszerzése a neve alapján</span><span class="sxs-lookup"><span data-stu-id="1e433-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="1e433-113">Ez a parancs a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1e433-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="1e433-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e433-114">PARAMETERS</span></span>

### <span data-ttu-id="1e433-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e433-115">-ResourceGroupName</span></span>
<span data-ttu-id="1e433-116">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyből a parancsmag munkaterületi gyűjteményeket kap.</span><span class="sxs-lookup"><span data-stu-id="1e433-116">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e433-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1e433-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="1e433-118">Annak a Power BI-munkaterületi gyűjteménynek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="1e433-118">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e433-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e433-119">-DefaultProfile</span></span>
<span data-ttu-id="1e433-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e433-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e433-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e433-121">CommonParameters</span></span>
<span data-ttu-id="1e433-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e433-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e433-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e433-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e433-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e433-124">INPUTS</span></span>

## <span data-ttu-id="1e433-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e433-125">OUTPUTS</span></span>

### <span data-ttu-id="1e433-126">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1e433-126">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="1e433-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e433-127">NOTES</span></span>

## <span data-ttu-id="1e433-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e433-128">RELATED LINKS</span></span>

[<span data-ttu-id="1e433-129">Új – AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1e433-129">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="1e433-130">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1e433-130">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


