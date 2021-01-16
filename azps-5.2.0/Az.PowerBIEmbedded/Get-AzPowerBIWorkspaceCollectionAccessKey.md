---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355770"
---
# <span data-ttu-id="a5419-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="a5419-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="a5419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5419-102">SYNOPSIS</span></span>
<span data-ttu-id="a5419-103">A Power BI munkaterület-gyűjteményéhez tartozó aktuális hozzáférési kulcsok lekérte.</span><span class="sxs-lookup"><span data-stu-id="a5419-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="a5419-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5419-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5419-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5419-105">DESCRIPTION</span></span>
<span data-ttu-id="a5419-106">A **Get-AzPowerBIWorkspaceCollectionAccessKey** parancsmag a Power BI munkaterület-gyűjteményéhez társított aktuális hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a5419-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="a5419-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5419-107">EXAMPLES</span></span>

### <span data-ttu-id="a5419-108">1. példa: A hozzáférési kulcsok lekérte</span><span class="sxs-lookup"><span data-stu-id="a5419-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="a5419-109">Ez a parancs a WCN11 nevű munkaterület-gyűjtemény hozzáférési kulcsait kapja meg a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="a5419-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="a5419-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5419-110">PARAMETERS</span></span>

### <span data-ttu-id="a5419-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5419-111">-DefaultProfile</span></span>
<span data-ttu-id="a5419-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5419-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5419-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5419-113">-ResourceGroupName</span></span>
<span data-ttu-id="a5419-114">A gyűjtemény erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5419-114">Specifies the name of the resource group of the collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5419-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a5419-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a5419-116">Annak a Power BI-munkaterületi gyűjteménynek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="a5419-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5419-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5419-117">CommonParameters</span></span>
<span data-ttu-id="a5419-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5419-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5419-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5419-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5419-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5419-120">INPUTS</span></span>

### <span data-ttu-id="a5419-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a5419-121">System.String</span></span>

## <span data-ttu-id="a5419-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5419-122">OUTPUTS</span></span>

### <span data-ttu-id="a5419-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="a5419-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="a5419-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5419-124">NOTES</span></span>

## <span data-ttu-id="a5419-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5419-125">RELATED LINKS</span></span>

[<span data-ttu-id="a5419-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="a5419-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


