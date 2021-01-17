---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347934"
---
# <span data-ttu-id="74041-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="74041-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="74041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74041-102">SYNOPSIS</span></span>
<span data-ttu-id="74041-103">Töltse le az engedélyezési dokumentumot egy gyors útvonalporthoz.</span><span class="sxs-lookup"><span data-stu-id="74041-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="74041-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74041-104">SYNTAX</span></span>

### <span data-ttu-id="74041-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74041-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74041-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74041-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74041-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74041-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74041-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74041-108">DESCRIPTION</span></span>
<span data-ttu-id="74041-109">New-AzExpressRoutePortLOA parancsmag egy engedélyezési dokumentumot tölt le PDF formátumban egy gyors útvonalporthoz.</span><span class="sxs-lookup"><span data-stu-id="74041-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="74041-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74041-110">EXAMPLES</span></span>

### <span data-ttu-id="74041-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="74041-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="74041-112">Töltse le a "myPort" express route portjához szükséges engedélyezési dokumentumot, és tárolja "loa.pdf" fájlban.</span><span class="sxs-lookup"><span data-stu-id="74041-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="74041-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74041-113">PARAMETERS</span></span>

### <span data-ttu-id="74041-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74041-114">-AsJob</span></span>
<span data-ttu-id="74041-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="74041-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74041-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="74041-116">-CustomerName</span></span>
<span data-ttu-id="74041-117">Az ügyfél neve, akihez az Express Route Port hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="74041-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="74041-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74041-118">-DefaultProfile</span></span>
<span data-ttu-id="74041-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74041-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74041-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="74041-120">-Destination</span></span>
<span data-ttu-id="74041-121">A kimeneti fájlpath, amelybe a meghatalmazást tárolni kell.</span><span class="sxs-lookup"><span data-stu-id="74041-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="74041-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="74041-122">-ExpressRoutePort</span></span>
<span data-ttu-id="74041-123">Az express route port erőforrás.</span><span class="sxs-lookup"><span data-stu-id="74041-123">The express route port resource.</span></span>

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

### <span data-ttu-id="74041-124">-Id</span><span class="sxs-lookup"><span data-stu-id="74041-124">-Id</span></span>
<span data-ttu-id="74041-125">Az expressz útvonalport Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="74041-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="74041-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74041-126">-PassThru</span></span>
<span data-ttu-id="74041-127">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="74041-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="74041-128">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="74041-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74041-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="74041-129">-PortName</span></span>
<span data-ttu-id="74041-130">Az express route port neve.</span><span class="sxs-lookup"><span data-stu-id="74041-130">The express route port name.</span></span>

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

### <span data-ttu-id="74041-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74041-131">-ResourceGroupName</span></span>
<span data-ttu-id="74041-132">Az express route port erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="74041-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="74041-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74041-133">CommonParameters</span></span>
<span data-ttu-id="74041-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74041-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74041-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74041-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74041-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74041-136">INPUTS</span></span>

### <span data-ttu-id="74041-137">System.String</span><span class="sxs-lookup"><span data-stu-id="74041-137">System.String</span></span>

## <span data-ttu-id="74041-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74041-138">OUTPUTS</span></span>

### <span data-ttu-id="74041-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74041-139">System.Boolean</span></span>

## <span data-ttu-id="74041-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74041-140">NOTES</span></span>

## <span data-ttu-id="74041-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74041-141">RELATED LINKS</span></span>
