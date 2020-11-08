---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195646"
---
# <span data-ttu-id="86bee-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86bee-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="86bee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86bee-102">SYNOPSIS</span></span>
<span data-ttu-id="86bee-103">A Traffic Manager végpontjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="86bee-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="86bee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86bee-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86bee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86bee-105">DESCRIPTION</span></span>
<span data-ttu-id="86bee-106">A **set-AzTrafficManagerEndpoint** parancsmag az Azure Traffic Manager végpontját frissíti.</span><span class="sxs-lookup"><span data-stu-id="86bee-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="86bee-107">Ez a parancsmag frissíti a helyi végpont-objektum beállításait.</span><span class="sxs-lookup"><span data-stu-id="86bee-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="86bee-108">A végpont-objektumot a *TrafficManagerEndpoint* paraméterrel vagy a csővezeték használatával is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="86bee-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="86bee-109">A végpontokat az Get-AzTrafficManagerEndpoint parancsmag használatával is beolvashatja.</span><span class="sxs-lookup"><span data-stu-id="86bee-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="86bee-110">Módosítsa az objektumot helyileg, majd használja a **set-AzTrafficManagerEndpoint** a módosítások véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="86bee-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="86bee-111">Példák</span><span class="sxs-lookup"><span data-stu-id="86bee-111">EXAMPLES</span></span>

### <span data-ttu-id="86bee-112">Példa 1: végpont frissítése</span><span class="sxs-lookup"><span data-stu-id="86bee-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="86bee-113">Az első parancs az Azure Traffic Manager végpontját a **Get-AzTrafficManagerEndpoint** parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86bee-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="86bee-114">A parancs helyileg, a $TrafficManagerEndpoint változóban tárolja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="86bee-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="86bee-115">A második parancs helyileg módosítja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="86bee-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="86bee-116">Ez a parancs 20 értékre módosítja a végpont vastagságát.</span><span class="sxs-lookup"><span data-stu-id="86bee-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="86bee-117">A harmadik parancs a forgalmi vezető végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="86bee-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="86bee-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86bee-118">PARAMETERS</span></span>

### <span data-ttu-id="86bee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86bee-119">-DefaultProfile</span></span>
<span data-ttu-id="86bee-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86bee-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86bee-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86bee-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="86bee-122">Helyi **TrafficManagerEndpoint** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="86bee-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="86bee-123">Ez a parancsmag frissíti a Traffic Manager alkalmazást a helyi objektum egyeztetéséhez.</span><span class="sxs-lookup"><span data-stu-id="86bee-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="86bee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86bee-124">CommonParameters</span></span>
<span data-ttu-id="86bee-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86bee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86bee-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86bee-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86bee-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86bee-127">INPUTS</span></span>

### <span data-ttu-id="86bee-128">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86bee-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="86bee-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86bee-129">OUTPUTS</span></span>

### <span data-ttu-id="86bee-130">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86bee-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="86bee-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86bee-131">NOTES</span></span>

## <span data-ttu-id="86bee-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86bee-132">RELATED LINKS</span></span>