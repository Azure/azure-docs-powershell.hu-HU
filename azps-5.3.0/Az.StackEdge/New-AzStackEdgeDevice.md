---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468361"
---
# <span data-ttu-id="0e13b-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0e13b-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="0e13b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e13b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e13b-103">Új Stack Edge-eszköz beállítása</span><span class="sxs-lookup"><span data-stu-id="0e13b-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="0e13b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e13b-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e13b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e13b-105">DESCRIPTION</span></span>
<span data-ttu-id="0e13b-106">A **New-AzStackEdgeDevice** parancsmag konfigurál egy új Stack Edge eszközt</span><span class="sxs-lookup"><span data-stu-id="0e13b-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="0e13b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e13b-107">EXAMPLES</span></span>

### <span data-ttu-id="0e13b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0e13b-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="0e13b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e13b-109">PARAMETERS</span></span>

### <span data-ttu-id="0e13b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e13b-110">-AsJob</span></span>
<span data-ttu-id="0e13b-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0e13b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e13b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e13b-112">-DefaultProfile</span></span>
<span data-ttu-id="0e13b-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e13b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e13b-114">-Location</span><span class="sxs-lookup"><span data-stu-id="0e13b-114">-Location</span></span>
<span data-ttu-id="0e13b-115">Az eszköz helye</span><span class="sxs-lookup"><span data-stu-id="0e13b-115">Location of the device</span></span>

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

### <span data-ttu-id="0e13b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0e13b-116">-Name</span></span>
<span data-ttu-id="0e13b-117">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="0e13b-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e13b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e13b-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e13b-119">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0e13b-119">Resource Group Name</span></span>

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

### <span data-ttu-id="0e13b-120">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="0e13b-120">-Sku</span></span>
<span data-ttu-id="0e13b-121">A rendelkezésre álló skus a Edge, az Átjáró</span><span class="sxs-lookup"><span data-stu-id="0e13b-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="0e13b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e13b-122">-Confirm</span></span>
<span data-ttu-id="0e13b-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0e13b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e13b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e13b-124">-WhatIf</span></span>
<span data-ttu-id="0e13b-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0e13b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e13b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e13b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e13b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e13b-127">CommonParameters</span></span>
<span data-ttu-id="0e13b-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e13b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e13b-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e13b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e13b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e13b-130">INPUTS</span></span>

### <span data-ttu-id="0e13b-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="0e13b-131">None</span></span>

## <span data-ttu-id="0e13b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e13b-132">OUTPUTS</span></span>

### <span data-ttu-id="0e13b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0e13b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="0e13b-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e13b-134">NOTES</span></span>

## <span data-ttu-id="0e13b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e13b-135">RELATED LINKS</span></span>
