---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c8e6f54b5bd4deeb4ef24559298306880740c6d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158634"
---
# <span data-ttu-id="c2ad7-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c2ad7-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="c2ad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ad7-103">Eltávolít egy Power BI-munkaterület-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="c2ad7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2ad7-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ad7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ad7-106">A **Remove-AzPowerBIWorkspaceCollection** parancsmag eltávolítja a Power BI munkaterület-gyűjteményét az Azure-előfizetésből és -erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="c2ad7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2ad7-107">EXAMPLES</span></span>

### <span data-ttu-id="c2ad7-108">1. példa: Munkaterület-gyűjtemény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c2ad7-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c2ad7-109">Ez a parancs eltávolítja a WCN11 nevű munkaterület-gyűjteményt a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c2ad7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2ad7-110">PARAMETERS</span></span>

### <span data-ttu-id="c2ad7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ad7-111">-DefaultProfile</span></span>
<span data-ttu-id="c2ad7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c2ad7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2ad7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2ad7-113">-ResourceGroupName</span></span>
<span data-ttu-id="c2ad7-114">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolít egy munkaterület-gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="c2ad7-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c2ad7-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c2ad7-116">Annak a Power BI-munkaterületi gyűjteménynek a neve, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c2ad7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2ad7-117">-Confirm</span></span>
<span data-ttu-id="c2ad7-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ad7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ad7-119">-WhatIf</span></span>
<span data-ttu-id="c2ad7-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ad7-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ad7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ad7-122">CommonParameters</span></span>
<span data-ttu-id="c2ad7-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ad7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ad7-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ad7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ad7-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2ad7-125">INPUTS</span></span>

### <span data-ttu-id="c2ad7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c2ad7-126">System.String</span></span>

## <span data-ttu-id="c2ad7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2ad7-127">OUTPUTS</span></span>

### <span data-ttu-id="c2ad7-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="c2ad7-128">System.Void</span></span>

## <span data-ttu-id="c2ad7-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2ad7-129">NOTES</span></span>

## <span data-ttu-id="c2ad7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2ad7-130">RELATED LINKS</span></span>

[<span data-ttu-id="c2ad7-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c2ad7-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="c2ad7-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c2ad7-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


