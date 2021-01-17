---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468782"
---
# <span data-ttu-id="413f6-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="413f6-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="413f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="413f6-102">SYNOPSIS</span></span>
<span data-ttu-id="413f6-103">A megadott hozzáférési kulcs alaphelyzetbe állítása.</span><span class="sxs-lookup"><span data-stu-id="413f6-103">Resets the specified access key.</span></span>

## <span data-ttu-id="413f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="413f6-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="413f6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="413f6-105">DESCRIPTION</span></span>
<span data-ttu-id="413f6-106">A **Reset-AzPowerBIWorkspaceCollectionAccessKey** parancsmag alaphelyzetbe állítja a megadott hozzáférési kulcsot a Power BI-munkaterületi gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="413f6-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="413f6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="413f6-107">EXAMPLES</span></span>

### <span data-ttu-id="413f6-108">1. példa: Az elsődleges hozzáférési kulcs alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="413f6-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="413f6-109">Ez a parancs alaphelyzetbe állítja a WCN11 nevű munkaterület-gyűjtemény elsődleges hozzáférési kulcsát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="413f6-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="413f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="413f6-110">PARAMETERS</span></span>

### <span data-ttu-id="413f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413f6-111">-DefaultProfile</span></span>
<span data-ttu-id="413f6-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="413f6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="413f6-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="413f6-113">-Key1</span></span>
<span data-ttu-id="413f6-114">Azt jelzi, hogy ez a parancsmag alaphelyzetbe állítja az elsődleges hozzáférési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="413f6-114">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413f6-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="413f6-115">-Key2</span></span>
<span data-ttu-id="413f6-116">Azt jelzi, hogy ez a parancsmag alaphelyzetbe állítja a másodlagos hozzáférési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="413f6-116">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="413f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="413f6-118">A gyűjtemény erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="413f6-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="413f6-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="413f6-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="413f6-120">Annak a Power BI-munkaterületi gyűjteménynek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="413f6-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="413f6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="413f6-121">-Confirm</span></span>
<span data-ttu-id="413f6-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="413f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="413f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="413f6-123">-WhatIf</span></span>
<span data-ttu-id="413f6-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="413f6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="413f6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="413f6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="413f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413f6-126">CommonParameters</span></span>
<span data-ttu-id="413f6-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="413f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413f6-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413f6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413f6-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="413f6-129">INPUTS</span></span>

### <span data-ttu-id="413f6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="413f6-130">System.String</span></span>

## <span data-ttu-id="413f6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="413f6-131">OUTPUTS</span></span>

### <span data-ttu-id="413f6-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="413f6-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="413f6-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="413f6-133">NOTES</span></span>

## <span data-ttu-id="413f6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="413f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="413f6-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="413f6-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


