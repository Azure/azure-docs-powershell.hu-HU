---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: f9ce00bb5efbe5182143a08f9f205101b9f85611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932409"
---
# <span data-ttu-id="73d5b-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="73d5b-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="73d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="73d5b-103">Azure ExpressRoutePort-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="73d5b-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="73d5b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73d5b-104">SYNTAX</span></span>

### <span data-ttu-id="73d5b-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73d5b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73d5b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73d5b-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73d5b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73d5b-107">DESCRIPTION</span></span>
<span data-ttu-id="73d5b-108">A **Get-AzExpressRoutePort** parancsmaggal lekérhető egy ExpressRoutePort-objektum az előfizetéséből.</span><span class="sxs-lookup"><span data-stu-id="73d5b-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="73d5b-109">A visszaadott expressrouteport objektum használható bemenetként az ExpressRoutePorton működő más parancsmagok számára.</span><span class="sxs-lookup"><span data-stu-id="73d5b-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="73d5b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73d5b-110">EXAMPLES</span></span>

### <span data-ttu-id="73d5b-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="73d5b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="73d5b-112">Beszerzi az ExpressRoutePort objektumot, $PortName az előfizetés erőforráscsoport-$rg nevét.</span><span class="sxs-lookup"><span data-stu-id="73d5b-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="73d5b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="73d5b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="73d5b-114">Beszerzi az összes Olyan ExpressRoutePort-objektumot, amelynek a neve "teszt" névvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="73d5b-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="73d5b-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="73d5b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="73d5b-116">Beszerzi az ExpressRoutePort objektumot a ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="73d5b-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="73d5b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73d5b-117">PARAMETERS</span></span>

### <span data-ttu-id="73d5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d5b-118">-DefaultProfile</span></span>
<span data-ttu-id="73d5b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73d5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73d5b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="73d5b-120">-Name</span></span>
<span data-ttu-id="73d5b-121">Az ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="73d5b-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="73d5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73d5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="73d5b-123">Az ExpressRoutePort erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="73d5b-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="73d5b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73d5b-124">-ResourceId</span></span>
<span data-ttu-id="73d5b-125">Az expressz útvonalport Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="73d5b-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d5b-126">CommonParameters</span></span>
<span data-ttu-id="73d5b-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d5b-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73d5b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d5b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73d5b-129">INPUTS</span></span>

### <span data-ttu-id="73d5b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="73d5b-130">System.String</span></span>

## <span data-ttu-id="73d5b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73d5b-131">OUTPUTS</span></span>

### <span data-ttu-id="73d5b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="73d5b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="73d5b-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73d5b-133">NOTES</span></span>

## <span data-ttu-id="73d5b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73d5b-134">RELATED LINKS</span></span>

[<span data-ttu-id="73d5b-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="73d5b-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="73d5b-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="73d5b-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="73d5b-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="73d5b-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
