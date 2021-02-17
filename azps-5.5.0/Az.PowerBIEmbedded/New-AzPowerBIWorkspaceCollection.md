---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169371"
---
# <span data-ttu-id="22e0d-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="22e0d-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="22e0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="22e0d-103">Power BI-munkaterületi gyűjteményt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="22e0d-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="22e0d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22e0d-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22e0d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22e0d-105">DESCRIPTION</span></span>
<span data-ttu-id="22e0d-106">A **New-AzPowerBIWorkspaceCollection** parancsmag létrehoz egy Power BI-munkaterületi gyűjteményt az Azure-előfizetéshez a megadott erőforráscsoportban és helyen.</span><span class="sxs-lookup"><span data-stu-id="22e0d-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="22e0d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22e0d-107">EXAMPLES</span></span>

### <span data-ttu-id="22e0d-108">1. példa: Munkaterület-gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="22e0d-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="22e0d-109">Ez a parancs wcn11 nevű munkaterület-gyűjteményt hoz létre a megadott erőforráscsoportban a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="22e0d-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="22e0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22e0d-110">PARAMETERS</span></span>

### <span data-ttu-id="22e0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e0d-111">-DefaultProfile</span></span>
<span data-ttu-id="22e0d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22e0d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22e0d-113">-Location</span><span class="sxs-lookup"><span data-stu-id="22e0d-113">-Location</span></span>
<span data-ttu-id="22e0d-114">Megadja azt az Azure-helyet, ahol ez a parancsmag munkaterület-gyűjteményt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="22e0d-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e0d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e0d-115">-ResourceGroupName</span></span>
<span data-ttu-id="22e0d-116">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag munkaterület-gyűjteményt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="22e0d-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="22e0d-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="22e0d-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="22e0d-118">A Power BI munkaterület-gyűjteményének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22e0d-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="22e0d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22e0d-119">-Confirm</span></span>
<span data-ttu-id="22e0d-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22e0d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e0d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e0d-121">-WhatIf</span></span>
<span data-ttu-id="22e0d-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22e0d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22e0d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22e0d-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e0d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e0d-124">CommonParameters</span></span>
<span data-ttu-id="22e0d-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e0d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e0d-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e0d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e0d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22e0d-127">INPUTS</span></span>

### <span data-ttu-id="22e0d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="22e0d-128">System.String</span></span>

## <span data-ttu-id="22e0d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22e0d-129">OUTPUTS</span></span>

### <span data-ttu-id="22e0d-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="22e0d-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="22e0d-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22e0d-131">NOTES</span></span>

## <span data-ttu-id="22e0d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22e0d-132">RELATED LINKS</span></span>

[<span data-ttu-id="22e0d-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="22e0d-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="22e0d-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="22e0d-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


