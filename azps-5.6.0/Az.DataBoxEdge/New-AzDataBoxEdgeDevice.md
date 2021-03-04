---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: b7deb19377d893d28d5b5924acf8c49daf706907
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931954"
---
# <span data-ttu-id="086dd-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="086dd-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="086dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="086dd-102">SYNOPSIS</span></span>
<span data-ttu-id="086dd-103">Új Data Box Edge-eszköz beállítása</span><span class="sxs-lookup"><span data-stu-id="086dd-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="086dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="086dd-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="086dd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="086dd-105">DESCRIPTION</span></span>
<span data-ttu-id="086dd-106">A **New-AzDataBoxEdgeDevice** parancsmag konfigurál egy új Data Box Edge eszközt</span><span class="sxs-lookup"><span data-stu-id="086dd-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="086dd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="086dd-107">EXAMPLES</span></span>

### <span data-ttu-id="086dd-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="086dd-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="086dd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="086dd-109">PARAMETERS</span></span>

### <span data-ttu-id="086dd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="086dd-110">-AsJob</span></span>
<span data-ttu-id="086dd-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="086dd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="086dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086dd-112">-DefaultProfile</span></span>
<span data-ttu-id="086dd-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="086dd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="086dd-114">-Location</span><span class="sxs-lookup"><span data-stu-id="086dd-114">-Location</span></span>
<span data-ttu-id="086dd-115">Az eszköz helye</span><span class="sxs-lookup"><span data-stu-id="086dd-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="086dd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="086dd-116">-Name</span></span>
<span data-ttu-id="086dd-117">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="086dd-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="086dd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="086dd-118">-ResourceGroupName</span></span>
<span data-ttu-id="086dd-119">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="086dd-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="086dd-120">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="086dd-120">-Sku</span></span>
<span data-ttu-id="086dd-121">A rendelkezésre álló skus a Edge, az Átjáró</span><span class="sxs-lookup"><span data-stu-id="086dd-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="086dd-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="086dd-122">-Confirm</span></span>
<span data-ttu-id="086dd-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="086dd-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="086dd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="086dd-124">-WhatIf</span></span>
<span data-ttu-id="086dd-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="086dd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="086dd-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="086dd-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="086dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086dd-127">CommonParameters</span></span>
<span data-ttu-id="086dd-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="086dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086dd-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="086dd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086dd-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="086dd-130">INPUTS</span></span>

### <span data-ttu-id="086dd-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="086dd-131">None</span></span>

## <span data-ttu-id="086dd-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="086dd-132">OUTPUTS</span></span>

### <span data-ttu-id="086dd-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="086dd-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="086dd-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="086dd-134">NOTES</span></span>

## <span data-ttu-id="086dd-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="086dd-135">RELATED LINKS</span></span>
