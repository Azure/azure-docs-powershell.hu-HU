---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146306"
---
# <span data-ttu-id="c7a62-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7a62-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="c7a62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a62-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a62-103">Munkaterületeket kap a Power BI munkaterület-gyűjteményében.</span><span class="sxs-lookup"><span data-stu-id="c7a62-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c7a62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7a62-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a62-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7a62-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a62-106">A **Get-AzPowerBIWorkspace** parancsmag munkaterületeket kap egy Power BI-munkaterület-gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="c7a62-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c7a62-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7a62-107">EXAMPLES</span></span>

### <span data-ttu-id="c7a62-108">1. példa: Munkaterület-gyűjtemény munkaterületei</span><span class="sxs-lookup"><span data-stu-id="c7a62-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c7a62-109">Ez a parancs a MEGADOTT erőforráscsoport WCN11 nevű munkaterület-gyűjteményéhez tartozó munkaterületeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7a62-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c7a62-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7a62-110">PARAMETERS</span></span>

### <span data-ttu-id="c7a62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a62-111">-DefaultProfile</span></span>
<span data-ttu-id="c7a62-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c7a62-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7a62-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a62-113">-ResourceGroupName</span></span>
<span data-ttu-id="c7a62-114">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a munkaterület-gyűjtemény tartozik.</span><span class="sxs-lookup"><span data-stu-id="c7a62-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="c7a62-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c7a62-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c7a62-116">Annak a munkaterület-gyűjteménynek a neve, amelyhez ez a parancsmag munkaterületet kap.</span><span class="sxs-lookup"><span data-stu-id="c7a62-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="c7a62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a62-117">CommonParameters</span></span>
<span data-ttu-id="c7a62-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a62-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a62-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a62-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7a62-120">INPUTS</span></span>

### <span data-ttu-id="c7a62-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c7a62-121">System.String</span></span>

## <span data-ttu-id="c7a62-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7a62-122">OUTPUTS</span></span>

### <span data-ttu-id="c7a62-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7a62-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="c7a62-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7a62-124">NOTES</span></span>

## <span data-ttu-id="c7a62-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7a62-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7a62-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c7a62-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


