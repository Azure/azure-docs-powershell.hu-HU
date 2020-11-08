---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195288"
---
# <span data-ttu-id="2badb-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2badb-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="2badb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2badb-102">SYNOPSIS</span></span>
<span data-ttu-id="2badb-103">Új halom él eszköz beállítása</span><span class="sxs-lookup"><span data-stu-id="2badb-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="2badb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2badb-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2badb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2badb-105">DESCRIPTION</span></span>
<span data-ttu-id="2badb-106">A **New-AzStackEdgeDevice** parancsmag egy új, a halom szélén álló eszköz beállítása</span><span class="sxs-lookup"><span data-stu-id="2badb-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="2badb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2badb-107">EXAMPLES</span></span>

### <span data-ttu-id="2badb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2badb-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="2badb-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2badb-109">PARAMETERS</span></span>

### <span data-ttu-id="2badb-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2badb-110">-AsJob</span></span>
<span data-ttu-id="2badb-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2badb-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2badb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2badb-112">-DefaultProfile</span></span>
<span data-ttu-id="2badb-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2badb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2badb-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="2badb-114">-Location</span></span>
<span data-ttu-id="2badb-115">Az eszköz helye</span><span class="sxs-lookup"><span data-stu-id="2badb-115">Location of the device</span></span>

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

### <span data-ttu-id="2badb-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2badb-116">-Name</span></span>
<span data-ttu-id="2badb-117">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="2badb-117">Resource Name</span></span>

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

### <span data-ttu-id="2badb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2badb-118">-ResourceGroupName</span></span>
<span data-ttu-id="2badb-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2badb-119">Resource Group Name</span></span>

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

### <span data-ttu-id="2badb-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="2badb-120">-Sku</span></span>
<span data-ttu-id="2badb-121">Az elérhető SKU-élek, átjáró</span><span class="sxs-lookup"><span data-stu-id="2badb-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="2badb-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2badb-122">-Confirm</span></span>
<span data-ttu-id="2badb-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2badb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2badb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2badb-124">-WhatIf</span></span>
<span data-ttu-id="2badb-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2badb-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2badb-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2badb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2badb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2badb-127">CommonParameters</span></span>
<span data-ttu-id="2badb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2badb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2badb-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2badb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2badb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2badb-130">INPUTS</span></span>

### <span data-ttu-id="2badb-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="2badb-131">None</span></span>

## <span data-ttu-id="2badb-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2badb-132">OUTPUTS</span></span>

### <span data-ttu-id="2badb-133">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2badb-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="2badb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2badb-134">NOTES</span></span>

## <span data-ttu-id="2badb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2badb-135">RELATED LINKS</span></span>