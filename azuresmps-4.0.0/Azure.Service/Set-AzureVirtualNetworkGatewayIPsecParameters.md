---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016412"
---
# <span data-ttu-id="e1a6e-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="e1a6e-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="e1a6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a6e-103">Virtuális hálózati átjáró IPsec-paramétereinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="e1a6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1a6e-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e1a6e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1a6e-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a6e-106">A **set-AzureVirtualNetworkGatewayIPsecParameters** parancsmag IPSec-paramétereket állít be egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="e1a6e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1a6e-107">EXAMPLES</span></span>

## <span data-ttu-id="e1a6e-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1a6e-108">PARAMETERS</span></span>

### <span data-ttu-id="e1a6e-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="e1a6e-109">-ConnectedEntityId</span></span>
<span data-ttu-id="e1a6e-110">Egy csatlakoztatott entitás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="e1a6e-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="e1a6e-111">-EncryptionType</span></span>
<span data-ttu-id="e1a6e-112">A virtuális hálózati átjáró titkosítási típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="e1a6e-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e1a6e-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1a6e-114">Nem titkosított</span><span class="sxs-lookup"><span data-stu-id="e1a6e-114">NoEncryption</span></span>
- <span data-ttu-id="e1a6e-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="e1a6e-115">RequireEncryption</span></span>

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

### <span data-ttu-id="e1a6e-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e1a6e-116">-GatewayId</span></span>
<span data-ttu-id="e1a6e-117">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="e1a6e-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="e1a6e-118">-PfsGroup</span></span>
<span data-ttu-id="e1a6e-119">A tökéletes továbbítási titoktartási (PFS) csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="e1a6e-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e1a6e-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1a6e-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="e1a6e-121">PFS1</span></span>
- <span data-ttu-id="e1a6e-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1a6e-122">None</span></span>

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

### <span data-ttu-id="e1a6e-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="e1a6e-123">-Profile</span></span>
<span data-ttu-id="e1a6e-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e1a6e-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1a6e-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="e1a6e-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="e1a6e-127">A biztonsági társítás (SA) méretét kilobájtban adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="e1a6e-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="e1a6e-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="e1a6e-129">A biztonsági társítás másodpercben megadott időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1a6e-129">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="e1a6e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a6e-130">CommonParameters</span></span>
<span data-ttu-id="e1a6e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1a6e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a6e-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a6e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a6e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1a6e-133">INPUTS</span></span>

## <span data-ttu-id="e1a6e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1a6e-134">OUTPUTS</span></span>

## <span data-ttu-id="e1a6e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1a6e-135">NOTES</span></span>

## <span data-ttu-id="e1a6e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1a6e-136">RELATED LINKS</span></span>

[<span data-ttu-id="e1a6e-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="e1a6e-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


