---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 99a9d8e4dcf10eaae67516e871c90d78021e6218
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919346"
---
# <span data-ttu-id="0481b-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0481b-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="0481b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0481b-102">SYNOPSIS</span></span>
<span data-ttu-id="0481b-103">Power BI-munkaterületi gyűjteményeket kap.</span><span class="sxs-lookup"><span data-stu-id="0481b-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="0481b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0481b-104">SYNTAX</span></span>

### <span data-ttu-id="0481b-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0481b-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0481b-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0481b-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0481b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0481b-107">DESCRIPTION</span></span>
<span data-ttu-id="0481b-108">A **Get-AzPowerBIWorkspaceCollection** parancsmag Power BI-munkaterület-gyűjteményeket kap az Azure-előfizetésében és az erőforráscsoportban, illetve a gyűjtemény neve alapján.</span><span class="sxs-lookup"><span data-stu-id="0481b-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="0481b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0481b-109">EXAMPLES</span></span>

### <span data-ttu-id="0481b-110">1. példa: Erőforráscsoport összes munkaterület-gyűjteményének begyűjtése</span><span class="sxs-lookup"><span data-stu-id="0481b-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="0481b-111">Ez a parancs az Erőforráscsoport17 nevű erőforráscsoporthoz tartozó munkaterület-gyűjteményeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0481b-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="0481b-112">2. példa: Munkaterület-gyűjtemény lekérte a nevét</span><span class="sxs-lookup"><span data-stu-id="0481b-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="0481b-113">Ez a parancs a WCN11 nevű munkaterület-gyűjteményt a megadott erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0481b-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="0481b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0481b-114">PARAMETERS</span></span>

### <span data-ttu-id="0481b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0481b-115">-DefaultProfile</span></span>
<span data-ttu-id="0481b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0481b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0481b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0481b-117">-ResourceGroupName</span></span>
<span data-ttu-id="0481b-118">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag munkaterület-gyűjteményeket kap.</span><span class="sxs-lookup"><span data-stu-id="0481b-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="0481b-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0481b-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0481b-120">Annak a Power BI-munkaterületi gyűjteménynek a neve, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="0481b-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0481b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0481b-121">CommonParameters</span></span>
<span data-ttu-id="0481b-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0481b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0481b-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0481b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0481b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0481b-124">INPUTS</span></span>

### <span data-ttu-id="0481b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0481b-125">System.String</span></span>

## <span data-ttu-id="0481b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0481b-126">OUTPUTS</span></span>

### <span data-ttu-id="0481b-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0481b-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="0481b-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0481b-128">NOTES</span></span>

## <span data-ttu-id="0481b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0481b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0481b-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0481b-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="0481b-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0481b-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


