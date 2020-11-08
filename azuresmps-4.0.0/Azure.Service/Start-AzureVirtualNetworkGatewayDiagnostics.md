---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015772"
---
# <span data-ttu-id="5463e-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5463e-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="5463e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5463e-102">SYNOPSIS</span></span>
<span data-ttu-id="5463e-103">Elindítja a diagnosztikát a virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5463e-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="5463e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5463e-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5463e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5463e-105">DESCRIPTION</span></span>
<span data-ttu-id="5463e-106">A **Start-AzureVirtualNetworkGatewayDiagnostics** parancsmag új átjáró-diagnosztikai munkamenetet indít a virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5463e-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="5463e-107">Egyszerre csak egy átjáró-diagnosztikai munkamenet futhat.</span><span class="sxs-lookup"><span data-stu-id="5463e-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="5463e-108">Ha futtatja ezt a parancsmagot egy átjáró-diagnosztikai munkamenet futása közben, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="5463e-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="5463e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5463e-109">EXAMPLES</span></span>

## <span data-ttu-id="5463e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5463e-110">PARAMETERS</span></span>

### <span data-ttu-id="5463e-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="5463e-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="5463e-112">A rögzítés időtartamát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="5463e-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5463e-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5463e-113">-ContainerName</span></span>
<span data-ttu-id="5463e-114">Egy Azure-tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5463e-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="5463e-115">Ez a parancsmag a paraméter által megadott tárolóba menti a találatokat.</span><span class="sxs-lookup"><span data-stu-id="5463e-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5463e-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5463e-116">-GatewayId</span></span>
<span data-ttu-id="5463e-117">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5463e-117">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5463e-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="5463e-118">-Profile</span></span>
<span data-ttu-id="5463e-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5463e-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5463e-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5463e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5463e-121">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="5463e-121">-StorageContext</span></span>
<span data-ttu-id="5463e-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5463e-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5463e-123">Ez a parancsmag a paraméter által megadott tárolási környezettel menti az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="5463e-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5463e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5463e-124">CommonParameters</span></span>
<span data-ttu-id="5463e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5463e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5463e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5463e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5463e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5463e-127">INPUTS</span></span>

## <span data-ttu-id="5463e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5463e-128">OUTPUTS</span></span>

## <span data-ttu-id="5463e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5463e-129">NOTES</span></span>

## <span data-ttu-id="5463e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5463e-130">RELATED LINKS</span></span>

[<span data-ttu-id="5463e-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5463e-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="5463e-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5463e-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


