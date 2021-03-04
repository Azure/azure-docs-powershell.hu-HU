---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 06e17c012f52883d5e160698bb6f858f4644af6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929921"
---
# <span data-ttu-id="19945-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="19945-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="19945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19945-102">SYNOPSIS</span></span>
<span data-ttu-id="19945-103">A Power BI munkaterület-gyűjteményéhez tartozó aktuális hozzáférési kulcsok lekérte.</span><span class="sxs-lookup"><span data-stu-id="19945-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="19945-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19945-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19945-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19945-105">DESCRIPTION</span></span>
<span data-ttu-id="19945-106">A **Get-AzPowerBIWorkspaceCollectionAccessKey** parancsmag a Power BI munkaterület-gyűjteményéhez társított aktuális hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19945-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="19945-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19945-107">EXAMPLES</span></span>

### <span data-ttu-id="19945-108">1. példa: A hozzáférési kulcsok lekérte</span><span class="sxs-lookup"><span data-stu-id="19945-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="19945-109">Ez a parancs a WCN11 nevű munkaterület-gyűjtemény hozzáférési kulcsait kapja meg a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="19945-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="19945-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19945-110">PARAMETERS</span></span>

### <span data-ttu-id="19945-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19945-111">-DefaultProfile</span></span>
<span data-ttu-id="19945-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19945-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19945-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19945-113">-ResourceGroupName</span></span>
<span data-ttu-id="19945-114">A gyűjtemény erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19945-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="19945-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="19945-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="19945-116">Annak a Power BI-munkaterületi gyűjteménynek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="19945-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="19945-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19945-117">CommonParameters</span></span>
<span data-ttu-id="19945-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19945-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19945-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19945-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19945-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19945-120">INPUTS</span></span>

### <span data-ttu-id="19945-121">System.String</span><span class="sxs-lookup"><span data-stu-id="19945-121">System.String</span></span>

## <span data-ttu-id="19945-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19945-122">OUTPUTS</span></span>

### <span data-ttu-id="19945-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="19945-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="19945-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19945-124">NOTES</span></span>

## <span data-ttu-id="19945-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19945-125">RELATED LINKS</span></span>

[<span data-ttu-id="19945-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="19945-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


