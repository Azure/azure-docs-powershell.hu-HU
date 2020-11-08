---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016026"
---
# <span data-ttu-id="c4d19-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c4d19-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="c4d19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4d19-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d19-103">Átjáró diagnosztikát indít a VPN-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c4d19-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="c4d19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4d19-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4d19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4d19-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d19-106">A **Start-AzureVNetGatewayDiagnostics** parancsmag új átjáró-diagnosztikai munkamenetet indít egy virtuális magánhálózati (VPN-) átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c4d19-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="c4d19-107">Egyszerre csak egy átjáró-diagnosztikai munkamenet futhat.</span><span class="sxs-lookup"><span data-stu-id="c4d19-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="c4d19-108">Ha futtatja ezt a parancsmagot egy átjáró-diagnosztikai munkamenet futása közben, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="c4d19-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="c4d19-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c4d19-109">EXAMPLES</span></span>

## <span data-ttu-id="c4d19-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4d19-110">PARAMETERS</span></span>

### <span data-ttu-id="c4d19-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="c4d19-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="c4d19-112">A rögzítés időtartamát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c4d19-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d19-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c4d19-113">-ContainerName</span></span>
<span data-ttu-id="c4d19-114">Egy Azure-tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4d19-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="c4d19-115">Ez a parancsmag a paraméter által megadott tárolóba menti a találatokat.</span><span class="sxs-lookup"><span data-stu-id="c4d19-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="c4d19-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4d19-116">-Profile</span></span>
<span data-ttu-id="c4d19-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c4d19-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c4d19-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c4d19-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4d19-119">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c4d19-119">-StorageContext</span></span>
<span data-ttu-id="c4d19-120">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4d19-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c4d19-121">Ez a parancsmag a paraméter által megadott tárolási környezettel menti az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="c4d19-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d19-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c4d19-122">-VNetName</span></span>
<span data-ttu-id="c4d19-123">Azt a virtuális hálózati átjárót tartalmazó virtuális hálózat, amelyhez ez a parancsmag futtatja a diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="c4d19-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="c4d19-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d19-124">CommonParameters</span></span>
<span data-ttu-id="c4d19-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4d19-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d19-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d19-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d19-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4d19-127">INPUTS</span></span>

## <span data-ttu-id="c4d19-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4d19-128">OUTPUTS</span></span>

## <span data-ttu-id="c4d19-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4d19-129">NOTES</span></span>

## <span data-ttu-id="c4d19-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4d19-130">RELATED LINKS</span></span>

[<span data-ttu-id="c4d19-131">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c4d19-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="c4d19-132">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c4d19-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


