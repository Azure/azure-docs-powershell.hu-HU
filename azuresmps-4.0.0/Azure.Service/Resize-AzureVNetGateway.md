---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016087"
---
# <span data-ttu-id="b9123-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b9123-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="b9123-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9123-102">SYNOPSIS</span></span>
<span data-ttu-id="b9123-103">VPN-átjáró átméretezése</span><span class="sxs-lookup"><span data-stu-id="b9123-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="b9123-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9123-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9123-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9123-105">DESCRIPTION</span></span>
<span data-ttu-id="b9123-106">Az **átméretezés-AzureVNetGateway** parancsmag a virtuális hálózat virtuális MAGÁNHÁLÓZATI (VPN) átjáróját egy másik SKU-ba méretezi át.</span><span class="sxs-lookup"><span data-stu-id="b9123-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="b9123-107">A virtuális hálózati átjáró érvényes SKU-je alapértelmezés szerint normál és HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="b9123-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="b9123-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b9123-108">EXAMPLES</span></span>

### <span data-ttu-id="b9123-109">Példa 1: virtuális hálózati átjáró SKU-ának módosítása</span><span class="sxs-lookup"><span data-stu-id="b9123-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="b9123-110">Ez a parancs a virtuális hálózati átjáró SKU-ContosoVN07 a HighPerformance nevű virtuális hálózat számára módosítja.</span><span class="sxs-lookup"><span data-stu-id="b9123-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="b9123-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9123-111">PARAMETERS</span></span>

### <span data-ttu-id="b9123-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="b9123-112">-GatewaySKU</span></span>
<span data-ttu-id="b9123-113">Azt a SKU-ot adja meg, amelyre ez a parancsmag átméretezi a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="b9123-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="b9123-114">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b9123-114">Valid values are:</span></span> 

- <span data-ttu-id="b9123-115">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="b9123-115">Default</span></span> 
- <span data-ttu-id="b9123-116">Standard</span><span class="sxs-lookup"><span data-stu-id="b9123-116">Standard</span></span> 
- <span data-ttu-id="b9123-117">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="b9123-117">HighPerformance</span></span>

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

### <span data-ttu-id="b9123-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="b9123-118">-Profile</span></span>
<span data-ttu-id="b9123-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b9123-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b9123-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b9123-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b9123-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b9123-121">-VNetName</span></span>
<span data-ttu-id="b9123-122">Annak a virtuális hálózatnak a meghatározása, amelyben ez a parancsmag átméretezi a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="b9123-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

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

### <span data-ttu-id="b9123-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9123-123">CommonParameters</span></span>
<span data-ttu-id="b9123-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9123-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9123-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9123-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9123-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9123-126">INPUTS</span></span>

## <span data-ttu-id="b9123-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9123-127">OUTPUTS</span></span>

## <span data-ttu-id="b9123-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9123-128">NOTES</span></span>

## <span data-ttu-id="b9123-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9123-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9123-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b9123-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="b9123-131">Új – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b9123-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="b9123-132">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b9123-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="b9123-133">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b9123-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="b9123-134">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="b9123-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


