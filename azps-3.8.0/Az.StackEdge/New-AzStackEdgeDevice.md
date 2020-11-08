---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011662"
---
# <span data-ttu-id="2ab9c-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2ab9c-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="2ab9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ab9c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab9c-103">Új halom él eszköz beállítása</span><span class="sxs-lookup"><span data-stu-id="2ab9c-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="2ab9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ab9c-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ab9c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ab9c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab9c-106">A **New-AzStackEdgeDevice** parancsmag egy új, a halom szélén álló eszköz beállítása</span><span class="sxs-lookup"><span data-stu-id="2ab9c-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="2ab9c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2ab9c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ab9c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2ab9c-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="2ab9c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ab9c-109">PARAMETERS</span></span>

### <span data-ttu-id="2ab9c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ab9c-110">-AsJob</span></span>
<span data-ttu-id="2ab9c-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2ab9c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ab9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab9c-112">-DefaultProfile</span></span>
<span data-ttu-id="2ab9c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ab9c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ab9c-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="2ab9c-114">-Location</span></span>
<span data-ttu-id="2ab9c-115">Az eszköz helye</span><span class="sxs-lookup"><span data-stu-id="2ab9c-115">Location of the device</span></span>

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

### <span data-ttu-id="2ab9c-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ab9c-116">-Name</span></span>
<span data-ttu-id="2ab9c-117">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="2ab9c-117">Resource Name</span></span>

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

### <span data-ttu-id="2ab9c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ab9c-118">-ResourceGroupName</span></span>
<span data-ttu-id="2ab9c-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2ab9c-119">Resource Group Name</span></span>

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

### <span data-ttu-id="2ab9c-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ab9c-120">-Sku</span></span>
<span data-ttu-id="2ab9c-121">Az elérhető SKU-élek, átjáró</span><span class="sxs-lookup"><span data-stu-id="2ab9c-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="2ab9c-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ab9c-122">-Confirm</span></span>
<span data-ttu-id="2ab9c-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ab9c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ab9c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ab9c-124">-WhatIf</span></span>
<span data-ttu-id="2ab9c-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ab9c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ab9c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ab9c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ab9c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab9c-127">CommonParameters</span></span>
<span data-ttu-id="2ab9c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ab9c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab9c-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2ab9c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab9c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ab9c-130">INPUTS</span></span>

### <span data-ttu-id="2ab9c-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ab9c-131">None</span></span>

## <span data-ttu-id="2ab9c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ab9c-132">OUTPUTS</span></span>

### <span data-ttu-id="2ab9c-133">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2ab9c-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="2ab9c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ab9c-134">NOTES</span></span>

## <span data-ttu-id="2ab9c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ab9c-135">RELATED LINKS</span></span>
