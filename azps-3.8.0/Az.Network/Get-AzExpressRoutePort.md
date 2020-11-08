---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013361"
---
# <span data-ttu-id="1aa7d-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1aa7d-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="1aa7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1aa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa7d-103">Azure ExpressRoutePort-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="1aa7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1aa7d-104">SYNTAX</span></span>

### <span data-ttu-id="1aa7d-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1aa7d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aa7d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa7d-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aa7d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1aa7d-107">DESCRIPTION</span></span>
<span data-ttu-id="1aa7d-108">A **Get-AzExpressRoutePort** parancsmag az ExpressRoutePort-objektum beolvasására szolgál az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="1aa7d-109">A visszaadott expressrouteport objektum bemenetként használható a ExpressRoutePort működő többi parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="1aa7d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1aa7d-110">EXAMPLES</span></span>

### <span data-ttu-id="1aa7d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1aa7d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="1aa7d-112">Beolvassa a ExpressRoutePort objektumot az előfizetésben az erőforráscsoport $rg néven $PortName.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="1aa7d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1aa7d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="1aa7d-114">Beilleszti az összes olyan ExpressRoutePort-objektumot, amelynek a neve "teszt" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="1aa7d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="1aa7d-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="1aa7d-116">Beolvassa a ExpressRoutePort objektumot a ResourceId $idtal.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="1aa7d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1aa7d-117">PARAMETERS</span></span>

### <span data-ttu-id="1aa7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa7d-118">-DefaultProfile</span></span>
<span data-ttu-id="1aa7d-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa7d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1aa7d-120">-Name</span></span>
<span data-ttu-id="1aa7d-121">A ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="1aa7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="1aa7d-123">A ExpressRoutePort erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="1aa7d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aa7d-124">-ResourceId</span></span>
<span data-ttu-id="1aa7d-125">Az Express Route port ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aa7d-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="1aa7d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa7d-126">CommonParameters</span></span>
<span data-ttu-id="1aa7d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1aa7d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa7d-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1aa7d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa7d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1aa7d-129">INPUTS</span></span>

### <span data-ttu-id="1aa7d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1aa7d-130">System.String</span></span>

## <span data-ttu-id="1aa7d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1aa7d-131">OUTPUTS</span></span>

### <span data-ttu-id="1aa7d-132">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1aa7d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="1aa7d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1aa7d-133">NOTES</span></span>

## <span data-ttu-id="1aa7d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1aa7d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1aa7d-135">Új – AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1aa7d-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="1aa7d-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1aa7d-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="1aa7d-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1aa7d-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
