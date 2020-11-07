---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 99f621824d10b574c7f64fb7653bc4154ba6766e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672506"
---
# <span data-ttu-id="e581c-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e581c-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="e581c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e581c-102">SYNOPSIS</span></span>
<span data-ttu-id="e581c-103">A Traffic Manager végpontjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="e581c-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e581c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e581c-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e581c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e581c-105">DESCRIPTION</span></span>
<span data-ttu-id="e581c-106">A **set-AzureRmTrafficManagerEndpoint** parancsmag az Azure Traffic Manager végpontját frissíti.</span><span class="sxs-lookup"><span data-stu-id="e581c-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="e581c-107">Ez a parancsmag frissíti a helyi végpont-objektum beállításait.</span><span class="sxs-lookup"><span data-stu-id="e581c-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="e581c-108">A végpont-objektumot a *TrafficManagerEndpoint* paraméterrel vagy a csővezeték használatával is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="e581c-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="e581c-109">A végpontokat az Get-AzureRmTrafficManagerEndpoint parancsmag használatával is beolvashatja.</span><span class="sxs-lookup"><span data-stu-id="e581c-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="e581c-110">Módosítsa az objektumot helyileg, majd használja a **set-AzureRmTrafficManagerEndpoint** a módosítások véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e581c-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="e581c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e581c-111">EXAMPLES</span></span>

### <span data-ttu-id="e581c-112">Példa 1: végpont frissítése</span><span class="sxs-lookup"><span data-stu-id="e581c-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e581c-113">Az első parancs az Azure Traffic Manager végpontját a **Get-AzureRmTrafficManagerEndpoint** parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e581c-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="e581c-114">A parancs helyileg, a $TrafficManagerEndpoint változóban tárolja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="e581c-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="e581c-115">A második parancs helyileg módosítja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="e581c-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="e581c-116">Ez a parancs 20 értékre módosítja a végpont vastagságát.</span><span class="sxs-lookup"><span data-stu-id="e581c-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="e581c-117">A harmadik parancs a forgalmi vezető végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="e581c-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e581c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e581c-118">PARAMETERS</span></span>

### <span data-ttu-id="e581c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e581c-119">-DefaultProfile</span></span>
<span data-ttu-id="e581c-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e581c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e581c-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e581c-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e581c-122">Helyi **TrafficManagerEndpoint** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e581c-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e581c-123">Ez a parancsmag frissíti a Traffic Manager alkalmazást a helyi objektum egyeztetéséhez.</span><span class="sxs-lookup"><span data-stu-id="e581c-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e581c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e581c-124">CommonParameters</span></span>
<span data-ttu-id="e581c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e581c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e581c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e581c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e581c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e581c-127">INPUTS</span></span>

### <span data-ttu-id="e581c-128">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e581c-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e581c-129">Ez a parancsmag a **TrafficManagerEndpoint** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="e581c-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="e581c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e581c-130">OUTPUTS</span></span>

### <span data-ttu-id="e581c-131">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e581c-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e581c-132">Ez a parancsmag egy **TrafficManagerEndpoint** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="e581c-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="e581c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e581c-133">NOTES</span></span>

## <span data-ttu-id="e581c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e581c-134">RELATED LINKS</span></span>

