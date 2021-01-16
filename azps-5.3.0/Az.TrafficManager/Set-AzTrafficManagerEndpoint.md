---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382757"
---
# <span data-ttu-id="fc129-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc129-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="fc129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc129-102">SYNOPSIS</span></span>
<span data-ttu-id="fc129-103">Frissíti a Traffic Manager-végpontot.</span><span class="sxs-lookup"><span data-stu-id="fc129-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="fc129-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc129-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc129-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc129-105">DESCRIPTION</span></span>
<span data-ttu-id="fc129-106">A **Set-AzTrafficManagerEndpoint** parancsmag frissíti a végpontokat az Azure Traffic Managerben.</span><span class="sxs-lookup"><span data-stu-id="fc129-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="fc129-107">Ez a parancsmag frissíti a beállításokat egy helyi végpontobjektumból.</span><span class="sxs-lookup"><span data-stu-id="fc129-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="fc129-108">A végpontobjektumot a *TrafficManagerEndpoint* paraméterrel vagy a folyamat használatával adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="fc129-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="fc129-109">A végpontot képviselő helyi objektumot a Get-AzTrafficManagerEndpoint használatával szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="fc129-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="fc129-110">Módosítsa az objektumot helyben, majd a **Set-AzTrafficManagerEndpoint** segítségével véglegesítse a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="fc129-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="fc129-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc129-111">EXAMPLES</span></span>

### <span data-ttu-id="fc129-112">1. példa: Végpont frissítése</span><span class="sxs-lookup"><span data-stu-id="fc129-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="fc129-113">Az első parancs a **Get-AzTrafficManagerEndpoint** parancsmag használatával kap egy Azure Traffic Manager-végpontot.</span><span class="sxs-lookup"><span data-stu-id="fc129-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="fc129-114">A parancs helyileg tárolja a végpontot a $TrafficManagerEndpoint változóban.</span><span class="sxs-lookup"><span data-stu-id="fc129-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="fc129-115">A második parancs helyben módosítja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="fc129-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="fc129-116">Ez a parancs 20-ra módosítja a végpont súlyát.</span><span class="sxs-lookup"><span data-stu-id="fc129-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="fc129-117">A harmadik parancs frissíti a végpontot a Traffic Managerben úgy, hogy megfeleljen a helyi $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fc129-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="fc129-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc129-118">PARAMETERS</span></span>

### <span data-ttu-id="fc129-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc129-119">-DefaultProfile</span></span>
<span data-ttu-id="fc129-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc129-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc129-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc129-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="fc129-122">Helyi **TrafficManagerEndpoint-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="fc129-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="fc129-123">Ez a parancsmag frissíti a Traffic Managert, hogy megfeleljen ennek a helyi objektumnak.</span><span class="sxs-lookup"><span data-stu-id="fc129-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc129-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc129-124">CommonParameters</span></span>
<span data-ttu-id="fc129-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc129-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc129-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc129-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc129-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc129-127">INPUTS</span></span>

### <span data-ttu-id="fc129-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc129-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="fc129-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc129-129">OUTPUTS</span></span>

### <span data-ttu-id="fc129-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc129-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="fc129-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc129-131">NOTES</span></span>

## <span data-ttu-id="fc129-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc129-132">RELATED LINKS</span></span>
