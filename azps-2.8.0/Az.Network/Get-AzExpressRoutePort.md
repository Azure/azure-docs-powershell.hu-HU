---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 69a03bc9772e9d74fdc1863221c99b46620ae700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837594"
---
# <span data-ttu-id="3ae66-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ae66-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="3ae66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ae66-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae66-103">Azure ExpressRoutePort-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="3ae66-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="3ae66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ae66-104">SYNTAX</span></span>

### <span data-ttu-id="3ae66-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ae66-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ae66-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ae66-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ae66-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ae66-107">DESCRIPTION</span></span>
<span data-ttu-id="3ae66-108">A **Get-AzExpressRoutePort** parancsmag az ExpressRoutePort-objektum beolvasására szolgál az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="3ae66-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="3ae66-109">A visszaadott expressrouteport objektum bemenetként használható a ExpressRoutePort működő többi parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ae66-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="3ae66-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ae66-110">EXAMPLES</span></span>

### <span data-ttu-id="3ae66-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ae66-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="3ae66-112">Beolvassa a ExpressRoutePort objektumot az előfizetésben az erőforráscsoport $rg néven $PortName.</span><span class="sxs-lookup"><span data-stu-id="3ae66-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="3ae66-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3ae66-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="3ae66-114">Beilleszti az összes olyan ExpressRoutePort-objektumot, amelynek a neve "teszt" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="3ae66-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="3ae66-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="3ae66-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="3ae66-116">Beolvassa a ExpressRoutePort objektumot a ResourceId $idtal.</span><span class="sxs-lookup"><span data-stu-id="3ae66-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="3ae66-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ae66-117">PARAMETERS</span></span>

### <span data-ttu-id="3ae66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae66-118">-DefaultProfile</span></span>
<span data-ttu-id="3ae66-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ae66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae66-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ae66-120">-Name</span></span>
<span data-ttu-id="3ae66-121">A ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="3ae66-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="3ae66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae66-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ae66-123">A ExpressRoutePort erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ae66-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="3ae66-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ae66-124">-ResourceId</span></span>
<span data-ttu-id="3ae66-125">Az Express Route port ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ae66-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="3ae66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae66-126">CommonParameters</span></span>
<span data-ttu-id="3ae66-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ae66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae66-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3ae66-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae66-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ae66-129">INPUTS</span></span>

### <span data-ttu-id="3ae66-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3ae66-130">System.String</span></span>

## <span data-ttu-id="3ae66-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ae66-131">OUTPUTS</span></span>

### <span data-ttu-id="3ae66-132">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ae66-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3ae66-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ae66-133">NOTES</span></span>

## <span data-ttu-id="3ae66-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ae66-134">RELATED LINKS</span></span>

[<span data-ttu-id="3ae66-135">Új – AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ae66-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="3ae66-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ae66-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="3ae66-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3ae66-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
