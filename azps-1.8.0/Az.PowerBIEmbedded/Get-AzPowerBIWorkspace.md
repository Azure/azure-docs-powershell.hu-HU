---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 0bba0651d8b1125673b97aea625a11e598db6c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669818"
---
# <span data-ttu-id="160a0-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="160a0-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="160a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="160a0-102">SYNOPSIS</span></span>
<span data-ttu-id="160a0-103">Beolvassa a munkaterületeket egy Power BI-munkaterületi gyűjteménybe.</span><span class="sxs-lookup"><span data-stu-id="160a0-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="160a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="160a0-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="160a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="160a0-105">DESCRIPTION</span></span>
<span data-ttu-id="160a0-106">A **Get-AzPowerBIWorkspace** parancsmag a Power bi-munkaterületi gyűjteményben kapja meg a munkaterületeket.</span><span class="sxs-lookup"><span data-stu-id="160a0-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="160a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="160a0-107">EXAMPLES</span></span>

### <span data-ttu-id="160a0-108">Példa 1: munkaterület-gyűjtemény munkaterületének beszerzése</span><span class="sxs-lookup"><span data-stu-id="160a0-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="160a0-109">Ez a parancs a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményéhez tartozó munkaterületeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="160a0-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="160a0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="160a0-110">PARAMETERS</span></span>

### <span data-ttu-id="160a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160a0-111">-DefaultProfile</span></span>
<span data-ttu-id="160a0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="160a0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="160a0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160a0-113">-ResourceGroupName</span></span>
<span data-ttu-id="160a0-114">Annak az erőforráscsoport-csoportnak a neve, amelyhez a munkaterületi gyűjtemény tartozik.</span><span class="sxs-lookup"><span data-stu-id="160a0-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="160a0-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="160a0-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="160a0-116">Annak a munkaterületi gyűjteménynek a neve, amelyhez ez a parancsmag munkaterületet kap.</span><span class="sxs-lookup"><span data-stu-id="160a0-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="160a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160a0-117">CommonParameters</span></span>
<span data-ttu-id="160a0-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="160a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160a0-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="160a0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160a0-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="160a0-120">INPUTS</span></span>

### <span data-ttu-id="160a0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="160a0-121">System.String</span></span>

## <span data-ttu-id="160a0-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="160a0-122">OUTPUTS</span></span>

### <span data-ttu-id="160a0-123">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="160a0-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="160a0-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="160a0-124">NOTES</span></span>

## <span data-ttu-id="160a0-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="160a0-125">RELATED LINKS</span></span>

[<span data-ttu-id="160a0-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="160a0-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


