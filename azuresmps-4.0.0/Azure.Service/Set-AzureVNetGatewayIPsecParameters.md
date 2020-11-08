---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016036"
---
# <span data-ttu-id="838f2-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="838f2-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="838f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="838f2-102">SYNOPSIS</span></span>
<span data-ttu-id="838f2-103">A virtuális hálózati átjáró és a helyi hálózati webhely közötti kapcsolat IPsec-paramétereinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="838f2-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="838f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="838f2-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="838f2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="838f2-105">DESCRIPTION</span></span>
<span data-ttu-id="838f2-106">A **set-AzureVNetGatewayIPsecParameters** parancsmag az IP-biztonság (IPSec) és az internetes KULCSCSERE (IKE) paramétereinek beállítása a virtuális hálózati átjáró és egy helyi hálózati webhely közötti kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="838f2-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="838f2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="838f2-107">EXAMPLES</span></span>

## <span data-ttu-id="838f2-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="838f2-108">PARAMETERS</span></span>

### <span data-ttu-id="838f2-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="838f2-109">-EncryptionType</span></span>
<span data-ttu-id="838f2-110">A virtuális hálózati átjáró titkosítási típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="838f2-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="838f2-111">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="838f2-111">Valid values are:</span></span> 

- <span data-ttu-id="838f2-112">Nem titkosított</span><span class="sxs-lookup"><span data-stu-id="838f2-112">NoEncryption</span></span> 
- <span data-ttu-id="838f2-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="838f2-113">RequireEncryption</span></span>

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

### <span data-ttu-id="838f2-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="838f2-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="838f2-115">Annak a helyi hálózati webhelynek a neve, amelyen a parancsmag az IPsec és az IKE paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="838f2-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="838f2-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="838f2-116">-PfsGroup</span></span>
<span data-ttu-id="838f2-117">A tökéletes továbbítási titoktartási (PFS) csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="838f2-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="838f2-118">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="838f2-118">Valid values are:</span></span> 

- <span data-ttu-id="838f2-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="838f2-119">PFS1</span></span> 
- <span data-ttu-id="838f2-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="838f2-120">None</span></span>

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

### <span data-ttu-id="838f2-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="838f2-121">-Profile</span></span>
<span data-ttu-id="838f2-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="838f2-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="838f2-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="838f2-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="838f2-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="838f2-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="838f2-125">A biztonsági társítás (SA) méretét kilobájtban adja meg.</span><span class="sxs-lookup"><span data-stu-id="838f2-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="838f2-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="838f2-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="838f2-127">A biztonsági társítás másodpercben megadott időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="838f2-127">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="838f2-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="838f2-128">-VNetName</span></span>
<span data-ttu-id="838f2-129">Annak a virtuális hálózatnak a megadása, amelyhez a parancsmag az IPsec-paramétereket állítja be a kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="838f2-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="838f2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838f2-130">CommonParameters</span></span>
<span data-ttu-id="838f2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="838f2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838f2-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838f2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838f2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="838f2-133">INPUTS</span></span>

## <span data-ttu-id="838f2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="838f2-134">OUTPUTS</span></span>

## <span data-ttu-id="838f2-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="838f2-135">NOTES</span></span>

## <span data-ttu-id="838f2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="838f2-136">RELATED LINKS</span></span>

[<span data-ttu-id="838f2-137">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="838f2-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


