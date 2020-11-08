---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016186"
---
# <span data-ttu-id="f3e67-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3e67-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="f3e67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3e67-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e67-103">Azure virtuális hálózati átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f3e67-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="f3e67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3e67-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3e67-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3e67-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e67-106">A **New-AzureVirtualNetworkGateway** parancsmag egy Azure virtuális hálózati átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f3e67-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="f3e67-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3e67-107">EXAMPLES</span></span>

## <span data-ttu-id="f3e67-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3e67-108">PARAMETERS</span></span>

### <span data-ttu-id="f3e67-109">-ASN</span><span class="sxs-lookup"><span data-stu-id="f3e67-109">-Asn</span></span>
<span data-ttu-id="f3e67-110">Az autonóm rendszer számát adja meg (ASN).</span><span class="sxs-lookup"><span data-stu-id="f3e67-110">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e67-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f3e67-111">-Force</span></span>
<span data-ttu-id="f3e67-112">Ne erősítse meg az Azure virtuális hálózati átjáró létrehozását</span><span class="sxs-lookup"><span data-stu-id="f3e67-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e67-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="f3e67-113">-GatewayName</span></span>
<span data-ttu-id="f3e67-114">Az átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3e67-114">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="f3e67-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="f3e67-115">-GatewaySKU</span></span>
<span data-ttu-id="f3e67-116">Annak a virtuális hálózati átjárónak az SKU-számát adja meg, amelyre a parancsmag létrehozta.</span><span class="sxs-lookup"><span data-stu-id="f3e67-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="f3e67-117">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f3e67-117">Valid values are:</span></span>

- <span data-ttu-id="f3e67-118">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="f3e67-118">Default</span></span>
- <span data-ttu-id="f3e67-119">Standard</span><span class="sxs-lookup"><span data-stu-id="f3e67-119">Standard</span></span>
- <span data-ttu-id="f3e67-120">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="f3e67-120">HighPerformance</span></span>

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

### <span data-ttu-id="f3e67-121">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="f3e67-121">-GatewayType</span></span>
<span data-ttu-id="f3e67-122">Az átjáró típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3e67-122">Specifies the type of gateway.</span></span>

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

### <span data-ttu-id="f3e67-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="f3e67-123">-Location</span></span>
<span data-ttu-id="f3e67-124">A helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3e67-124">Specifies the location.</span></span>

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

### <span data-ttu-id="f3e67-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f3e67-125">-PeerWeight</span></span>
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

### <span data-ttu-id="f3e67-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3e67-126">-Profile</span></span>
<span data-ttu-id="f3e67-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f3e67-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3e67-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f3e67-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3e67-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="f3e67-129">-VnetId</span></span>
<span data-ttu-id="f3e67-130">A virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3e67-130">Specifies the ID of a virtual network.</span></span>

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

### <span data-ttu-id="f3e67-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="f3e67-131">-VNetName</span></span>
<span data-ttu-id="f3e67-132">Virtuális hálózatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f3e67-132">Specifies a virtual network.</span></span>

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

### <span data-ttu-id="f3e67-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e67-133">CommonParameters</span></span>
<span data-ttu-id="f3e67-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3e67-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e67-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e67-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e67-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3e67-136">INPUTS</span></span>

## <span data-ttu-id="f3e67-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3e67-137">OUTPUTS</span></span>

## <span data-ttu-id="f3e67-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3e67-138">NOTES</span></span>

## <span data-ttu-id="f3e67-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3e67-139">RELATED LINKS</span></span>

[<span data-ttu-id="f3e67-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3e67-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="f3e67-141">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3e67-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="f3e67-142">Átméretezés-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3e67-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
