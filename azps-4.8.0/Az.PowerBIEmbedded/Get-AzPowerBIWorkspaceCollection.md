---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182922"
---
# <span data-ttu-id="52f9d-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="52f9d-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="52f9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="52f9d-103">A Power BI Workspace-gyűjteményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="52f9d-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="52f9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52f9d-104">SYNTAX</span></span>

### <span data-ttu-id="52f9d-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="52f9d-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52f9d-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52f9d-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52f9d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="52f9d-107">DESCRIPTION</span></span>
<span data-ttu-id="52f9d-108">A **Get-AzPowerBIWorkspaceCollection** PARANCSMAG Power bi-munkaterületi gyűjteményeket kap az Azure-előfizetésben és az erőforrás-csoportban, illetve a gyűjtemény neve alapján.</span><span class="sxs-lookup"><span data-stu-id="52f9d-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="52f9d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="52f9d-109">EXAMPLES</span></span>

### <span data-ttu-id="52f9d-110">Példa 1: az összes munkaterületi gyűjtemény beolvasása egy erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="52f9d-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="52f9d-111">Ez a parancs a ResourceGroup17 nevű erőforráscsoport csoportjába tartozó munkaterületi gyűjteményeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="52f9d-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="52f9d-112">2. példa: munkaterületi gyűjtemény beszerzése a neve alapján</span><span class="sxs-lookup"><span data-stu-id="52f9d-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="52f9d-113">Ez a parancs a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="52f9d-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="52f9d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52f9d-114">PARAMETERS</span></span>

### <span data-ttu-id="52f9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f9d-115">-DefaultProfile</span></span>
<span data-ttu-id="52f9d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="52f9d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52f9d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f9d-117">-ResourceGroupName</span></span>
<span data-ttu-id="52f9d-118">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyből a parancsmag munkaterületi gyűjteményeket kap.</span><span class="sxs-lookup"><span data-stu-id="52f9d-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="52f9d-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="52f9d-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="52f9d-120">Annak a Power BI-munkaterületi gyűjteménynek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="52f9d-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="52f9d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f9d-121">CommonParameters</span></span>
<span data-ttu-id="52f9d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52f9d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f9d-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f9d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f9d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52f9d-124">INPUTS</span></span>

### <span data-ttu-id="52f9d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="52f9d-125">System.String</span></span>

## <span data-ttu-id="52f9d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52f9d-126">OUTPUTS</span></span>

### <span data-ttu-id="52f9d-127">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="52f9d-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="52f9d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52f9d-128">NOTES</span></span>

## <span data-ttu-id="52f9d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52f9d-129">RELATED LINKS</span></span>

[<span data-ttu-id="52f9d-130">Új – AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="52f9d-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="52f9d-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="52f9d-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


