---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184860"
---
# <span data-ttu-id="e743e-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="e743e-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="e743e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e743e-102">SYNOPSIS</span></span>
<span data-ttu-id="e743e-103">Az Express Route porthoz tartozó engedélyezési dokumentum letöltése</span><span class="sxs-lookup"><span data-stu-id="e743e-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="e743e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e743e-104">SYNTAX</span></span>

### <span data-ttu-id="e743e-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e743e-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e743e-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e743e-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e743e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e743e-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e743e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e743e-108">DESCRIPTION</span></span>
<span data-ttu-id="e743e-109">New-AzExpressRoutePortLOA parancsmag az Express Route-port PDF formátumban tölti le az engedélyezési dokumentum egy betűjét.</span><span class="sxs-lookup"><span data-stu-id="e743e-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="e743e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e743e-110">EXAMPLES</span></span>

### <span data-ttu-id="e743e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e743e-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="e743e-112">Töltse le az Express Route port "myPort" engedélyezési dokumentumát, és tárolja az "loa.pdf" fájlban.</span><span class="sxs-lookup"><span data-stu-id="e743e-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="e743e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e743e-113">PARAMETERS</span></span>

### <span data-ttu-id="e743e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e743e-114">-AsJob</span></span>
<span data-ttu-id="e743e-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e743e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e743e-116">-Ügyfélneve</span><span class="sxs-lookup"><span data-stu-id="e743e-116">-CustomerName</span></span>
<span data-ttu-id="e743e-117">Annak az ügyfélnek a neve, akihez az Express Route port van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e743e-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e743e-118">-DefaultProfile</span></span>
<span data-ttu-id="e743e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e743e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e743e-120">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="e743e-120">-Destination</span></span>
<span data-ttu-id="e743e-121">A kimeneti filepath az engedély betűjelének tárolásához.</span><span class="sxs-lookup"><span data-stu-id="e743e-121">The output filepath to store the Letter of Authorization to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743e-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e743e-122">-ExpressRoutePort</span></span>
<span data-ttu-id="e743e-123">Az Express Route port erőforrás.</span><span class="sxs-lookup"><span data-stu-id="e743e-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743e-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e743e-124">-Id</span></span>
<span data-ttu-id="e743e-125">Az Express Route port ResourceId</span><span class="sxs-lookup"><span data-stu-id="e743e-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e743e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e743e-126">-PassThru</span></span>
<span data-ttu-id="e743e-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e743e-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e743e-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e743e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e743e-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="e743e-129">-PortName</span></span>
<span data-ttu-id="e743e-130">Az Express Route port neve.</span><span class="sxs-lookup"><span data-stu-id="e743e-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e743e-131">-ResourceGroupName</span></span>
<span data-ttu-id="e743e-132">Az Express Route portot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e743e-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e743e-133">CommonParameters</span></span>
<span data-ttu-id="e743e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e743e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e743e-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e743e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e743e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e743e-136">INPUTS</span></span>

### <span data-ttu-id="e743e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e743e-137">System.String</span></span>

## <span data-ttu-id="e743e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e743e-138">OUTPUTS</span></span>

### <span data-ttu-id="e743e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e743e-139">System.Boolean</span></span>

## <span data-ttu-id="e743e-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e743e-140">NOTES</span></span>

## <span data-ttu-id="e743e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e743e-141">RELATED LINKS</span></span>