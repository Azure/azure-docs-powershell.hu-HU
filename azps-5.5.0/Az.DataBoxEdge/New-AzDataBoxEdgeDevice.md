---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162106"
---
# <span data-ttu-id="80269-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="80269-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="80269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80269-102">SYNOPSIS</span></span>
<span data-ttu-id="80269-103">Új Data Box Edge-eszköz beállítása</span><span class="sxs-lookup"><span data-stu-id="80269-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="80269-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80269-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80269-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80269-105">DESCRIPTION</span></span>
<span data-ttu-id="80269-106">A **New-AzDataBoxEdgeDevice** parancsmag konfigurál egy új Data Box Edge eszközt</span><span class="sxs-lookup"><span data-stu-id="80269-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="80269-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80269-107">EXAMPLES</span></span>

### <span data-ttu-id="80269-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="80269-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="80269-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80269-109">PARAMETERS</span></span>

### <span data-ttu-id="80269-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80269-110">-AsJob</span></span>
<span data-ttu-id="80269-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="80269-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80269-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80269-112">-DefaultProfile</span></span>
<span data-ttu-id="80269-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80269-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80269-114">-Location</span><span class="sxs-lookup"><span data-stu-id="80269-114">-Location</span></span>
<span data-ttu-id="80269-115">Az eszköz helye</span><span class="sxs-lookup"><span data-stu-id="80269-115">Location of the device</span></span>

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

### <span data-ttu-id="80269-116">-Name</span><span class="sxs-lookup"><span data-stu-id="80269-116">-Name</span></span>
<span data-ttu-id="80269-117">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="80269-117">Resource Name</span></span>

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

### <span data-ttu-id="80269-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80269-118">-ResourceGroupName</span></span>
<span data-ttu-id="80269-119">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="80269-119">Resource Group Name</span></span>

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

### <span data-ttu-id="80269-120">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="80269-120">-Sku</span></span>
<span data-ttu-id="80269-121">A rendelkezésre álló skus a Edge, az Átjáró</span><span class="sxs-lookup"><span data-stu-id="80269-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="80269-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80269-122">-Confirm</span></span>
<span data-ttu-id="80269-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="80269-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80269-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80269-124">-WhatIf</span></span>
<span data-ttu-id="80269-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="80269-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80269-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80269-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80269-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80269-127">CommonParameters</span></span>
<span data-ttu-id="80269-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80269-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80269-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80269-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80269-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80269-130">INPUTS</span></span>

### <span data-ttu-id="80269-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="80269-131">None</span></span>

## <span data-ttu-id="80269-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80269-132">OUTPUTS</span></span>

### <span data-ttu-id="80269-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="80269-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="80269-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80269-134">NOTES</span></span>

## <span data-ttu-id="80269-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80269-135">RELATED LINKS</span></span>
