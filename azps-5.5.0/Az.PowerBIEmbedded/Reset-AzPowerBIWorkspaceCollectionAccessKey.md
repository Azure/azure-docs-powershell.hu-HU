---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158627"
---
# <span data-ttu-id="8670a-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="8670a-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="8670a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8670a-102">SYNOPSIS</span></span>
<span data-ttu-id="8670a-103">A megadott hozzáférési kulcs alaphelyzetbe állítása.</span><span class="sxs-lookup"><span data-stu-id="8670a-103">Resets the specified access key.</span></span>

## <span data-ttu-id="8670a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8670a-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8670a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8670a-105">DESCRIPTION</span></span>
<span data-ttu-id="8670a-106">A **Reset-AzPowerBIWorkspaceCollectionAccessKey** parancsmag alaphelyzetbe állítja a megadott hozzáférési kulcsot a Power BI-munkaterületi gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="8670a-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="8670a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8670a-107">EXAMPLES</span></span>

### <span data-ttu-id="8670a-108">1. példa: Az elsődleges hozzáférési kulcs alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="8670a-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="8670a-109">Ez a parancs alaphelyzetbe állítja a WCN11 nevű munkaterület-gyűjtemény elsődleges hozzáférési kulcsát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="8670a-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="8670a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8670a-110">PARAMETERS</span></span>

### <span data-ttu-id="8670a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8670a-111">-DefaultProfile</span></span>
<span data-ttu-id="8670a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8670a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8670a-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="8670a-113">-Key1</span></span>
<span data-ttu-id="8670a-114">Azt jelzi, hogy ez a parancsmag alaphelyzetbe állítja az elsődleges hozzáférési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8670a-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="8670a-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="8670a-115">-Key2</span></span>
<span data-ttu-id="8670a-116">Azt jelzi, hogy ez a parancsmag alaphelyzetbe állítja a másodlagos hozzáférési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8670a-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="8670a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8670a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8670a-118">A gyűjtemény erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8670a-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="8670a-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="8670a-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="8670a-120">Annak a Power BI-munkaterületi gyűjteménynek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="8670a-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8670a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8670a-121">-Confirm</span></span>
<span data-ttu-id="8670a-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8670a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8670a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8670a-123">-WhatIf</span></span>
<span data-ttu-id="8670a-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8670a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8670a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8670a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8670a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8670a-126">CommonParameters</span></span>
<span data-ttu-id="8670a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8670a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8670a-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8670a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8670a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8670a-129">INPUTS</span></span>

### <span data-ttu-id="8670a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8670a-130">System.String</span></span>

## <span data-ttu-id="8670a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8670a-131">OUTPUTS</span></span>

### <span data-ttu-id="8670a-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="8670a-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="8670a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8670a-133">NOTES</span></span>

## <span data-ttu-id="8670a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8670a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8670a-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="8670a-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


